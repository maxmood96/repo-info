## `wordpress:cli-2-php8.3`

```console
$ docker pull wordpress@sha256:baaef923c5d0ed6cc83deaa3be1132ba4a7e94e2dc035c22eb1b9a1bdf8be194
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

### `wordpress:cli-2-php8.3` - linux; amd64

```console
$ docker pull wordpress@sha256:2ab78dd4e5b3d78c8bbfbbbb242f7c251d64cf3bb7bd09cd8326b8518b92ccd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66914176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8681978613c84a92ccaf28a4bc7eef4e214867e5f1066531e000f2abe1e7ef7`
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92c3fb2543980155e707715c1807f17b105412cd8a2528484c25d7ced76ebd0`  
		Last Modified: Thu, 28 Aug 2025 18:54:12 GMT  
		Size: 5.9 MB (5927529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fc0402d547809980039811ae9b42dfcded62490cdfd22f86eeae02a5401c4f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5118a89a65a7879c4cdee30e47c63bad49e3b3db33a51de3fe326c3d569fc205`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ba7ed8f9e73d58bc5b8771d20971a671da18ddb9efe27282794787a86d8ec`  
		Last Modified: Thu, 28 Aug 2025 18:54:12 GMT  
		Size: 12.6 MB (12604762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4fd03c096a9343dc9b88b4ac373c12505799ffb0b398401d1778a2904e4a2d`  
		Last Modified: Thu, 28 Aug 2025 18:54:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab589c57b5ae59de9920fea8643cf0814256b3c1f426393c6f8edcfb06ce6e7`  
		Last Modified: Thu, 28 Aug 2025 18:54:13 GMT  
		Size: 17.4 MB (17416001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b9828837b2041b08b4a63dc9f647751f04bc69bc2d610ec971252993ff1121`  
		Last Modified: Thu, 28 Aug 2025 18:54:11 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f3083bd498d5827086cee716658307065f174a095e2a3e677fb719c033151`  
		Last Modified: Thu, 28 Aug 2025 18:54:11 GMT  
		Size: 20.0 KB (19960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777f30255e077de73af1d5d54aa1688a77f484c1a165a99ab8b9e7eac71a74ac`  
		Last Modified: Thu, 28 Aug 2025 18:54:11 GMT  
		Size: 20.0 KB (19961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d4f4d2411aa4aaa6a936f8bceafcad6e4ab77ee1cd1a734099e3bb9d048d2a`  
		Last Modified: Thu, 28 Aug 2025 18:55:57 GMT  
		Size: 11.1 MB (11076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea615d4e283a3d7a7975aabd645b029d24a334079a47bc4867acfb29d7ca9d2`  
		Last Modified: Thu, 28 Aug 2025 18:55:58 GMT  
		Size: 14.5 MB (14520022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530418e35a6b69bb6388a5455c1c08fb73fb45d27ba4bb144ef364f8545115f6`  
		Last Modified: Thu, 28 Aug 2025 18:55:57 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcf632459d037e743bb72bf1794aea396f36fa87d704555e9a98058263cdcc1`  
		Last Modified: Thu, 28 Aug 2025 18:55:57 GMT  
		Size: 1.5 MB (1525004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf20dce743798c9401252f9b12ef353418fd2d5f78278b7d630aa281b59185f`  
		Last Modified: Thu, 28 Aug 2025 18:55:57 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:6d650a0fd831d2713d391d211f4eca24e3bf48e0579eed5edcabe12b33bbbc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95af70c407ab05e67ef42a947708dbbe2c0d2f47aab568f7c8d0710fc63ae4`

```dockerfile
```

-	Layers:
	-	`sha256:86de92f014897b6d1f6cff46907f4ef0d7229a9135d7a945161cf9100b46f957`  
		Last Modified: Thu, 28 Aug 2025 22:18:03 GMT  
		Size: 595.3 KB (595274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67190a2c6a42676ae037291d977178d91b8f0089cba6a8a5749ce8c424d0689`  
		Last Modified: Thu, 28 Aug 2025 22:18:04 GMT  
		Size: 42.1 KB (42082 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:cd21fab721000b41cf8cf4986da00f77a6693077bd94b5904bf56da9329c38af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2de2a4a457cdb1b26f1b231adba99f486a0b910c136702cff2f54b2608fc7`
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ffb49c82cf16fea2b2658c93683845111cd140ee61f49d53a82c3343d66eec`  
		Last Modified: Thu, 28 Aug 2025 18:50:06 GMT  
		Size: 12.6 MB (12604744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dede99cf30270dcfe20bbea8569fb35edb90a7f2526cf016a454258c5bd825`  
		Last Modified: Thu, 28 Aug 2025 18:50:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d23ea457d72c55c12788a80b5cb59f8a810f75ac5f26ed35508cb8756bccf82`  
		Last Modified: Thu, 28 Aug 2025 18:50:08 GMT  
		Size: 18.4 MB (18392810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86179e2426b1387a040938c26ff1823e11d30b2eaeb92ff8349b566def5a1fe8`  
		Last Modified: Thu, 28 Aug 2025 18:50:05 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18223b2bc4396a63368497bc671b37cb02fb15a55c2751e2426de3dfd01757a5`  
		Last Modified: Thu, 28 Aug 2025 18:50:05 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b34e7aca9386099434405f800a62423f09625f47c6319349eae871006f15a12`  
		Last Modified: Thu, 28 Aug 2025 18:50:05 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbf9150f286af8f538d172fb930f9de7d20544956fb9a7eefc2d916b445d017`  
		Last Modified: Thu, 28 Aug 2025 19:27:53 GMT  
		Size: 10.8 MB (10775229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e86fb2ca0e47a5ae0ea110b80336a51afad9bc7b885b252605170a9ff98456`  
		Last Modified: Thu, 28 Aug 2025 19:27:53 GMT  
		Size: 11.5 MB (11459937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3fcfd56f6eee9cf73e4d11bbd2d7d324828a5a5f1f5272d00e93828be7016a`  
		Last Modified: Thu, 28 Aug 2025 19:27:52 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062d24b300490023c2addfda0b2173f31afd04b29d00b91419f2bd97d55bf260`  
		Last Modified: Thu, 28 Aug 2025 19:27:51 GMT  
		Size: 1.5 MB (1525004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c536e20a8036aa8462212d20221c6ae1603691d4ded7a7261055a55d5a56fa8b`  
		Last Modified: Thu, 28 Aug 2025 19:27:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:055425bb493564be5ae104b942ae44dca9830f0b929b2b443e756419ad6fc13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (41995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef427ed50e94fcee2bc59f437ee85c11822f17805db65bcbcc1083d4feffeb0`

```dockerfile
```

-	Layers:
	-	`sha256:d0a639b0e3a8cd7a7ca835828e420b8f060674905734b85c3361a9466a460392`  
		Last Modified: Thu, 28 Aug 2025 22:18:07 GMT  
		Size: 42.0 KB (41995 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:6eb844c22d1e072271fee77e869049f0f2e7addff324010ae34cb0b6d3069f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60652431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932529987c01e0ef035ffc44cd3e8f726c3ffc8105950559cf33f21bd96c0c60`
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2918785e629efa03cf38782364004ea1df208a39271bb2a5151ecbdbdb5e9ce8`  
		Last Modified: Thu, 28 Aug 2025 20:03:12 GMT  
		Size: 12.6 MB (12604738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c080e32941e053d3c4d92eca9329f64f69bf58840130e5db6255bd511a32de`  
		Last Modified: Thu, 28 Aug 2025 20:03:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd7d0ec397e11c9218ddb22c5e7e3d09672ac43fa6d2cc8ea5e9f745e48144a`  
		Last Modified: Thu, 28 Aug 2025 20:03:13 GMT  
		Size: 17.3 MB (17273095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913a09802d342c634d4a91397fb8e6cd523086cbf6d923e38de6c8825de9e77`  
		Last Modified: Thu, 28 Aug 2025 20:03:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eaac45be5dc9ecfce010f27c3740833ba399ac77d8835140098d4bec5f8c6`  
		Last Modified: Thu, 28 Aug 2025 20:03:12 GMT  
		Size: 19.7 KB (19727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee262647f0732b703a75d8b0a3bc142c1c40a244a5e5d2dbb2e79c017fe2490`  
		Last Modified: Thu, 28 Aug 2025 20:03:13 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d02c6316c2fa993a268c1be2dd63754341b9f9df2aeed5add5b279c6d18a6f`  
		Last Modified: Thu, 28 Aug 2025 20:40:36 GMT  
		Size: 10.4 MB (10446883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0d364315e818e0cd26dd310c6cad7ac40fcb8d3b8e73662e0c7df9c0420ed8`  
		Last Modified: Thu, 28 Aug 2025 20:40:36 GMT  
		Size: 12.3 MB (12298395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcdf4c3cabd85c72d981c1527235ef8d4e1af6d90880c79470858973d0f2cce`  
		Last Modified: Thu, 28 Aug 2025 20:40:35 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab15211f657ca55e48a2937e89d362efb300c0312fdc2f4f1208479be3a8e1ea`  
		Last Modified: Thu, 28 Aug 2025 20:40:35 GMT  
		Size: 1.5 MB (1524985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b1e8f540030b820e55777308bca43a1ef269c7b77455715f3e0ef627cb1b03`  
		Last Modified: Thu, 28 Aug 2025 20:40:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:826467db5a1b015d2860eef077909767b07bb7be1ddac5b768934d1b5ad958d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4872bf993fba8b2c596b7f34cb6db220cd6db9a3b16ff135e572ef73c8ff8a59`

```dockerfile
```

-	Layers:
	-	`sha256:7972eb7592b80c2598b0b18c2ca734bb101057a97df734800a01cd266a0077b2`  
		Last Modified: Thu, 28 Aug 2025 22:18:11 GMT  
		Size: 594.1 KB (594066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06869ee193d1402ef8ec9814d35ef29301e4967d735275f5592474c3b61c99`  
		Last Modified: Thu, 28 Aug 2025 22:18:12 GMT  
		Size: 42.2 KB (42211 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:1483ef093fec32c724bab1a9c36994b9117d58f20710c386151c46a46c2a79b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67602335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1409ce69a28b6ecc11e19722b52bfd1ad3a434b29148f91fecb0d2017a6bc0b4`
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb46ec3ec285c20759c8abcbd1fba586aee25c6fbedc58e70878ff9bbf9d07`  
		Last Modified: Thu, 14 Aug 2025 22:51:06 GMT  
		Size: 3.5 MB (3454714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e261bfce6cd6273c06f83b374dbb38f92be17c8f1164bc775f5b69489eb88a68`  
		Last Modified: Thu, 14 Aug 2025 22:51:05 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff0d60a0178ee618748f0a5b1b04c9c64b64af3eeca8d0b1566e182adf144e5`  
		Last Modified: Thu, 14 Aug 2025 22:51:05 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf4676eacbdefe39bfac32e05cda23795bc9daee2e796b169fe7f1bb5b999c`  
		Last Modified: Thu, 28 Aug 2025 19:55:42 GMT  
		Size: 12.6 MB (12604750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312dbb78ee6211e9f8bc4c4092f74a8593ed65c1777538e94ca527ec39b4919d`  
		Last Modified: Thu, 28 Aug 2025 19:55:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df17c8b1b593ae14233be43e4901347efba37ff5e303e7d7b6e789f3dd2167a6`  
		Last Modified: Thu, 28 Aug 2025 20:08:53 GMT  
		Size: 20.6 MB (20551970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5470ef80105ee64452d8afc8a7d900d8303a79add6ade2c6fca6ee125253ef75`  
		Last Modified: Thu, 28 Aug 2025 20:08:49 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a0bb9b5857a77c957ef30e4384be80ee60d74b61ad370600faf222e8efb4d`  
		Last Modified: Thu, 28 Aug 2025 20:08:49 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8394d96990e7ab8eb31f0f513087ce8c5363e5a026bfc4f36cbd8bc04eb3f29`  
		Last Modified: Thu, 28 Aug 2025 20:08:49 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5855a9e06f59411f2a411c0d489862200bf0a497bf4d72fa6f10df1c3bde782`  
		Last Modified: Thu, 28 Aug 2025 20:46:43 GMT  
		Size: 11.1 MB (11080178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a7305b3e6a531ffc5f79d2e98facef78f47228a0c1fbe9cc41ce045669e28`  
		Last Modified: Thu, 28 Aug 2025 20:46:42 GMT  
		Size: 14.2 MB (14210533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec548a205bac8efb62e030cb024abcf3d0551798b2e1fc7d9da1f46f2c3aae23`  
		Last Modified: Thu, 28 Aug 2025 20:46:40 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b089d3597a625b3baf0ce047e7babdd7ddc10a14194558beda46ff16b186ca8`  
		Last Modified: Thu, 28 Aug 2025 20:46:43 GMT  
		Size: 1.5 MB (1524987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0864c2c17e5fa5fbf7e0d1e4a21d5bf45dd2e8191f5efbbd7934468066a60e`  
		Last Modified: Thu, 28 Aug 2025 20:46:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:c781cbe8765d575c8fd88e9e4984cfcd5e139d6dde97ba723383c8f89417928a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dfd5d678893b6e91e29925d1165506d68603d05b2b5dd68f17efbfdcf0c182`

```dockerfile
```

-	Layers:
	-	`sha256:60ebe91b1ae1db9c9d28bca8bab84cabe73b785a0e3b9df3819afba66d3f3db6`  
		Last Modified: Thu, 28 Aug 2025 22:18:15 GMT  
		Size: 594.1 KB (594086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6266fc6687bb3dda8dab912af48301058bdcac84ead118a3f3a9d474845d34`  
		Last Modified: Thu, 28 Aug 2025 22:18:16 GMT  
		Size: 42.2 KB (42247 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; 386

```console
$ docker pull wordpress@sha256:4765695ad1b73c57cf74ba55d392f676aeb41156fd008b5ee4cb2cd12b096586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66039839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ab68567c3f811fd5c29beebc0f610247c752f348f76504e1f63be0f285ecfa`
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298255a36e44259ad58dccd9a522c2ac3ce5b048320d2e08a1d19abbd0afe406`  
		Last Modified: Thu, 28 Aug 2025 18:20:08 GMT  
		Size: 5.8 MB (5794093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee8d0601ef0cdcd74644286ae45252cffe7951f757d2c35add3c5215f230b35`  
		Last Modified: Thu, 28 Aug 2025 18:20:08 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d2fff9026b4b3ddec2daa80aaf4b5f50b5f4965a5f7bb9e8889b86fdfba988`  
		Last Modified: Thu, 28 Aug 2025 18:20:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1542577e36a30ec90f812b41dbec9ad1e2d7cf58789705c35f3518495f43c36`  
		Last Modified: Thu, 28 Aug 2025 18:20:09 GMT  
		Size: 12.6 MB (12604749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271b9acb47459b7a6eb77a4c1afb88b77441ddc1ca6af92a689f9187ba680a36`  
		Last Modified: Thu, 28 Aug 2025 18:20:08 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7702bff4cc34c1635a4ea2b8cc02220086c30dcc7836337ba627e7cc8640979e`  
		Last Modified: Thu, 28 Aug 2025 18:20:09 GMT  
		Size: 17.8 MB (17823171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f0cf9bcc95f9450ec308c0712a4b360aad623ac810c623d61e7e6092d30f71`  
		Last Modified: Thu, 28 Aug 2025 18:20:09 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c1b9265fc56c4ccb78ffac6be572d37dddb9c37410fc0b5fd7ce46c9d83ed1`  
		Last Modified: Thu, 28 Aug 2025 18:20:14 GMT  
		Size: 19.9 KB (19934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade6bdecab2ecbac2ea129d2454deda5b5767f17543cec2b5e9a0ddf83e2312`  
		Last Modified: Thu, 28 Aug 2025 18:20:09 GMT  
		Size: 19.9 KB (19926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbff637bad0bf221b58f25e120e8f0f346a92759670772b22f2ae11958bf6`  
		Last Modified: Thu, 28 Aug 2025 18:56:00 GMT  
		Size: 11.3 MB (11274814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8742e078e69cd677fa3c0e57a5e627026c80663bf2488de55220a5d95043555e`  
		Last Modified: Thu, 28 Aug 2025 18:56:00 GMT  
		Size: 13.4 MB (13358241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f435cedaede39736bf377152b8af647e248235dc3008b6b3639aa5038e619e`  
		Last Modified: Thu, 28 Aug 2025 18:55:59 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9471629bb87b0d5021ae4d9932fd0d46543ef095be7f2fd8e328b95aecf32f3c`  
		Last Modified: Thu, 28 Aug 2025 18:55:59 GMT  
		Size: 1.5 MB (1524973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0279ebbf7619f5bbddf9c0e0e3cadad49c05bcc61851d1e389691ba3a4d63b58`  
		Last Modified: Thu, 28 Aug 2025 18:55:59 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:76611d12015a61eb6dab4eef98c72e7e93a3cb1173d8dc2653ad6c4a66d7f32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97d5e2cbbe76c186f7b4e196d08bf1ba858508f93a15bc8254c2d5797d02713`

```dockerfile
```

-	Layers:
	-	`sha256:bf4921203a6b5ef55426047c982643d8e3fc9ffbc2fb1aa5d582accbbe1be20e`  
		Last Modified: Thu, 28 Aug 2025 19:14:17 GMT  
		Size: 595.2 KB (595249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a0c0eae1930fb9f7d9a7912c54c8230a4d31e98a21103c8f3b8b9ca60305b2`  
		Last Modified: Thu, 28 Aug 2025 19:14:18 GMT  
		Size: 42.0 KB (42043 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:7e5b05e305f8530046c58e7ca9a1e8e052c171edbe1e13e489b5591658745824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68398886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf9e974362a6d2a80fbfd393f0276065ff189b6b814ec9972183856dfebc3a7`
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
	-	`sha256:99a10f54e3cf46392e1b1d8a3fdbbd55dab891b479c19b6c11b26198bda8124b`  
		Last Modified: Thu, 28 Aug 2025 19:57:53 GMT  
		Size: 12.6 MB (12604760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a936478d6b913e27fb074f07561c747b02dab3a8fe48e6c6fbf14865eceeb23`  
		Last Modified: Thu, 28 Aug 2025 19:57:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6734013ec1f2fad09cc935c625fdad3d60da73620dc44e723faa8e9280527e27`  
		Last Modified: Thu, 28 Aug 2025 19:57:52 GMT  
		Size: 21.1 MB (21063052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2030155be1d4295bceab7f73e11910c0fc62b52082ecd66a1040ff44e99a4bf`  
		Last Modified: Thu, 28 Aug 2025 19:57:51 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9548981d937499040a4956a94cb34f8fcd3120621cbf27ef79b1897621e8141d`  
		Last Modified: Thu, 28 Aug 2025 19:57:51 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0dba9ced466197bf0ba79ce8f2da0ff94182edd0ef82cf6ee02cd63a460e68`  
		Last Modified: Thu, 28 Aug 2025 19:57:51 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dad622c49610aec3732722d82d0d472a77bef33f441afb816e12b02c78da78a`  
		Last Modified: Thu, 28 Aug 2025 20:53:59 GMT  
		Size: 11.7 MB (11689348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983cfcf00d0411ed246f130672c7289ed4a382ea9322394e297cd9a4f22aed76`  
		Last Modified: Thu, 28 Aug 2025 20:53:59 GMT  
		Size: 14.1 MB (14134009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982654506a6381fc1756505ef0b1e0585cb60cd30affbe4d73c2c4e5c154ac06`  
		Last Modified: Thu, 28 Aug 2025 20:53:58 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1945b824e0c7d76011ad2ea040a0f6237078bb11b23a0cfb340c0ac10e00e`  
		Last Modified: Thu, 28 Aug 2025 20:53:58 GMT  
		Size: 1.5 MB (1525001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16b34b18afadc393c40d1fc219a08404f0fd7570f76df31d6e0b29949727f61`  
		Last Modified: Thu, 28 Aug 2025 20:53:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:228a2c26005cca4681431995eec74593508ad3f53fb4253b607c34bf596626f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06fb98dc88fec9349fb69d66c7683b4c516b9551bbde5de7bdf721b7c509516`

```dockerfile
```

-	Layers:
	-	`sha256:12f98d9eabaadf8a0fa5adb1457135f4a96e306b11abcdf336d38f99d8133a8a`  
		Last Modified: Thu, 28 Aug 2025 22:18:22 GMT  
		Size: 592.1 KB (592113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8edf8feb7e3ce9a82d12837383ca95b277771c0cffe4388b73bb295b7341e2`  
		Last Modified: Thu, 28 Aug 2025 22:18:23 GMT  
		Size: 42.1 KB (42135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; riscv64

```console
$ docker pull wordpress@sha256:92ffdfc88c8f3d582169c5de7806df798c4a5bc0a93425a8db015d0e6a21290d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61604642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60d7c5e82bec9b32adf6df0b646bbd4faf8408ae0f2dfb95f029aaf561eb85f`
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
ENV PHP_VERSION=8.3.24
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
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
	-	`sha256:5a201b0a16aadc2a7c27ca0b373c85630463930fde99bd3c73f103ab676945d2`  
		Last Modified: Tue, 05 Aug 2025 12:57:01 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24220ce5963ab886efe9c3b3f66ba547029509a02a6800ed1f96dd054b509f70`  
		Last Modified: Tue, 05 Aug 2025 12:57:00 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582a82271d94e3cddf595efbe473eda9da52ac6c30aa75156d89d5b789160f92`  
		Last Modified: Tue, 05 Aug 2025 12:57:02 GMT  
		Size: 16.9 MB (16914575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff16cddd36bc4cd63aa736c572c6522b9abd213d700092b78eb3e0ac6329b7`  
		Last Modified: Tue, 05 Aug 2025 12:57:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71870953c7a7b7c700b1fa524e9ea39e05f8c595dca466189fd6780158f58d40`  
		Last Modified: Tue, 05 Aug 2025 12:57:03 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165833eee71fd7cc6746329bde7510f9ea6046c4e63e3b02830929cd2c7c5e6`  
		Last Modified: Tue, 05 Aug 2025 12:57:00 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1450385c247166068ddf5e768476d285d24de320ee337586219f7eb8475d6de2`  
		Last Modified: Wed, 06 Aug 2025 08:26:01 GMT  
		Size: 11.5 MB (11525429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6732e62793608c2b0e43e3dc5a051112c15539c4db39c038a84f3ef9f96c59`  
		Last Modified: Wed, 06 Aug 2025 08:26:01 GMT  
		Size: 11.9 MB (11888337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0718480a94c6d0209c1f80a5cc363b2089bb032d30da95786770e1fa551df80c`  
		Last Modified: Wed, 06 Aug 2025 08:26:00 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db889e487ab80ea34595f5afaaff5c65a8261590c809f4f0918b2859bc251bcb`  
		Last Modified: Wed, 06 Aug 2025 08:26:01 GMT  
		Size: 1.5 MB (1525017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc7268920d6725e7c2c8a6dbdccbb23ca0548888e5a649a52c819f1e4a4b08a`  
		Last Modified: Wed, 06 Aug 2025 08:26:00 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:6540a78211586ec58e1e3ad20a23e3c0a8a31decd0a00b112eaf8e5a4a37985e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff0ad70db3ffea828b3bb8cb75e634c1772096de9a522044f0f458333e7a355`

```dockerfile
```

-	Layers:
	-	`sha256:2e307d7adcaf89e98af8559f47f24d8d757ae773345b678e7fa8323e810bcff6`  
		Last Modified: Wed, 06 Aug 2025 10:14:48 GMT  
		Size: 592.1 KB (592109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17efd9b396dbfaeacf9a229b17fdc7a143db1bf5bebce0cc4a9593b270f1a544`  
		Last Modified: Wed, 06 Aug 2025 10:14:48 GMT  
		Size: 42.1 KB (42135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:772e770a5d53abdab6d066b6e391fa85b8985f78a0cba47d8207c8ab0e014f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65228108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0180afaccfd6521f445ff2d2c080eb15ba869779d08c9b771872fd1f2ce23c`
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
ENV PHP_VERSION=8.3.24
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
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
	-	`sha256:2523afe7bac87b158b525d19c04b257f3c07e08691519ce8330dd437653643c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:17 GMT  
		Size: 12.6 MB (12599878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78df3cd97ddbf126a4a6dfd5bf63960fc6ccf9adfdb9aa202edcc51b19c13c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61007fec367f20a3b1555589ff089c406d108e5ce57f51c6a2d1007e31581fef`  
		Last Modified: Mon, 04 Aug 2025 23:37:17 GMT  
		Size: 17.5 MB (17482830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48536e354301af398810239f1e04b0a9830f16f0c012b52896e5d29120c65048`  
		Last Modified: Mon, 04 Aug 2025 23:37:15 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a3476dd870762700931026d58cc6a8f24005bd0c12a562e35c5e455aac2ef1`  
		Last Modified: Mon, 04 Aug 2025 23:37:15 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d1f9c356831d72a55cc6a924173ac20ad626980231f0d517ec11c63286ea09`  
		Last Modified: Mon, 04 Aug 2025 23:37:16 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfd14578ae19701e02c0332eb4735a1fc480992c75fca4f00f0f5fdd4248299`  
		Last Modified: Tue, 05 Aug 2025 21:26:05 GMT  
		Size: 12.4 MB (12425246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe102e2aababf7523cb34fe2f0d78320b5e80d824d4dcfbda606d55a0a99df4`  
		Last Modified: Tue, 05 Aug 2025 02:44:29 GMT  
		Size: 13.8 MB (13825899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57f1f628e3c0e1ed8d92a4b0cb0b3fe921ab1d41873312c7ce63cf5229a894f`  
		Last Modified: Tue, 05 Aug 2025 02:44:28 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334f2b98b8a6621f11878df80aa0990d127a3f27fc78e076bf928b6d1cd75fb`  
		Last Modified: Tue, 05 Aug 2025 02:44:29 GMT  
		Size: 1.5 MB (1525001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194a905b73c38f080276aa227033b8320c434c66b5b50fcb4dc95b347b5a171`  
		Last Modified: Tue, 05 Aug 2025 02:44:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:79da7720b08d40cc0ffefe5f6c2e6a57521ec0b0cd82f70c00da643037527b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbc1a85ff6422988db3c823a52c8d97797ddf3f7290e60146b77a3173679eaf`

```dockerfile
```

-	Layers:
	-	`sha256:681958ad39ce77065d4598ee788fe8b0f341434ac028d6869c8c88d623f25730`  
		Last Modified: Tue, 05 Aug 2025 04:17:08 GMT  
		Size: 592.1 KB (592079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d40525830dff5b4f308aec5870aa089a82d5d188374ea9be9917fc5efa3123`  
		Last Modified: Tue, 05 Aug 2025 04:17:08 GMT  
		Size: 42.1 KB (42083 bytes)  
		MIME: application/vnd.in-toto+json
