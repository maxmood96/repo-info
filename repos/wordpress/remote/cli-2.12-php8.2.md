## `wordpress:cli-2.12-php8.2`

```console
$ docker pull wordpress@sha256:b01c677935f36f175a743a48296ac361886b3c838f6a9e8b663dcca19a5b9d51
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

### `wordpress:cli-2.12-php8.2` - linux; amd64

```console
$ docker pull wordpress@sha256:f292382b7db8fc9d5e21874358930f69aae23140d5ee2ed37c758e749301718c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67792999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fd9c1e24f61cc67c0d48b9efde4360a859b803e1086184603251e403102266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:06:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:06:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:06:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:06:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:06:13 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:06:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:06:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:09:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:09:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:09:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:09:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:09:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:09:34 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:12:54 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:12:54 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:12:54 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:13:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:13:43 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:13:44 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:13:44 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:13:44 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:13:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:13:44 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:13:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:13:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:13:44 GMT
USER www-data
# Thu, 04 Dec 2025 02:13:44 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da36a36c993e0734f24d7af195ac17611098fbf3e94e5130d1afaf64cb5bbb34`  
		Last Modified: Thu, 04 Dec 2025 01:09:51 GMT  
		Size: 3.6 MB (3591353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b68741955f310d24c98458a05b787a80d873511c3b934c34a9d37a0754c90b`  
		Last Modified: Thu, 04 Dec 2025 01:09:50 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84341e016bdaaf3e17e01fa9989c800ad6a81743171efe9194a4ef8b4cd4272`  
		Last Modified: Thu, 04 Dec 2025 01:09:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9245803571ecc36cb174858e586744bd8b630db2b454652f9cd3fd4e6d5eab`  
		Last Modified: Thu, 04 Dec 2025 01:09:51 GMT  
		Size: 12.2 MB (12186105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b258b693e0703d7f8811dc998368d77a459da26e02df970d0beae5e7c8ec34a4`  
		Last Modified: Thu, 04 Dec 2025 01:09:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862d516067a7291dabe9f8b95ce6c833214ca2808e99a1af2202485244e0f8c`  
		Last Modified: Thu, 04 Dec 2025 01:09:53 GMT  
		Size: 17.2 MB (17199653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5de5452ec8f69a0e881001e7e858564b77210285e70d4792b06564eab2154a4`  
		Last Modified: Thu, 04 Dec 2025 01:09:50 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909df8c75f537ee954ec3b5063717cda3269c6081d6f7f89aed3d1aec83e2fcc`  
		Last Modified: Thu, 04 Dec 2025 01:09:50 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da2a7d34bff46e9848c3b5f5b5214962b6c744b4986e39fc9a84d1b40b7bda`  
		Last Modified: Thu, 04 Dec 2025 01:09:50 GMT  
		Size: 23.5 KB (23508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc05c2c73cd551b00e4b88231680474bd93e15de1ca1b367556e886d942bcfb9`  
		Last Modified: Thu, 04 Dec 2025 02:14:00 GMT  
		Size: 11.2 MB (11154521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95aea2998283ac174d23b53b314a65b29d2d0ecf798ae276762f52bc6eda61`  
		Last Modified: Thu, 04 Dec 2025 02:14:01 GMT  
		Size: 18.2 MB (18214470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2013475ee7b99c8738e042e812caf5a9da18fd8ff81ecc0c3c4ac4837ceacd3f`  
		Last Modified: Thu, 04 Dec 2025 02:13:59 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5f1f2e899a9363e0c32a09d6d64f64429e9c4b172070cd6d0c9ba8f0a347c1`  
		Last Modified: Thu, 04 Dec 2025 02:13:59 GMT  
		Size: 1.5 MB (1535649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf9495b177b8165bd1287bff2cdcbe96fc467672db1c51a509e9e6ec7899fb`  
		Last Modified: Thu, 04 Dec 2025 02:13:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:b45a00df89891b8ea8cbb076e67ee1dfe03764a94e366f24572e8ac8aa7efeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 KB (683146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176c6663624705e69d5cbcb4897f4af602e3ded3b9deb1a2aba4307d685dc475`

```dockerfile
```

-	Layers:
	-	`sha256:03722e9beec372a52271fc38027bd44b47fab417d5c663837a7ab71d26d3bf21`  
		Last Modified: Thu, 04 Dec 2025 05:17:33 GMT  
		Size: 641.0 KB (641045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de194d094037c6f49f9933824fc70704dfce344fca861e5e5e6ba8e3fec6649d`  
		Last Modified: Thu, 04 Dec 2025 05:17:34 GMT  
		Size: 42.1 KB (42101 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:2df5970c41e9a95f6e9fccd5dc3d0d1f773958054ee5b0213babffa1b4cc0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62184740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b7be9fc03b84cf51d322f7ae5444e2f05b792c9376a686c1e11d7068a3e915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:10:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:10:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:10:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:10:08 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:10:08 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:10:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:10:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:12:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:12:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:12:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:12:55 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:16:18 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:16:18 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:16:18 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:17:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:17:29 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:17:31 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:17:31 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:17:31 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:17:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:17:31 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:17:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:17:31 GMT
USER www-data
# Thu, 04 Dec 2025 02:17:31 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525f020ca2e7bd42f765c4f507ff9aa855251093e59692f8d0cf5ab7f159cf49`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 3.5 MB (3547617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3943efd0ebe508e07c6a09a7ae4ad670c7d5abab446e08f9c52887c113ad9c2e`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a71af9c75aca1d8b3a447df1f129a26846956094860a441fa7e7cf28b067444`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f29900e1613c1eab27e1f90988f3ff7c45a929a6fba542af9103a45cf0af7c`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 12.2 MB (12186148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56628740f549b92bc9dc273f266fb2dc3827c6c362df93484b16eec5c0fba7f1`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82291142a6d1d98790c4e8a34ce23c3d61c60346d71a4db473b9bfb7f4486e46`  
		Last Modified: Thu, 04 Dec 2025 01:13:09 GMT  
		Size: 15.6 MB (15609991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f98f4c6e4b0e7dc8f10d588af78765b1a42c61121be0a73dce183afe6476f1`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f2f0a3c07461c4391e1a83948938df2c6cc4a815645dcfb28c5aa778f98d73`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 23.3 KB (23330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8736762cb5cd9dd80c5598495d0ed810521952a867a331fe7d692d7f2c311d9b`  
		Last Modified: Thu, 04 Dec 2025 01:13:08 GMT  
		Size: 23.4 KB (23356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941fe4f0a6ebae3bd14ff7c5d285fd3d2e6065eaa6ac7337a5750944b2fd3d3b`  
		Last Modified: Thu, 04 Dec 2025 02:17:43 GMT  
		Size: 10.9 MB (10882431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0382aab6c1ee248cac4fa774509fd6dbee4b912a1f30716a8198be70947df`  
		Last Modified: Thu, 04 Dec 2025 02:17:43 GMT  
		Size: 14.8 MB (14803361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7da2d58fe00f289e66eb0f5fb8909ff26bef9c958a4b925933e66ca0cd779e5`  
		Last Modified: Thu, 04 Dec 2025 02:17:42 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c36682c990ab8a726bb9ea3f26651b26e08cffe231972031118e0e40c28cd4`  
		Last Modified: Thu, 04 Dec 2025 02:17:42 GMT  
		Size: 1.5 MB (1535677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1e54779ccb0c75d4b7f67388fba9211cd748744afdd3b446f52dc98e3870df`  
		Last Modified: Thu, 04 Dec 2025 02:17:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:663979ec7094939b4bbc2cecd0cac7198241b25c1c1f86b83868ec67c9efefc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547d7b8545598ab1644ed9d6fd97fc6d7cccaf8ba8ae84303630f10001ca6f3c`

```dockerfile
```

-	Layers:
	-	`sha256:99952f2354bb7e745fc2e7cee171afb6718c7c1bd4b349c66cbc0287a7512208`  
		Last Modified: Thu, 04 Dec 2025 05:17:37 GMT  
		Size: 42.0 KB (42018 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:695d4a311a236953867b760091d9ea9fdb4c9065066c04bb79d0f7099f28d03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60877090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a875c009e2c273adb55dfd6c9e9e3159d42828a0f4cac69ac4419a4cf820b031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:13:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:13:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:13:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:13:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:13:34 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:13:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:13:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:16:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:16:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:16:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:16:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:16:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:16:24 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:15:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:15:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:15:15 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:16:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:16:26 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:16:28 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:16:28 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:16:28 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:16:28 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:16:28 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:16:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:16:28 GMT
USER www-data
# Thu, 04 Dec 2025 02:16:28 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18afb0f83694e5fba1a75d805891edf5b5e7fdeae89744124c3dc9a2f3fb5c1`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 3.3 MB (3346506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c8bd1b601f330da1b5b8648bf31c0c42af98bc4acf3b4d4f05d96451c1b83c`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b730ccb52de8940348e86a74212bce4f1e896fb1a47395a08052a2a73f3a7e3`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a1c9817768325816aafdbab3bdbe70d8d7654e34a095268fda16960170b8f5`  
		Last Modified: Thu, 04 Dec 2025 01:16:38 GMT  
		Size: 12.2 MB (12186118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d7935e287fd45509581d02184a03616fce4c203a963730a5c5f73a0bc8735`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed45e664c94f7fc85aa65756e1833f5f89c127b87cbc9b9faf63b5506f1318b`  
		Last Modified: Thu, 04 Dec 2025 01:16:38 GMT  
		Size: 14.7 MB (14678262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abce8ef4989a0a1f205ef3192cb027cc38d825df984559ef9edf9d70c58c0bde`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b5ad3a4e03c612735e71cff07046c3906a764b1d0794f9c87ec6fda08e31a`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d871d51ea29a65a4f3a3b9296061a0d00f797433e65c9a3d1a8edeae0b25212`  
		Last Modified: Thu, 04 Dec 2025 01:16:37 GMT  
		Size: 23.3 KB (23336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b834533222fceee03a0dc31e7e1081fcbc592e677132df094cc3db2f25f59d`  
		Last Modified: Thu, 04 Dec 2025 02:16:48 GMT  
		Size: 10.5 MB (10535814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed93c28874c5030071e68e0668ee35e7828b47dd1e22adbdd83e5b6ade6382`  
		Last Modified: Thu, 04 Dec 2025 02:16:47 GMT  
		Size: 15.3 MB (15264703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd24f03591427a5f77868e44537e81c5584ff7762059fd0ac167055dc0ec5cf`  
		Last Modified: Thu, 04 Dec 2025 02:16:47 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4f8dfe0a7c687ad6fbfbaa179c9e174bbb10f15637671a2eb63f0b2436915a`  
		Last Modified: Thu, 04 Dec 2025 02:16:47 GMT  
		Size: 1.5 MB (1535632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc06a52add6cbeefa8f9efb7d1b193781c221fa3f46ddc574a6bcfbae1a44`  
		Last Modified: Thu, 04 Dec 2025 02:16:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:81448614b9b395c6e1982356e4882b35e0e6eeadd34368732c403650c37d6ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.4 KB (681421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127a8cd7551ce9e7bb275bd84b5a110b2eb02e66ee6bad2e2d518bdb3a63b8c6`

```dockerfile
```

-	Layers:
	-	`sha256:62a2c4278dab0fe821012411ed8ba2b468acc813bae22bb31e50b70ca3d1eb44`  
		Last Modified: Thu, 04 Dec 2025 05:17:41 GMT  
		Size: 639.2 KB (639187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8fc96b396ea9b589498786087da0a563a79a8e7da953a28b4bab7f6b3d9758f`  
		Last Modified: Thu, 04 Dec 2025 05:17:42 GMT  
		Size: 42.2 KB (42234 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:fa7f02a30e789c525f17b3d0f6b84e0f3abb77a5cae9680cf1adaa883e3e6667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66867738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7d5438032a64647eedbab06c9704ddf18c86f1deca64e5076d6997cfb50669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:03:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:03:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:03:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:03:59 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:04:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:04:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:08:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:08:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:08:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:08:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:08:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:08:11 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:11:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:11:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:11:48 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:12:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:12:42 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:12:44 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:12:44 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:12:44 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:12:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:12:44 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:12:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:44 GMT
USER www-data
# Thu, 04 Dec 2025 02:12:44 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f177bc53297712b7195490aec10dd6a2d6a190038859f36c70e3db4f45b60`  
		Last Modified: Thu, 04 Dec 2025 01:08:28 GMT  
		Size: 3.6 MB (3600638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdb29529b954a557dffcc0edeb9bc1b4f40f6f0621bdefdf4d6b45c20406e4`  
		Last Modified: Thu, 04 Dec 2025 01:08:28 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83bcbdcef923cb83e8261d92765d06d2f52511eeac67d0d858b003de4752276`  
		Last Modified: Thu, 04 Dec 2025 01:08:29 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf25963f2bf768693f601536e6e1db27b268496b2d5e1731bc9c781eeaeeb67`  
		Last Modified: Thu, 04 Dec 2025 01:08:30 GMT  
		Size: 12.2 MB (12186119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de3639ad251abe94b415847479d3ea9bb6b39d10be1389b03d708057cee8ae`  
		Last Modified: Thu, 04 Dec 2025 01:08:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71af24255bb145eb180dc24959b98579f8e6dcdb1fb80b7bfd8bfacf10c4047a`  
		Last Modified: Thu, 04 Dec 2025 01:08:32 GMT  
		Size: 17.0 MB (16979501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e8430817ec38818b5d4c854b62c8540eae7db52b964b47cdc37d829d466dfa`  
		Last Modified: Thu, 04 Dec 2025 01:08:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a25cb87975f65ede0a4088cc575776b2fd7c013ffa7d2f8005a8d2fcb7976e7`  
		Last Modified: Thu, 04 Dec 2025 01:08:30 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3829bf1c544853f4149f1b6188bf551d8a210d9cd39b2f1a85b4b9a74a15b3f0`  
		Last Modified: Thu, 04 Dec 2025 01:08:30 GMT  
		Size: 23.3 KB (23345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651ffffd1abbb44b387de439249d20f37ff2fa86377f7f1984241331dab15ad6`  
		Last Modified: Thu, 04 Dec 2025 02:13:03 GMT  
		Size: 11.1 MB (11097831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372dec0d99c336171feb13079855584e780b6cbd193cf23cc08e97f74b18a03`  
		Last Modified: Thu, 04 Dec 2025 02:13:04 GMT  
		Size: 17.2 MB (17221165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4636f3307f9a4f834146bb4b86d97b15ae05a07542638bc0c912ca281cec34`  
		Last Modified: Thu, 04 Dec 2025 02:13:03 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519ab78154dab0940d77795c0879c702f949b4b04e524a9129c7aa65e442b92`  
		Last Modified: Thu, 04 Dec 2025 02:13:03 GMT  
		Size: 1.5 MB (1535674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910ea096fec65484cefaf85277b0e374af01dc8e3f2ab787462e4d41c7fb47b4`  
		Last Modified: Thu, 04 Dec 2025 02:13:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:fce12d138a93e5efd1f9c5678b672f00562b0b9d3f40b996c731e83d2091d02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.5 KB (681473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674e1a26d8f3d0d10c0b9354ac2d3750fb709a81288a60141a950e45638cbeb3`

```dockerfile
```

-	Layers:
	-	`sha256:d39d008c669abdc555e859ccbeb20260a79362d6669132c6dcb4bff0ae1ade10`  
		Last Modified: Thu, 04 Dec 2025 05:17:45 GMT  
		Size: 639.2 KB (639207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e714aaac5ffb13b77dd73c5885ae8ad1abe8d877d9f1bd7a20353c5d21fb53`  
		Last Modified: Thu, 04 Dec 2025 05:17:46 GMT  
		Size: 42.3 KB (42266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:9fe0a9e3fd2f700ad6f66205cc01d9f6c9185a8504b52b13228064d85da6992d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67260721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ca71d4a5e9e779e745651f678ffb639e7086d6bf42f306f1a142f286998f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:05:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:05:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:05:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:05:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:05:41 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:05:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:08:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:08:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:08:26 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:08:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:08:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:08:26 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:12:37 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:12:37 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:12:37 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:13:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:13:29 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:13:31 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:13:31 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:13:31 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:13:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:13:31 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:13:31 GMT
USER www-data
# Thu, 04 Dec 2025 02:13:31 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f210ad3cd1da310a57fb726ea0de49e522afa6efe080a516d67734d589eff5da`  
		Last Modified: Thu, 04 Dec 2025 01:08:45 GMT  
		Size: 3.6 MB (3628342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a06b01144999260337bba913106517a61e094d0b4aced6f7d3ec587bee4f1`  
		Last Modified: Thu, 04 Dec 2025 01:08:44 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65b7cd441fef9dacb86e4117ea43fe5d877a42c3ccf0d5dd8db0363cbdd9e9b`  
		Last Modified: Thu, 04 Dec 2025 01:08:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec640b5fc3b7edd5e857b5e354dddc30a9ac7a73c327658a23c87d69f44c8ccd`  
		Last Modified: Thu, 04 Dec 2025 01:08:45 GMT  
		Size: 12.2 MB (12186115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00df3cb28e8746c2ba53dcebf43721cfa74648d5e54f14c6be33872cfb42358a`  
		Last Modified: Thu, 04 Dec 2025 01:08:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2024380637df4b6264df60e97a4b2596287f49c5808e0de420f961d804acda6`  
		Last Modified: Thu, 04 Dec 2025 01:08:46 GMT  
		Size: 17.6 MB (17560979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca22bbdc85f164946274b8c5daf0e9a565bcd394062d455685eb581f15e8d67`  
		Last Modified: Thu, 04 Dec 2025 01:08:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef439325b1f8e23f9cccd5d69017dd1b6c1a9a52bd1fd474382c19ca6b181ce`  
		Last Modified: Thu, 04 Dec 2025 01:08:45 GMT  
		Size: 23.5 KB (23495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f779d79a6cbeb7320c62eb25d02a0bc28ddcfb479cfd9d3096e1dbcb5a481c`  
		Last Modified: Thu, 04 Dec 2025 01:08:46 GMT  
		Size: 23.5 KB (23515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d05f530f42c8d97f02ab46697163d0cc5384979d26c21c2bd5a662b8dbc87`  
		Last Modified: Thu, 04 Dec 2025 02:13:46 GMT  
		Size: 11.3 MB (11339806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a79711ba5ba619e6fda550d774b9ce53b6c907abce2d65d84ea462886e5e5`  
		Last Modified: Thu, 04 Dec 2025 02:13:50 GMT  
		Size: 17.3 MB (17272060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcc9deb7cb06469a7baada535341d2e3698bb763dcb2d71495d1b1d7b5faa7`  
		Last Modified: Thu, 04 Dec 2025 02:13:45 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcc83724bc4cc5902e316a65c9757af9e9a973a9a0331d9e23ac33d3d03137e`  
		Last Modified: Thu, 04 Dec 2025 02:13:46 GMT  
		Size: 1.5 MB (1535609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3911f5eb9ff6efa57ed45b80180c041e06df3be131e0922778b07de403dc20b`  
		Last Modified: Thu, 04 Dec 2025 02:13:46 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:92e7c6b164d837cd02016213cccb32f7bae0dd7ab810071663196fa640ee99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 KB (683082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbd834bec09205ae0c550e94dfde618ead3a844588965ff7ae3ae88ec9f4191`

```dockerfile
```

-	Layers:
	-	`sha256:36ec7778fdedc22b02518564c40b4c8134158f881148b9134d76a89f25709a2e`  
		Last Modified: Thu, 04 Dec 2025 05:17:49 GMT  
		Size: 641.0 KB (641020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79992637199efe3c58cbed2ab68eff5304154d018efb10a1e1e1a65b95146793`  
		Last Modified: Thu, 04 Dec 2025 05:17:50 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d076e39947af174b7961c39a9fee10da1e4651ed8e0e8b28d9050321f74bab0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69434369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a132b5bbf0b7c92cc742bfb41ef7d8cde9801e37aba3fec38d4da0687b465b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:39 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:27:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:27:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:31:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:31:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:31:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:31:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:31:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:31:07 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:16:09 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:16:09 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:16:10 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:17:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:17:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:17:51 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:17:51 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:17:51 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:17:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:17:51 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:17:52 GMT
USER www-data
# Thu, 04 Dec 2025 02:17:52 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a7d1a3b5b7008c71c24d3d5a87883f4c3804bbe6f605d645eca31542c453c`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 3.8 MB (3768890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4195a5efebe02f479fe9c6976a2651e23f862d3990e7d601648b7bd1f929850`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79239a134bbad0459d3e57c5cc7de1311cda2607ee4f1b08432fc54de839a4e5`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6d90b63dbc38f7bc029fc14d7f2d8ddff61ae3f79897d58a6f97571fa3f623`  
		Last Modified: Thu, 04 Dec 2025 01:31:30 GMT  
		Size: 12.2 MB (12186115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111e4ad6378d645b0c1a81efdf42ea50cdbb3b91d16223e8b0d4bb19c00f88a`  
		Last Modified: Thu, 04 Dec 2025 01:31:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea64e61e16b0b40b16ef61409e041288642fa5b1952980418823c00bbbdb5d5`  
		Last Modified: Thu, 04 Dec 2025 01:31:30 GMT  
		Size: 18.1 MB (18147874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da68f8f9836e24ee8e30708c2bd9cd342469c0f57a3aea5e3537f3b96c5be36`  
		Last Modified: Thu, 04 Dec 2025 01:31:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e90d68bbad5566c70c29fa012c7a67072bcbd6235cf056a4c325c6c440c5e0`  
		Last Modified: Thu, 04 Dec 2025 01:31:30 GMT  
		Size: 23.3 KB (23342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890efb7c1aaffbb4b8a797f0f93af962f6a73e21c31fbef29c4574949ff95c95`  
		Last Modified: Thu, 04 Dec 2025 01:31:30 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9d306fea624e441c09496cb570db7cda903514980012e217f31e2a32c6f3c0`  
		Last Modified: Thu, 04 Dec 2025 02:18:18 GMT  
		Size: 11.8 MB (11817767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660d4214ac73c934396f443f8be41eb5db2c7db196d6cf3777c250b9fe925e70`  
		Last Modified: Thu, 04 Dec 2025 02:18:18 GMT  
		Size: 18.1 MB (18099373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731716536a96eb738fac2f2bb9f84037726b419587680572d20234400c8fc7ab`  
		Last Modified: Thu, 04 Dec 2025 02:18:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca4e85eb60f3ad0b0f76f6090235f9424cd3cbcab83a9149de6a65d29aa0f5e`  
		Last Modified: Thu, 04 Dec 2025 02:18:17 GMT  
		Size: 1.5 MB (1535678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a94dcea6338316d9b471b0b6c538283b323c9ac9a666ef57409dfea235b5d`  
		Last Modified: Thu, 04 Dec 2025 02:18:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:30bae7187481cc05e25c10701681222cebc1197701c6ba6811a3d5629ca16d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 KB (681338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac1c99e109d6f90e3c178c2952b23727b96992b9e227f95fb7c56cc5184007a`

```dockerfile
```

-	Layers:
	-	`sha256:9283b3bdcc131e3bd6326a05a372b6efc4fc8a39f866653288551b0498443428`  
		Last Modified: Thu, 04 Dec 2025 05:17:53 GMT  
		Size: 639.2 KB (639184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0550828f7bfc1ac946abaa443c2acf56c4bdbc5779633031c272267a7c38c701`  
		Last Modified: Thu, 04 Dec 2025 05:17:53 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; riscv64

```console
$ docker pull wordpress@sha256:97af6dc68be2ddcdc232dadf422e7776ac22066ad25d343f50a04edf369a56dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64406120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a59aedfcbf949e78edb4d3de16dda90472dbd21b77a662d43f0a74cac7d006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 04:20:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 04:20:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 04:20:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 04:20:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 04:20:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 04:20:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 12:48:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 12:48:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 13:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 13:35:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 13:35:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 13:35:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 13:35:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 13:35:45 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 16:49:51 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 16:49:51 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 16:49:51 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 17:03:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 17:03:05 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 17:03:16 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 17:03:16 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 17:03:16 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 17:03:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 17:03:16 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 17:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 17:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 17:03:16 GMT
USER www-data
# Thu, 04 Dec 2025 17:03:16 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2559d37315299ac2974df718491e68e75407bd4024398180bf2e31452dba7291`  
		Last Modified: Thu, 04 Dec 2025 05:22:56 GMT  
		Size: 3.7 MB (3739982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3bd8574cb0921dcd93805f3fca6feedf60a33fb9c08e52f2eb9827989b0a`  
		Last Modified: Thu, 04 Dec 2025 05:22:55 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8090aa9a6be2d187aa1322d22eee1829c9afdeb8a4c68df173418fa6face7`  
		Last Modified: Thu, 04 Dec 2025 05:22:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515f92554d1cee6eac68fe1b42c81747cbc75ef8632a2da4e2a946176c1f6706`  
		Last Modified: Thu, 04 Dec 2025 13:37:08 GMT  
		Size: 12.2 MB (12186111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfa028c954f6140cea6d932d9fe1a50407adcf67fe8103852211f4bb1a9f6c2`  
		Last Modified: Thu, 04 Dec 2025 13:37:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d0ff5197981c89ad91877919cd8306090f79a2f8023c68d43e729d4e5ca3d0`  
		Last Modified: Thu, 04 Dec 2025 13:37:01 GMT  
		Size: 16.3 MB (16269104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57bdd169d0917a4d7068dd080e3649f90c1d7ef20e1943e606f32031fb72150`  
		Last Modified: Thu, 04 Dec 2025 13:36:59 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a106cac179a9f1987bd39b5d2e07aa0f90892a8ddd994ed5ac6e470b81970a3f`  
		Last Modified: Thu, 04 Dec 2025 13:36:59 GMT  
		Size: 23.3 KB (23304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353ff0803f0cf02b99aa47ceb2cbf3b5ebb86c991bf76d8346dbe9334309daf6`  
		Last Modified: Thu, 04 Dec 2025 13:37:00 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b3a4badbfc449526833a78190ee251313f873b5c556c280eeb7fcddce1abc1`  
		Last Modified: Thu, 04 Dec 2025 17:04:53 GMT  
		Size: 11.6 MB (11599309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c5436d72d0642c24c9aa3123b9a729f7779ddeaddd6a1e8f830bd742a9412`  
		Last Modified: Thu, 04 Dec 2025 17:04:53 GMT  
		Size: 15.4 MB (15440868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df64366dfb3833f42f0a6177938eef870b5ea3a34e12441389fc4edd2c071db`  
		Last Modified: Thu, 04 Dec 2025 17:04:52 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e7a387012ec91abb3b82fa5d997ff9e6db4ca44837f01fdaee5eb3304fcfe9`  
		Last Modified: Thu, 04 Dec 2025 17:04:52 GMT  
		Size: 1.5 MB (1535645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3432cb51c9158a92cd70f46ee53e5d4700cb5f1ee83e4f611f71eb0b0f2d8c`  
		Last Modified: Thu, 04 Dec 2025 17:04:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:f468cca43f58f40591567141cab577e406391196012117d90d77b6de24a5dc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 KB (681334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725cf8be80e676d4d852d9d786a6048b3a6e9d3de22b4c93a6668f30ab1f91d9`

```dockerfile
```

-	Layers:
	-	`sha256:7d2f121249e8dad794bfe38ae0774b0a0f853af79844d8cfb15ccc8709cff469`  
		Last Modified: Thu, 04 Dec 2025 17:14:39 GMT  
		Size: 639.2 KB (639180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baebb2962373b642a673597920bf9d87a53960762a809ca2c700660d6acc685c`  
		Last Modified: Thu, 04 Dec 2025 17:14:40 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:9bb211992fb9dfcfa053677fe4a6319469a4de75915f6f33091936d09faad221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68456295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486777c83da47079d91e51e815ac22faa3333edfcf512f68bf00bac9ab27dc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:03:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:03:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:03:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:03:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:03:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:03:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_VERSION=8.2.29
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 04 Dec 2025 01:20:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:20:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:25:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:25:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:26:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:26:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:26:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:26:02 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 02:14:40 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 04 Dec 2025 02:14:40 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 04 Dec 2025 02:14:40 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 02:16:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 04 Dec 2025 02:16:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 04 Dec 2025 02:16:14 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Dec 2025 02:16:14 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 04 Dec 2025 02:16:14 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 04 Dec 2025 02:16:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 04 Dec 2025 02:16:14 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 02:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 02:16:15 GMT
USER www-data
# Thu, 04 Dec 2025 02:16:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57875495d370cfefa264d828344954d60baa21cfed9c624ccc8c3f7017d281f`  
		Last Modified: Thu, 04 Dec 2025 01:11:43 GMT  
		Size: 3.8 MB (3793991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a484672f7cc3379a76694729bfaa2a2fc1eed11bf2448fd84a78a6c0e5cbf8`  
		Last Modified: Thu, 04 Dec 2025 01:11:42 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e20e4686724e9dce787d50b8e7300dbca70dabe54a633b4e671c04ac36e27`  
		Last Modified: Thu, 04 Dec 2025 01:11:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b3fba410a8a25be7e6cff8d794126bf78e3703aa183c95c9bc2ab9764b486`  
		Last Modified: Thu, 04 Dec 2025 01:26:29 GMT  
		Size: 12.2 MB (12186122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6c872267cb2ebf48248bbb67f976ce5512001eaee86434f5671d773e99eb0`  
		Last Modified: Thu, 04 Dec 2025 01:26:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acce7945fb632cc0ab10d75c7f38391d42e54d8ec29e91bb61d7430dcf789bb`  
		Last Modified: Thu, 04 Dec 2025 01:26:37 GMT  
		Size: 17.2 MB (17162982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8263583c8d6b7235f697b351058c1ec4527eba3f3b6c5608562f4197d36ed2`  
		Last Modified: Thu, 04 Dec 2025 01:26:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ce17cf983e1e7530757aed3ee09c6eea64781565e72ef16a40ca47bd3f3ee`  
		Last Modified: Thu, 04 Dec 2025 01:26:29 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403fdffb00d8da595777654f9956a4859fa3544c5d2322cf87d8d2981e27c67`  
		Last Modified: Thu, 04 Dec 2025 01:26:29 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9b3faedf70122c10aaaf060185588b0de9d00def1feeb3ebb3363249cb66a`  
		Last Modified: Thu, 04 Dec 2025 02:16:52 GMT  
		Size: 12.5 MB (12526681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cdd557346a470a0531b728a132f8e21e6e1978ac1bef2aa250c58cf6df9807`  
		Last Modified: Thu, 04 Dec 2025 02:16:51 GMT  
		Size: 17.5 MB (17475392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8cfdd86501c0154d0fa6abe7a619a7f7da88c99b6c37ccdab6e05423ce9912`  
		Last Modified: Thu, 04 Dec 2025 02:16:50 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47de3df6dd809e8c3b2409a92a2c8d94d4f272750a32d5be44881e6e27eac8`  
		Last Modified: Thu, 04 Dec 2025 02:16:50 GMT  
		Size: 1.5 MB (1535689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2120b9b15b32f96782ed217820a6f283423cb68f3940da32d6eddd9d45a9d91`  
		Last Modified: Thu, 04 Dec 2025 02:16:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:429854f21350d36f412228279154ef3b89e87622a148244ce3a7450e19edc8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 KB (681252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801d8f5dda1d32fedcb72331f325e21f23632cda56730f71e43b765c1b2aec4a`

```dockerfile
```

-	Layers:
	-	`sha256:1eef7c8cfeba1b93ad83ccabb2294d8cae56dd65c082c73af4f8cdc7249617a7`  
		Last Modified: Thu, 04 Dec 2025 05:17:59 GMT  
		Size: 639.1 KB (639150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a800311d0d20f56ed81a36e43580ff580c9ab84e81b15ac390de72f3cdb15753`  
		Last Modified: Thu, 04 Dec 2025 05:18:00 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json
