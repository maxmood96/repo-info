## `wordpress:cli-2.12-php8.3`

```console
$ docker pull wordpress@sha256:5ad48e48c088018bcb6278ecdddc838048a63141755eb1e9e3a663a409b35ebf
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

### `wordpress:cli-2.12-php8.3` - linux; amd64

```console
$ docker pull wordpress@sha256:a44494afed993374c1a50c5160734f2b11171161b320f83a4b9f95c655260a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64474422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b324c67b1a6105075f963e1bfbc2d15cd05d0377407b60be7f665da904e6a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:50:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:50:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:50:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:50:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:50:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:50:13 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:03:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:06:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:06:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:06:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:06:12 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:14:37 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:14:37 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:14:37 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:15:20 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:20 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:22 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:15:22 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:15:22 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:15:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:15:22 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:22 GMT
USER www-data
# Tue, 02 Dec 2025 01:15:22 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4ac052393b4cb84e6b1e06bb2d149b027d3a1aa06015d318b8fbfdc40ecf2`  
		Last Modified: Thu, 20 Nov 2025 19:53:50 GMT  
		Size: 3.5 MB (3463764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e334d186cbc72b6715bf607ab20ecf706cdd17da2992ef4b76c9590e2bfe82`  
		Last Modified: Thu, 20 Nov 2025 19:53:50 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465489b7241905031cd3f19ac1ed1feb46020d4fa06bbf5593af161ed947687`  
		Last Modified: Thu, 20 Nov 2025 19:53:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137fd31665e7c711f192fc5c6605c0a9803950096a872e4cadd1877b388fcf35`  
		Last Modified: Thu, 20 Nov 2025 20:06:41 GMT  
		Size: 12.6 MB (12625109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0e487b205e35b21aa81f9da7144256d779e4e2d6c83bfc4796375d06aaabb`  
		Last Modified: Thu, 20 Nov 2025 20:06:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cdff07dbec464c1cc7bee82b61175faa152091a17b52c9bc20c8708521688b`  
		Last Modified: Thu, 20 Nov 2025 20:06:44 GMT  
		Size: 17.4 MB (17418247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7430ec884cf40017a9749b6ab65108494598f5fd3085f81f9070ce475c9932`  
		Last Modified: Thu, 20 Nov 2025 20:06:40 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d97ece59e9df4c739d1e31e3cb213f05af7d75b9da5b156e6f23e9ede725f4`  
		Last Modified: Thu, 20 Nov 2025 20:06:40 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f35a757ee6a3ef732269c92351cc1500fdbd489fa07287d3d0fd6d7bc49d57`  
		Last Modified: Thu, 20 Nov 2025 20:06:41 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf669900e16833c4d2cd4bc4e8df47a43be6b4bac875c3ee20adb3f0cb9a3159`  
		Last Modified: Tue, 02 Dec 2025 01:15:55 GMT  
		Size: 11.1 MB (11076283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838824b81601f24aac0c0d54afdfc79a7d03f92a656b19a580a56f172d0ce82f`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 14.5 MB (14518286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c1b43facf346332da1de8a1876ca32c92ef6192a6d56d7f69b431c11482ca`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae596bd8d424b90dc79c9aedde16c995903293c96b5f05dc9b354f66696f0f8`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 1.5 MB (1525170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feed3bb20b17778b9228901c602576a3a93dabecaac553fc5b01f5a7db84d61`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:a4ff57fec1735c85e8c74d212718e09c4842b28b120b82c9546a0724442b39f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b2c15155869dd7d960983bc2d3fc99e034e849bdc35178ac30743d069ce14f`

```dockerfile
```

-	Layers:
	-	`sha256:1b855921794403cce8ff57926dee292bb48c72ab17cac2905cc450f0eb1c34c0`  
		Last Modified: Tue, 02 Dec 2025 02:33:30 GMT  
		Size: 599.1 KB (599107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d80cb0f54a4c6c724971acec81c9e3f09cad6167ce0e00bd510082ae14d799`  
		Last Modified: Tue, 02 Dec 2025 02:33:31 GMT  
		Size: 43.3 KB (43321 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:2eed85c0b9f4b032fdbdfb1b5559fbd29b0e42190fa559afc04d9162a7f8dad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59159677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e36e1079da4581fe2df2bc6190abd12968daac2ea236d73ed0c4e1419c199f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:45:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:45:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:45:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:45:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:45:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:45:13 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 19:57:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:57:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:00:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:00:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:00:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:00:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:00:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:00:30 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:04:38 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:04:38 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:04:38 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:05:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:05:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:05:55 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:05:55 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:05:55 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:05:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:05:55 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:05:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:05:55 GMT
USER www-data
# Tue, 02 Dec 2025 01:05:55 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d10eddd420460cddc455bf7050a161541e652e39a7c43aa5d4f52fb19f2828`  
		Last Modified: Thu, 20 Nov 2025 19:48:40 GMT  
		Size: 3.4 MB (3428331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ca95a81a2f7721adcc3c330200c289823e26bb898d6babfd3ac1a51b05dd49`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9bc7c7fc556dff05cf262185851000fb3715c543d8b79013eb88a442641293`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72dc1156432d463bbe9845807bfde419f13d4247a62ad9bb89212435d948e13`  
		Last Modified: Thu, 20 Nov 2025 20:01:01 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d138839efecbb0885b72b0e10bc00ab2ec66a66a93a293cdf70c3bc946f07`  
		Last Modified: Thu, 20 Nov 2025 20:01:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620991f0a48175bb7a8df531e8dfad647e395e2cda92719c1035399d82423341`  
		Last Modified: Thu, 20 Nov 2025 20:01:02 GMT  
		Size: 15.8 MB (15794857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64191400ef3991d3f29f31fca45c7781707b2957a8ce8bcbc12ac32cdff45d1`  
		Last Modified: Thu, 20 Nov 2025 20:01:00 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e383ad03013b8bda487ea38d708c732b1444f88445ca2e55ccdce0246b51b9`  
		Last Modified: Thu, 20 Nov 2025 20:01:01 GMT  
		Size: 19.9 KB (19869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a24f420f4f47505d45022d88ed4b64b50625390a36346c1a009254a70ea0137`  
		Last Modified: Thu, 20 Nov 2025 20:01:00 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962a2fd7ef9e0c8030039e1834886c1d77c2b62e79ee4d434576b743105f4ebf`  
		Last Modified: Tue, 02 Dec 2025 02:35:55 GMT  
		Size: 10.8 MB (10776108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7066e11d2fdb11112439fc9e0072fe37edb623117b306c293bf8922daae2692`  
		Last Modified: Tue, 02 Dec 2025 02:35:53 GMT  
		Size: 11.5 MB (11461357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4e57612d13b94d837683fdcdda7f6dbfe6822436aa1bec9b0f55bd0e3587ae`  
		Last Modified: Tue, 02 Dec 2025 01:15:21 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3156be3e11f2507632d01e45b9b30a6287e711e91810708eaeb7c8bcd8a821`  
		Last Modified: Tue, 02 Dec 2025 01:15:26 GMT  
		Size: 1.5 MB (1525151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2759fdfe82e3648c1550916e9754a77b388384b3264446413f09b95d32b18c`  
		Last Modified: Tue, 02 Dec 2025 01:15:29 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:92e080a7083e6c1c4963617bbb38a00626743a5f40c3a3e78a9d01d70e94b03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 KB (43271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f70edeb51ba15653cd9433b52ae31b30a7975520d4a4581c1e41f9906579c4`

```dockerfile
```

-	Layers:
	-	`sha256:8fedc6f957cf85cd5171820e162d88966838f4cc12c7ff7866021699831017e0`  
		Last Modified: Tue, 02 Dec 2025 02:33:34 GMT  
		Size: 43.3 KB (43271 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:232990898f54d128d0146cca27aa55389b4db882ea4db4ad83023230a480fbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58271017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c6e9a875ee3c9a72d2d364ede2c2182a342cb20b7c16ffa096bd35e03ac21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:16:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:16:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:16:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:16:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:16:10 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:16:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:16:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:18:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:18:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:19:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:19:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:19:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:19:00 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:16:03 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:16:03 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:16:03 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:17:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:15 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:17 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:17:17 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:17:17 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:17:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:17:17 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:17 GMT
USER www-data
# Tue, 02 Dec 2025 01:17:17 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749cb513e69c469d6084d27642a0381f732906a029a0302757e0ab8f39333310`  
		Last Modified: Thu, 20 Nov 2025 20:26:45 GMT  
		Size: 3.2 MB (3244395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f306556a8a0c6d53d06ebd40d4df9070c23542afb635c8c5611f4cb0c89efa1`  
		Last Modified: Thu, 20 Nov 2025 20:26:45 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd988ee1dc8e147c59b671201805243ce7c63eeeb830bfeafdee2ac67701dae`  
		Last Modified: Thu, 20 Nov 2025 20:26:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79ea2404ab7f497e13507cf3e2c2254e9a62d3c350358749b39ffe42788a6b`  
		Last Modified: Thu, 20 Nov 2025 20:26:40 GMT  
		Size: 12.6 MB (12625101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e720263c3b96e0567c8cebf6adfd810bf7da45b23728ca4412c09a94f3b8ea7`  
		Last Modified: Thu, 20 Nov 2025 20:26:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9894031234f37f6a0939e295b8d87e423661da638fa68f76f10c92c08c73d97c`  
		Last Modified: Thu, 20 Nov 2025 20:26:50 GMT  
		Size: 14.9 MB (14863196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1487ff50a530fc8d19ac88da7b10cd36f7a098a8f70302b15e4ecfb20249a66`  
		Last Modified: Thu, 20 Nov 2025 20:26:41 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b521d0cabbc98b8aa0a6e84005ffcc9ef62a4b86c2fca1b387ab142adfe1f30d`  
		Last Modified: Thu, 20 Nov 2025 20:26:47 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300db6343639d76fe46b6265bc787ea01477a054666b28f8a2cc6729f95f91ee`  
		Last Modified: Thu, 20 Nov 2025 20:26:37 GMT  
		Size: 19.9 KB (19850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5264016d3674606fad6b9609dd18d0ccafeb8d51c1dd31cef73e51dbbd8d42a`  
		Last Modified: Tue, 02 Dec 2025 01:17:38 GMT  
		Size: 10.4 MB (10447573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd90c9ec41d2200cedd479dfd5972b776dcbb87957a45fb44874add36cae8fcf`  
		Last Modified: Tue, 02 Dec 2025 01:17:38 GMT  
		Size: 12.3 MB (12299425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b88e2209c88615dfbb67d7036766fe7fcc2e07fb939a17f0eb3e13999ed71f`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9501b260bf6384144dc3d429fa47a08ebaa24a98f76bd8ba639b55dc245b7542`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 1.5 MB (1525119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fcef7dd22e3700f171d5d353dd0a496a0e471940ee73cdd91389c1b3d0dfe8`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:ebc7fd3b2978e0ce790a6ae44df3ecb3738be03af5a3b4455c3220262548bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 KB (641417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc38b4d8be91d5a1f53f94e828b10f69312b6efc77fde2db941e9082b87ff4ba`

```dockerfile
```

-	Layers:
	-	`sha256:c387f2e097aeec294bd0a64f4f7dc2a6f0fc2175a8513d234276388b89afe1b2`  
		Last Modified: Tue, 02 Dec 2025 02:33:37 GMT  
		Size: 597.9 KB (597931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa464a8235389040b24e68d825b1887438bf1659bb2ffac2a0340da67dbd7ff`  
		Last Modified: Tue, 02 Dec 2025 02:33:38 GMT  
		Size: 43.5 KB (43486 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:12077986b0cefe82045ce1eda977a1e9747bafccb18b187092e79f61c7342745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab13ec762f81ba8a6b0646f422a1eab589270b9fad220105753a50271141469`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:06:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:06:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:06:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:06:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:06:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:06:28 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:06:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:06:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:11:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:11:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:11:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:11:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:11:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:11:16 GMT
CMD ["php" "-a"]
# Thu, 20 Nov 2025 21:15:23 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 20 Nov 2025 21:15:23 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 20 Nov 2025 21:15:23 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 21:16:32 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 21:16:32 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 20 Nov 2025 21:16:34 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 20 Nov 2025 21:16:34 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 20 Nov 2025 21:16:34 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 20 Nov 2025 21:16:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 20 Nov 2025 21:16:34 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:16:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:16:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:16:34 GMT
USER www-data
# Thu, 20 Nov 2025 21:16:34 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847da6e7e44e7784184d99d16b0bea848655b28660be1c2c117629145fb2518`  
		Last Modified: Thu, 20 Nov 2025 20:58:55 GMT  
		Size: 3.5 MB (3466806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8535d2042df4a6dbbb9908c7a973fbd4c2103c77c223bb8b9921fb087ca72b43`  
		Last Modified: Thu, 20 Nov 2025 20:58:55 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e28b7feca258595386f80a27355340570ea1254571177fc79b4aadc65a2e5d`  
		Last Modified: Thu, 20 Nov 2025 20:58:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c4487d4842cc153b9b8c2de0ded707c9af8f3f2241e75cabccfecbc01cbba5`  
		Last Modified: Thu, 20 Nov 2025 21:15:22 GMT  
		Size: 12.6 MB (12625109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6a9a8afa3d6f0d5d886725a001a5a8677f24f9a47deeade37dde14a4c89008`  
		Last Modified: Thu, 20 Nov 2025 20:59:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963e3ac8585daff44b9d600c514fd5ef0ea6f3eab58fb21944634cc2f0a80bc6`  
		Last Modified: Thu, 20 Nov 2025 21:15:22 GMT  
		Size: 17.3 MB (17324295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8b43992f12623bac7c0576d31c34e493ec52f5ab0f5c3a2c5fec8589727321`  
		Last Modified: Thu, 20 Nov 2025 20:58:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149036800d48dace93d7f7736588ad714db9161bdbed7cd8e36e4005942573b6`  
		Last Modified: Thu, 20 Nov 2025 20:58:54 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21687b3501e0d952d1c93429f876e070194ac6de5ccb80c3fb590b0700e7fec`  
		Last Modified: Thu, 20 Nov 2025 20:58:54 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89502f8e0fa5861116695aa3b5276f64ed8080dcef3241ba9cde715de25e1451`  
		Last Modified: Thu, 20 Nov 2025 21:16:52 GMT  
		Size: 11.1 MB (11080288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e8a04caf1a6303546be9c77fe97ec84053efa69828583921ac93962444aaf9`  
		Last Modified: Thu, 20 Nov 2025 21:16:53 GMT  
		Size: 14.2 MB (14211294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec41d5d32c7bc1ac93d090c842acaf14d075cce211f66a68657a833e9aa4075`  
		Last Modified: Thu, 20 Nov 2025 21:16:51 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c4b0959e053c9f2776e93e5848867c1ab0e3d6b9b58a4def32ee2e42aa3155`  
		Last Modified: Thu, 20 Nov 2025 21:16:51 GMT  
		Size: 1.5 MB (1525132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d2f679bbbf0ab4e8c4a758f6e88ea968205f8b5e64d2e25a74c028577a167`  
		Last Modified: Thu, 20 Nov 2025 21:16:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:839c7c9c3e657b73711c6931c5aa3ae6d900410f898f26a596d72e4209a80243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 KB (641438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47d62c99b967f46358e2993c6aafbced06f9be895c7cd00c1772f449fd9f80c`

```dockerfile
```

-	Layers:
	-	`sha256:e0191163ec656e61755575da2336a27483c77384960b24f4c061d5120d147d50`  
		Last Modified: Thu, 20 Nov 2025 23:28:17 GMT  
		Size: 598.0 KB (597967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590bb3cbe25ea3c30500973f623cfcc319b51602497e930e615797847e56f795`  
		Last Modified: Thu, 20 Nov 2025 23:28:18 GMT  
		Size: 43.5 KB (43471 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; 386

```console
$ docker pull wordpress@sha256:5de600d7c5418d8d9bdf3497078a9cbc63549beb5933443464166e45a4e247a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63806665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cdd03d8bb98ee274fd88eaba002a118e60f5b5e96363be21737179cf787ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:59:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:59:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:59:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:59:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:59:45 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:03:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:03:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:06:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:06:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:06:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:06:48 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:10:08 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:10:08 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:10:08 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:11:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:11:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:11:04 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:11:04 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:11:04 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:11:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:11:04 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:11:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:11:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:11:04 GMT
USER www-data
# Tue, 02 Dec 2025 01:11:04 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f039de99adca0bfbabfa840c41c9b5faa5d85fc19ee172df914c09156ffe348`  
		Last Modified: Thu, 20 Nov 2025 20:03:21 GMT  
		Size: 3.5 MB (3522955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b7d55bad39b60da02eb5e137714d8da316ccbe2e3b9e305d1d0f603f6a099`  
		Last Modified: Thu, 20 Nov 2025 20:03:21 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40ea2314b2f2e4e2d7c3d449a2be63af6b10dc635a1f911f266c515f4321581`  
		Last Modified: Thu, 20 Nov 2025 20:03:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9b8b22c3cc05570c3e5f1b2db3e48b23575af4641a32dafe5be18ab76f2293`  
		Last Modified: Thu, 20 Nov 2025 20:07:06 GMT  
		Size: 12.6 MB (12625079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9207a68d68da59d6cae8342b240e3b77da5a2b72fc7c63181d2af37b1010ec8`  
		Last Modified: Thu, 20 Nov 2025 20:07:09 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6390301cdad6c886c85e841c26382e719733b7484d6d99c805f0af57a7e8c164`  
		Last Modified: Thu, 20 Nov 2025 20:07:10 GMT  
		Size: 17.8 MB (17836138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36155caca8189b0f0ee211ec19ecfccc987aeeda8ceb676f57cce73375c4552`  
		Last Modified: Thu, 20 Nov 2025 20:07:09 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81524b4287ebf8f997fa2a15c1d440bbc0317ec9e790ff0660510e0ba14ebf`  
		Last Modified: Thu, 20 Nov 2025 20:07:09 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30b095d12feb4b59ce87e91b0fff9b34d37443e6e6a11cbe50d26caeb4da87`  
		Last Modified: Thu, 20 Nov 2025 20:07:09 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3846f7885f9f4bef981bbaed0460459b3a2820dd749ac838f736c31256b563e`  
		Last Modified: Tue, 02 Dec 2025 01:11:21 GMT  
		Size: 11.3 MB (11274978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5407700ff345f5f91f1307656dbda3d115e7988f3d123a5ee6f1a66a924faad`  
		Last Modified: Tue, 02 Dec 2025 01:11:21 GMT  
		Size: 13.4 MB (13358401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5f626f1a587c3511f2abc333c244762e7dbc83cb1ac0061117f93484416ed3`  
		Last Modified: Tue, 02 Dec 2025 01:11:21 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811707da3ab8578771da2143589d86496d7a3f09c99d8666b96a5f82e326d9cb`  
		Last Modified: Tue, 02 Dec 2025 01:11:20 GMT  
		Size: 1.5 MB (1525135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec9e3005ec928f5f68bc9f5856236451a7613e0c0e5105d314208797d3008a7`  
		Last Modified: Tue, 02 Dec 2025 01:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:3538c72b4208f82d08ab10fa0113721c4616859124acfd219aec8602975f4d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfbeeed70882cc1a5ed0ce6e17c0875c0db41f52b009dfb419def5d83cd8eec`

```dockerfile
```

-	Layers:
	-	`sha256:1049c23ed6a192bcb42cfaedfc987a1014ab6b2c7a4fcba18f30714fdbc36c14`  
		Last Modified: Tue, 02 Dec 2025 02:33:44 GMT  
		Size: 599.1 KB (599062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb922c384ffc8a1fdfd15f308415c7f2e4986b4c70d8b22b465cf856b97dc27`  
		Last Modified: Tue, 02 Dec 2025 02:33:45 GMT  
		Size: 43.3 KB (43261 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:c46dab47e65400d352118f43abfb9f50a57ef7b142617c7d2e6d2deca058d6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65632921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a25f045c3fcb1da2d528d8b6fc47c20e9a030469b962172b68546b8ba897b79`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_VERSION=8.3.28
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 21:20:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 21:20:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:24:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 21:24:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:24:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 21:24:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 21:24:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 21:24:54 GMT
CMD ["php" "-a"]
# Thu, 20 Nov 2025 22:25:05 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 20 Nov 2025 22:25:05 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 20 Nov 2025 22:25:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 22:26:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 22:26:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 20 Nov 2025 22:26:33 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 20 Nov 2025 22:26:33 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 20 Nov 2025 22:26:33 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 20 Nov 2025 22:26:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 20 Nov 2025 22:26:33 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 22:26:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 22:26:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 22:26:34 GMT
USER www-data
# Thu, 20 Nov 2025 22:26:34 GMT
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
	-	`sha256:b53971e004648f8982fc3b37775bc935a3e17a526dffea78cab354e2849bfd0d`  
		Last Modified: Thu, 20 Nov 2025 21:25:17 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd2a999bdbd1916d536ced797c2f38b0416bdf9b4e4d63ebb04063c3aefe64`  
		Last Modified: Thu, 20 Nov 2025 21:25:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a947f250baf1bbf1ee3063b502095f34589e35f6f9255466f62627d23adf8`  
		Last Modified: Thu, 20 Nov 2025 21:25:18 GMT  
		Size: 18.3 MB (18266164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d9cec30a72de21622045bf26e71704ba5019b56da63167ae1717d2dd23fec5`  
		Last Modified: Thu, 20 Nov 2025 21:25:16 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b6ada8aed16ccd52f10895c67dd3193b33bb59354b73a7e5578682a3ab3aff`  
		Last Modified: Thu, 20 Nov 2025 21:25:16 GMT  
		Size: 19.9 KB (19880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0fff8bc2005844324eede9c1eed46cdabcd19d2f0b55611c46d598f2553f84`  
		Last Modified: Thu, 20 Nov 2025 21:25:16 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261fa7d755158c148503fda9f27bfb21effccd4c9fd1dbd63987306129d1e46`  
		Last Modified: Thu, 20 Nov 2025 22:27:11 GMT  
		Size: 11.7 MB (11690062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3795443889ca27366eb9b48201752331395089cf82a14a9fd9ebcc924a804d1`  
		Last Modified: Thu, 20 Nov 2025 22:27:10 GMT  
		Size: 14.1 MB (14134849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d21b6fd90006ddb7a63368824109d109be4e25a70aa824d05bfd5c8d599ef0`  
		Last Modified: Thu, 20 Nov 2025 22:27:09 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae65baedb8845128f692e49f781a78cebaf334b99d0b00cc64468da3e8575de`  
		Last Modified: Thu, 20 Nov 2025 22:27:09 GMT  
		Size: 1.5 MB (1525126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630bea29b47f3430a4296923f082f03821ad79f2ea45df88aff4940944d545c2`  
		Last Modified: Thu, 20 Nov 2025 22:27:08 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:b1c71ca4c4a6792d74479e2ce43dac465dbdeaec4e75dba835962cc2aab26857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f865c7d0cce60dc1ac4e5d211159a4ec03c039399eaf0672776668e375a0e0`

```dockerfile
```

-	Layers:
	-	`sha256:48ec9929611ee41e66497c3e80fc896f35bb29745cf995fe95ea8588204fed30`  
		Last Modified: Thu, 20 Nov 2025 23:28:25 GMT  
		Size: 596.0 KB (595970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666cb9ed1c953eb97a6937638882aa2810a0cf692484f24b7874569e097a19e2`  
		Last Modified: Thu, 20 Nov 2025 23:28:26 GMT  
		Size: 43.3 KB (43336 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; riscv64

```console
$ docker pull wordpress@sha256:9010a667f343077cdb5e2f5b2278f42b7e0b8cd8aba11ad7689befa69277fecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61693543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67b87ef6b0b349b1ac8b0ed4c1d78570ef77b255ea29b4e5c21bf095d4452a4`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.3.28
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Sat, 22 Nov 2025 15:38:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 22 Nov 2025 15:38:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 16:31:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 22 Nov 2025 16:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 16:31:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 22 Nov 2025 16:31:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 22 Nov 2025 16:31:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 22 Nov 2025 16:31:44 GMT
CMD ["php" "-a"]
# Sun, 23 Nov 2025 03:13:36 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sun, 23 Nov 2025 03:13:36 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sun, 23 Nov 2025 03:13:36 GMT
WORKDIR /var/www/html
# Sun, 23 Nov 2025 03:26:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sun, 23 Nov 2025 03:26:58 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sun, 23 Nov 2025 03:27:09 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sun, 23 Nov 2025 03:27:09 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sun, 23 Nov 2025 03:27:09 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sun, 23 Nov 2025 03:27:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sun, 23 Nov 2025 03:27:09 GMT
VOLUME [/var/www/html]
# Sun, 23 Nov 2025 03:27:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 23 Nov 2025 03:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 23 Nov 2025 03:27:09 GMT
USER www-data
# Sun, 23 Nov 2025 03:27:09 GMT
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
	-	`sha256:1991964637c5dacf87db7d4b063b50de6a499256ab7e57a034d7fbb66130c70c`  
		Last Modified: Sat, 22 Nov 2025 16:32:54 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851189fe88fff06f1beb5b7e6faad5356c44b7bfc59f4b4a31ba142d162b867c`  
		Last Modified: Sat, 22 Nov 2025 16:32:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63735985999752c21b7fc85404216cba46dfd42069725b62e27fd486dec5a5fd`  
		Last Modified: Sat, 22 Nov 2025 16:32:52 GMT  
		Size: 16.9 MB (16924834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d9a020419592242155891609d64e8cd7c9a35e95b7e9b9b555c58677206ac`  
		Last Modified: Sat, 22 Nov 2025 16:32:57 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1ff26237bc191efd2ef55df2cd9e27410546c1b4c3350235135dc052c391c3`  
		Last Modified: Sat, 22 Nov 2025 16:32:51 GMT  
		Size: 19.9 KB (19865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7a09a73e1b32cb4d04ac7da75bdf1ed1483483d63f5d01cde7df93f619b16c`  
		Last Modified: Sat, 22 Nov 2025 16:32:51 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50fa9a0c2fc1e59da30baa64574c4e5908f04facf44737275acd78bdd4051ac`  
		Last Modified: Sun, 23 Nov 2025 03:28:43 GMT  
		Size: 11.6 MB (11571136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821875da92e3abf72bdccc3e3f1f1c3bd77ee2811d32bcd934090430b31a1b5b`  
		Last Modified: Sun, 23 Nov 2025 03:28:42 GMT  
		Size: 11.9 MB (11887122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c28e34c1150d792e0495bc58f54371e3980f629bd2e7b9110b911e9763371`  
		Last Modified: Sun, 23 Nov 2025 03:28:41 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd47695d8d70d216e56dd51204f31d5ae318f029b7f7e975355e109ab27490a`  
		Last Modified: Sun, 23 Nov 2025 03:28:41 GMT  
		Size: 1.5 MB (1525142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da62700ccab9b1fa2b482621bb52949b9c568d6f609593d88920d01a10d2e80`  
		Last Modified: Sun, 23 Nov 2025 03:28:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:d0473e128e516d555bcfcc8819a8d7601d2522fce7e590e11d2cbce5b731d91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f93ee742e8b9985dcda12b082422a7d8c9313a052aa1a90b9d5bef08360976`

```dockerfile
```

-	Layers:
	-	`sha256:45bdc2de946f639013bf1ed524f1e2f8102b31f5ba98e3d0916317b77ae0bff5`  
		Last Modified: Sun, 23 Nov 2025 05:18:45 GMT  
		Size: 596.0 KB (595966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a075dd1b7ce84cac7837d8c966acd886dec36a4d3e4b0ee50aa289edea02c6e`  
		Last Modified: Sun, 23 Nov 2025 05:18:48 GMT  
		Size: 43.3 KB (43336 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:202b1c88dd5e691062d11ab73a3c8857f661213a2fd66e67c5da267d2e5592e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65303051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ff73a0b44e07845293ab23ae014ff5f17b3dad91dd5c0d6b2db1a9f37e5f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:48:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 14 Nov 2025 17:48:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 14 Nov 2025 17:48:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 14 Nov 2025 17:48:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:11:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:11:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:47:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:52:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:52:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:52:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:52:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:52:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:52:21 GMT
CMD ["php" "-a"]
# Thu, 20 Nov 2025 21:25:55 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 20 Nov 2025 21:25:55 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 20 Nov 2025 21:25:55 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 21:31:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 21:31:01 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 20 Nov 2025 21:31:04 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 20 Nov 2025 21:31:04 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 20 Nov 2025 21:31:04 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 20 Nov 2025 21:31:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 20 Nov 2025 21:31:04 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:31:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:31:05 GMT
USER www-data
# Thu, 20 Nov 2025 21:31:05 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21615e7c59e15e1f62a5a7808d0f5410d99d33eb1fa9e2321034798c88c649`  
		Last Modified: Fri, 14 Nov 2025 17:53:52 GMT  
		Size: 3.7 MB (3692784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246c35005445d4bbee50c8ecfabf7bfff37a35458ccab55f059ef588e7d1b15`  
		Last Modified: Fri, 14 Nov 2025 17:53:51 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cbf8f8851344a16a8334b41749b8f5de7602e34ddb78157ce3902c37e8a59a`  
		Last Modified: Thu, 20 Nov 2025 20:43:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c247a5593e1221a6d015cb4f96ffae67e1d2dc99228574ed713bc504ad1292b`  
		Last Modified: Thu, 20 Nov 2025 21:15:33 GMT  
		Size: 12.6 MB (12625128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484fcf9bd55b21ece798cfb747a1954931fcddd9f84d8768994b4f622dd43456`  
		Last Modified: Thu, 20 Nov 2025 21:15:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34db945dde5d567b00e2010c5b08fb1e675b8d8834bf195db230168c8fa6ded`  
		Last Modified: Thu, 20 Nov 2025 21:24:42 GMT  
		Size: 17.5 MB (17492485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901cbba11a64a6a7ea8c88064052757c697f1a305a16384b14254751e3d6683b`  
		Last Modified: Thu, 20 Nov 2025 21:24:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ebbcce97061d3b915d14cbb9266097eac2e92f7bc185435067fc1e23c31a05`  
		Last Modified: Thu, 20 Nov 2025 21:24:40 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1291708c9e4fe680df555f810b66695a42197069e5041dcdb3587f086e47b7c9`  
		Last Modified: Thu, 20 Nov 2025 21:24:40 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254d0b8936d6cce4d95a2d513ed9bd593be501211bc54a4dd7a049e2c5bde1c4`  
		Last Modified: Thu, 20 Nov 2025 21:31:34 GMT  
		Size: 12.5 MB (12452450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5997e6bdbf3338d231f02d40a1d6a7d77f1c3f158963e617084477a67579ef8`  
		Last Modified: Thu, 20 Nov 2025 21:31:35 GMT  
		Size: 13.8 MB (13821067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb48a9af40c840ffd1cc30af6f92a012e825892d0bd1600a00861e7dc645537b`  
		Last Modified: Thu, 20 Nov 2025 21:31:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19bad225b29bb529c35edd420c773284fe925af0c527d78458a1ef9b31b0469`  
		Last Modified: Thu, 20 Nov 2025 21:31:33 GMT  
		Size: 1.5 MB (1525177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7dded901772dfd73b13987c125c762adb4723ad29d02746080e7f1e3d57958`  
		Last Modified: Thu, 20 Nov 2025 21:31:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:fa84ee41a993691e4180474f1366851fa1a97e380ce14bc9f19beb738d6f1738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 KB (639172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7982cfa65d571b969ac2e3516ad47de44cdd8fc4d360a06d4fa32e0d44079944`

```dockerfile
```

-	Layers:
	-	`sha256:d8ce1bd681ec68976423a24cbef07ba20ea576b9c76aa4a0df0eac32471720f8`  
		Last Modified: Thu, 20 Nov 2025 23:28:32 GMT  
		Size: 595.9 KB (595912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d417d66271882fdd86ac37dbafc2a18ddd50fdfffc93e42b0ddf2ec0430bc447`  
		Last Modified: Thu, 20 Nov 2025 23:28:33 GMT  
		Size: 43.3 KB (43260 bytes)  
		MIME: application/vnd.in-toto+json
