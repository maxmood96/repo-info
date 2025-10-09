## `wordpress:cli-php8.2`

```console
$ docker pull wordpress@sha256:cf5c60aad396c80a58079c7a4e58546cfb579ca0adce8eda06c72cf069197b18
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

### `wordpress:cli-php8.2` - linux; amd64

```console
$ docker pull wordpress@sha256:b30dd8760e6c2a5efbb8665f456a0364c4cba41f057219a1d07e72384d2b7f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63683380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5089afc846e0e65d04a344018b1af9001d20f4221be289f7018b426f3f4296c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd87ee7422fd8786636293ad6c7afbcdd8fc12cdcfc3e84ea334275837ef30c`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 3.5 MB (3463765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af09a93268c7c338b7b09afbd144f6415904d5081863ccd39531ab5fb5cd0b`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cc3bcb1fd27dd98919a460aacc83abc0dc58acc0fa85ee5a782c5454b92986`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c36587f704405b8b25b00f745641217d934f9ace347de9fc01a7205202efa4e`  
		Last Modified: Wed, 08 Oct 2025 22:51:31 GMT  
		Size: 12.2 MB (12183660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb63ab588d619504f789d3829f8052d78808d07b94a47450336980c42ceaa6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350c32eb74b1fa150d00de84bb9a143ad8c208c8108e854727160a0c9d4cee21`  
		Last Modified: Wed, 08 Oct 2025 22:51:31 GMT  
		Size: 17.1 MB (17069655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc16179a3ebbc670adb53e245057d89cd8c91a61be03e47cbe091941fda9a48`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b53dc3e10aa0de8d3fdb17a6a5d3eabbd26fe43c1055983cd96745296cad99c`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 20.1 KB (20078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1cfcb9001bd8f1d8bf9f0981ea22b6dae65739dc873ee5e33c9c2149777025`  
		Last Modified: Wed, 08 Oct 2025 22:51:30 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc1ebb2a2e9c413cd26052b131f85a18120d7d53e14226c20aa5aafc1e756d5`  
		Last Modified: Thu, 09 Oct 2025 01:20:02 GMT  
		Size: 11.1 MB (11076262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33190632264589094fc752f2c11a0da78ce803c470b2ca09c6d6e55f123f3b0e`  
		Last Modified: Thu, 09 Oct 2025 01:20:06 GMT  
		Size: 14.5 MB (14517355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df64a706b86da53e67b8f9ffe9bf81886f19b6e1e6ca39835590fd35161a351d`  
		Last Modified: Thu, 09 Oct 2025 00:18:01 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2a31e97c26179fbbfec4619dc5a51fa004b6f00a9dec4f29a09a366f6659da`  
		Last Modified: Thu, 09 Oct 2025 00:18:01 GMT  
		Size: 1.5 MB (1525144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ab86b5594c6c5cd29ea26ae7e3a6e669fdd76cd93373293449737db2ed542`  
		Last Modified: Thu, 09 Oct 2025 00:18:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:02dc66f1783434ce7e1254cbd5e63b825b5c67f39414e3b41463faaff251f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eccf999e82a72b52e2f0a660679cebfb1da7aeea04854f14eb45aaec6d85095`

```dockerfile
```

-	Layers:
	-	`sha256:ed8378de8daea755ecd0508411d48ff40bed33af55408b4941f812adc2a3c0b3`  
		Last Modified: Thu, 09 Oct 2025 01:17:08 GMT  
		Size: 597.9 KB (597887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9c61780b6a74a87aeba7cf11381d93223611539510f56ef324df5ceabf4535`  
		Last Modified: Thu, 09 Oct 2025 01:17:09 GMT  
		Size: 42.1 KB (42083 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:3cc72c5a2159b7fb26c020f67de7e7eba6170b13b6aad399b5506ed48d37cc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58381239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214738cb29dbaf807c19b47ac00bd8325b282253f9b02e4006a6df3ea55d52f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cdcb39afd821d13b22ca21c865ff19e58569c683f9e18b9a0ceb95c92b680`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 3.4 MB (3428334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8740db6975c9b8c5220191ade53612421b7da5301d9f3f7da94286205eb5ec`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc4035a2fd0c27d5270cc96e2d8cfb3e6e50f6a5677241510df3134795ece31`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545381da6803f1b3638c53d36ad0a89ff6618a484992f75c01dd32a8a04b6fd`  
		Last Modified: Wed, 08 Oct 2025 22:59:02 GMT  
		Size: 12.2 MB (12183664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cca4aaa0398d566c8e610ace860a8bcbea5533584aa869ccf79913280bd1a2`  
		Last Modified: Wed, 08 Oct 2025 22:45:01 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d041d0172d80de11af8cdc8c32664a6d35fe7394cce7bf09360c09646d6917c`  
		Last Modified: Wed, 08 Oct 2025 22:59:01 GMT  
		Size: 15.5 MB (15463832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913fcc46e5075d05104ee3d77456c57af217e07bbe6fb88e65b0c1a77ea39480`  
		Last Modified: Wed, 08 Oct 2025 22:45:02 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7acc68801cd97d825fff7048bd568a246e1f14171d99ebd481c4aa217b3cb6`  
		Last Modified: Wed, 08 Oct 2025 22:45:04 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848cb478d47d7342e35704e1bd5a7eeb6a721ad33e8a1077a1000543737bdfa`  
		Last Modified: Wed, 08 Oct 2025 22:45:02 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd75030d8e6d8b01fb8191f9ae32fb28227c97057276d6facb3df7759d801b`  
		Last Modified: Wed, 08 Oct 2025 23:00:37 GMT  
		Size: 10.8 MB (10775986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9a797a439a921d7d17136e0342dbabfbafc7560fc929bc68174dc4e32f6d1b`  
		Last Modified: Wed, 08 Oct 2025 23:00:30 GMT  
		Size: 11.5 MB (11455525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38ae65f1259e7c59aa2d7a9a1d453157c04e14f35c01a14af16d8887d49ec56`  
		Last Modified: Wed, 08 Oct 2025 23:00:28 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf97c051baff73bb137d1d06e93dbded001d0c6d171cc09f81b5fff5f828c88`  
		Last Modified: Wed, 08 Oct 2025 23:00:28 GMT  
		Size: 1.5 MB (1525148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6cabbe71d9a8ea841b21160dc60f74380ac8b5e9ecf1b77a9f7422d1aa332`  
		Last Modified: Wed, 08 Oct 2025 23:00:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:b688de8541f350b4b9d041fbd2abb3f53b1d2ced8f5e190360b08adaa470e1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17924ddaa4f67fea4dfcd68762078afed375494b193387b44e8b6d67672819a`

```dockerfile
```

-	Layers:
	-	`sha256:9bc10c91bef979c180516a9ed75f6c4e31f141ed00487e9cfd66e783b6ea9201`  
		Last Modified: Thu, 09 Oct 2025 01:17:12 GMT  
		Size: 42.0 KB (42000 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:62b5550c517ca9c1cf6b200cb85f96718e6088282e78221cefd848fb756e4f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57500955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee97fb1c5e86bdfd9c7bbed1b1d510ecd24c4e5c6f4a9097b25dc8517d8d391`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd31953efba831f10d0cb18b5b3ad75edf03f314e7bbe38c1aca633e797fb`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 3.2 MB (3244402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b71c74c2ecafb3a798b10fd0c6397ad7786a6849c4856db6dd514a2c975c4`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c7f53a180a3a248d39673c498c7ab85a1a6d5183694c33d3038f736b071339`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01a92fb1547ed96ec01d1372016408e66bd364200cf97a2acd77561657cb93`  
		Last Modified: Wed, 08 Oct 2025 23:16:17 GMT  
		Size: 12.2 MB (12183655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1487154c0185b502c57939f11f6c55e90cdae1f3c54a0b52c3e1ecddb38594c1`  
		Last Modified: Wed, 08 Oct 2025 22:44:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940b80fe502bfeb3914258d5ee1c19183aab7c75ee591f7ef9a23b280009c66f`  
		Last Modified: Wed, 08 Oct 2025 23:16:19 GMT  
		Size: 14.5 MB (14537863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5083aa8963a692dacdd48b491715ede1c8d3e925cc0633965eec3524d410bee3`  
		Last Modified: Wed, 08 Oct 2025 22:44:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec3555351e63454dc14258318125789058a9047b3869e62c65f906475819c9`  
		Last Modified: Wed, 08 Oct 2025 22:44:11 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386e89bc7c6d8a57fc802b3496643079ce0cb779bafa0a3836ec5bd26e8afefb`  
		Last Modified: Wed, 08 Oct 2025 22:44:11 GMT  
		Size: 19.9 KB (19850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c0e26c0640de0f29744f23da03a43c125effc405e54d555c070ae7e115e34e`  
		Last Modified: Thu, 09 Oct 2025 01:12:29 GMT  
		Size: 10.4 MB (10447495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48489854c04b15144de130a93bb5ba86936837382c69c5846af815d62616da70`  
		Last Modified: Wed, 08 Oct 2025 23:17:42 GMT  
		Size: 12.3 MB (12296232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada17caa8c1a2ba8756b3572dadc9451ce022fe1fc5d2f14bccf5072fff8aff5`  
		Last Modified: Wed, 08 Oct 2025 23:48:39 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d7917b8812fbe3ca9829fed2681774a4c3eb12dbac803e3f4c16cafe2597f`  
		Last Modified: Wed, 08 Oct 2025 23:48:42 GMT  
		Size: 1.5 MB (1525104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c64ee41d635daaac3c28c879fdf510d086d33c6e222329edda2607ce13e42c`  
		Last Modified: Wed, 08 Oct 2025 23:48:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:598d8723fed5673a54b27e552aa4b339dcc088b257385b3947e6d3f38b2b1d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6676ca59d2588248da28a3101e33d3ce820be0c9078647b6817daadc242390`

```dockerfile
```

-	Layers:
	-	`sha256:117a9f9c0e41dbc1d5a8079b5fea59893110710b84a43ea51fea0de45b344810`  
		Last Modified: Thu, 09 Oct 2025 01:17:15 GMT  
		Size: 596.7 KB (596679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe3e2d2ccef1e8811c383efc7ea76eae5b47ed9dc5c134064724a88b49a4c3e`  
		Last Modified: Thu, 09 Oct 2025 01:17:16 GMT  
		Size: 42.2 KB (42215 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:166821b9745bfb67f59435ab1ee61672efc355a9d75025b3823159bc0b110cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63635349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1341f3e0567bf7293327cb41ef3ff5e5a8957ed099428e3b92c173fc4ab20af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5066d663b049004cd60b5deee99c55169457cb1768816d31310e9c8b190b5d`  
		Last Modified: Wed, 08 Oct 2025 21:18:05 GMT  
		Size: 3.5 MB (3466799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0e221940ad05f928b39599298d2a8e1169030e4c72a7bde38ee513c00c093`  
		Last Modified: Wed, 08 Oct 2025 21:18:05 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c43c4292b27c1aef96ff776c85d8b97b541f4075698c90d7101380e37f110ba`  
		Last Modified: Wed, 08 Oct 2025 21:18:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b634fac46e4afe873922469b820e1c15ab36c9c6b035f6712b017831a86a7c`  
		Last Modified: Wed, 08 Oct 2025 21:18:07 GMT  
		Size: 12.2 MB (12183658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2ba93bbf0aea33c2ed3177bb5145818adf53d6a051a4b4b1a910fc6020d577`  
		Last Modified: Wed, 08 Oct 2025 21:18:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b13644612f5d2aee26af7cce785cba5d03020c8421ea19ca5c386c966c0a3b`  
		Last Modified: Wed, 08 Oct 2025 21:18:07 GMT  
		Size: 17.0 MB (16989083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdbb0aac437dc127cd86001c005403fd17a98b7a83cfd72cf164c9cb825042`  
		Last Modified: Wed, 08 Oct 2025 21:18:06 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f796592c957ad56b7076ab808a92e3f96a4a79a8e1cf407a371a30d39b301fdb`  
		Last Modified: Wed, 08 Oct 2025 21:18:06 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de8b6eb9410a993710d960a2933bbb426c1be5cf07cd0aed3b6178b002d1b1e`  
		Last Modified: Wed, 08 Oct 2025 21:18:06 GMT  
		Size: 19.9 KB (19859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2df83970accfa57629fa1da4babaaedae788eb511428f67e0b958825695cf`  
		Last Modified: Thu, 09 Oct 2025 01:54:14 GMT  
		Size: 11.1 MB (11080263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac90852b47ad54b2c9f01ae63672ffa21dcabb05b823abaef9fa531e3f00315`  
		Last Modified: Thu, 09 Oct 2025 01:54:17 GMT  
		Size: 14.2 MB (14207680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3e45645a5b08b91c0b9ebc3cbc3b257f07dca74626a7a8f91dd40ea0ee4beb`  
		Last Modified: Wed, 08 Oct 2025 23:42:57 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3841869d67c69ad97702adfecd4799fc5da1c51523d352a6ad8566d81f2b669`  
		Last Modified: Wed, 08 Oct 2025 23:42:58 GMT  
		Size: 1.5 MB (1525131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3b64d66264faf653cac801dfe83bc5714b10dbaa899018f3a4d580030956`  
		Last Modified: Wed, 08 Oct 2025 23:42:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:74fe3d3af8812d68140a6009dc48b291e5b9491a1443915abed2db6bc34fd115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48af87e5d39a5af1098c960ea841c9e4ac589e14c7536d60d95378d0eac7b75d`

```dockerfile
```

-	Layers:
	-	`sha256:a9c0886d2ba2bbd13fd97fd02a64b72ccfca6b06a584103b6e2b90494911a084`  
		Last Modified: Thu, 09 Oct 2025 01:17:19 GMT  
		Size: 596.7 KB (596699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3db77be84324c344e68e43423d8d6929f22adeee83783fc7afb18c41c39f89`  
		Last Modified: Thu, 09 Oct 2025 01:17:20 GMT  
		Size: 42.2 KB (42247 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:b4cccdf4a6869771bab8e8e35c31e6268586e5e4a7abfd96e63452d7eb7b5fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63032272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0327c28b3c3369619cc16b48eadd9a1edbb27b1eda50af83bedfbc7f96408ed9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b22d6444372b06aa0fc5d9bc19203c95cb87f6b121d67cd216dc1117971273`  
		Last Modified: Wed, 08 Oct 2025 21:33:30 GMT  
		Size: 3.5 MB (3522959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b38bdd85ec03b4481f8213882ad2f7f7b8327f54eed97b3e2b82b8d14222e5`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f92f1d1f3d2ebc8f7369aab0c85606be8c03aa301dadedc3e1ac62562553`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a5ac6600cb28078e313d4158a3c0f0b0ce26981e7c39fead3ba18f6917779`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 12.2 MB (12183642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5fb30144382ce345b9447775d82d399a60f798d07fc1d0a86a7e769408895`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda19d0fc3b7f57aa2fd262d57f2baded380557f962b7f057efa4882b58e00a5`  
		Last Modified: Wed, 08 Oct 2025 21:33:30 GMT  
		Size: 17.5 MB (17506779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908d658b2f2c21a118dd0c18475f236420e58aedfce4b087f2bf67fdd352d48`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae67c7a0504511ef4b3f3c5ce6b67365b2b10086ee59f5c7dc980bd58f90110`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 20.1 KB (20054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a174efe8c73bbdcf0bd248b0226a1d55840e0e58becd7c64852089680a8663b`  
		Last Modified: Wed, 08 Oct 2025 21:33:29 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcda70c13586b1cdcf44629411184d0fe8dbee374a830b2da9de827d84977ab7`  
		Last Modified: Thu, 09 Oct 2025 03:47:17 GMT  
		Size: 11.3 MB (11274939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7340b616e956adf71fcf83b9fc4c3c516cd3cc55f343c691e5e5300f37c5134c`  
		Last Modified: Thu, 09 Oct 2025 03:55:57 GMT  
		Size: 13.4 MB (13354837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69640507d6905692994dc0c266fdd9364a08ffb068ad178699fbaa25327dd2fa`  
		Last Modified: Wed, 08 Oct 2025 23:13:15 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef91e424a23dc9616eb63595159188c6cd6a827cb5b4d1aa779785cca4c10567`  
		Last Modified: Wed, 08 Oct 2025 23:13:15 GMT  
		Size: 1.5 MB (1525134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cab47de9a7c38d7b67ae6fb1b5c4dbde99abecb0c2114f877c4efed5bcf475`  
		Last Modified: Wed, 08 Oct 2025 23:13:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:7ca4f1a0a77fc512f1a13c36d529f244f016c2317be4e1f6907fc4b49a68279d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3259bbb68232155f2249a389dec16d496e69847df5bffb301429169cb3bf92`

```dockerfile
```

-	Layers:
	-	`sha256:26d77b591289cb08fd9e423eb7ab1fc5c17266abe75d61d5bc5e96aa70af71fb`  
		Last Modified: Thu, 09 Oct 2025 01:17:23 GMT  
		Size: 597.9 KB (597862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b7184f4bd42ff5638b9e6fdd136efefba9ca432142c1464eca0f7f20f2a091`  
		Last Modified: Thu, 09 Oct 2025 01:17:24 GMT  
		Size: 42.0 KB (42043 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:5cf950dcc2fa7c195e526949bf4abd4d7cd98c1e205f66da1ebf7a4ed6a0aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64809608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1561e43a468dad28bc428f5378cbfc52a4adaac11b9667bef91a1f2f7cfd0fd`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:7900e6388edd03604b708395a43dcb5575064c5775ac1816102ddd605f13549b`  
		Last Modified: Tue, 05 Aug 2025 02:01:19 GMT  
		Size: 12.2 MB (12183566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b2efef804b3c74011adf0c8258a0943f2871010fb57c95989450df53826fd`  
		Last Modified: Tue, 05 Aug 2025 02:01:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fa34179ff5a124000c939f37330b7d8c0983b82716ea5105e8ba66c9aad12a`  
		Last Modified: Tue, 05 Aug 2025 02:01:21 GMT  
		Size: 17.9 MB (17911467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6b18e655b63df288f6f5661892cec1564526b034e33ef7cf46a0543706b51`  
		Last Modified: Tue, 05 Aug 2025 02:01:18 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c595ee3f3c1c5ed1889a045eebf670f4d54ad483e3255d0728f4481f8eb446`  
		Last Modified: Tue, 05 Aug 2025 02:01:18 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb34fc1c6db31a2b302d60c1b091ae570d6933f9e31f2ef24d4b2db023a74f8`  
		Last Modified: Tue, 05 Aug 2025 02:01:19 GMT  
		Size: 19.7 KB (19732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1a6281c46b45548b18ccc40bed828d0c928cbb4436266523b6b366e41af3c4`  
		Last Modified: Tue, 05 Aug 2025 05:03:18 GMT  
		Size: 11.7 MB (11677426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e56a69c51e795f0efda9413f972ee73eadeacf213f75d2dbb29ede1e650d105`  
		Last Modified: Tue, 05 Aug 2025 05:03:17 GMT  
		Size: 14.1 MB (14129448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec2ec9f4571afe5a96045194585f18807ad68fee49f35f66918db6445c7391`  
		Last Modified: Tue, 05 Aug 2025 05:03:16 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f0ceb4bd0b550d13aa116072ecf5664b898e325a56633f86f6fe1af6658a50`  
		Last Modified: Tue, 05 Aug 2025 05:03:17 GMT  
		Size: 1.5 MB (1525006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db981765643cf36673f860b0533909548f3fe670d7a4544c545729c63ac174f3`  
		Last Modified: Tue, 05 Aug 2025 05:03:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:85129beae83ee75ad9153defbd809c7d2259bca03f59932e16259ae3718c02fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8bd5a3e628e7931621ac28d6549f62d3e109786dbc8e1bd8e7171116670a60`

```dockerfile
```

-	Layers:
	-	`sha256:027338cc615f615b3a5a79a1d0005be199bee99af0db24a088312b0f61f330ca`  
		Last Modified: Tue, 05 Aug 2025 07:17:04 GMT  
		Size: 593.4 KB (593357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08a2c934485be43b902c0699c5d7b7b38067fcdb4debc8c7641decfc04b2d7c`  
		Last Modified: Tue, 05 Aug 2025 07:17:04 GMT  
		Size: 43.4 KB (43379 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; riscv64

```console
$ docker pull wordpress@sha256:94f6246329a795ee376fc393faf0ddfc4188abc0ba4a87bc898f8ddfa45cc2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60509893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c4fcc598956d8b6d970d7906291bb8433083375e9a69ad3f25528778465473`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:17b966016c016f70afd8266fca422f482b22e4eab3e9c9c6ac09e0eba67284ac`  
		Last Modified: Tue, 05 Aug 2025 18:18:28 GMT  
		Size: 12.2 MB (12183555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c65ae7e656bbf9bd79a076258055bf95b12d4bc9326418bd41498de782d287`  
		Last Modified: Tue, 05 Aug 2025 18:18:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e87f61d0767972557cef29bee74db3fa59276e864db90f6dded1ee4c092e5f`  
		Last Modified: Tue, 05 Aug 2025 18:18:28 GMT  
		Size: 16.2 MB (16241871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6797e126307c1e98e53074f7f9b43a7d8dabad9c02412813172e9615eb049c`  
		Last Modified: Tue, 05 Aug 2025 18:18:26 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a33ab103197ce2c98c0e2064a187ae977a5c332f51e26013ba8eb42b1d3fc`  
		Last Modified: Tue, 05 Aug 2025 18:18:27 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048affb07b9b4ff59fdb3d17b51d90f8d1e1211c293b0d8976560dfc6ba22a3f`  
		Last Modified: Tue, 05 Aug 2025 18:18:27 GMT  
		Size: 19.7 KB (19738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3422f221892b968b9b341adbc0c3594cd3b35efcad8de9b4fff28a0a09a95b0`  
		Last Modified: Wed, 06 Aug 2025 08:10:47 GMT  
		Size: 11.5 MB (11525447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556dc0b369eed708e40bd0237d60f4f75f15e446491cd62add2b44ab8d40388b`  
		Last Modified: Wed, 06 Aug 2025 08:10:47 GMT  
		Size: 11.9 MB (11882592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171302fa17ebccd6b69ee1773d27a8a63f9490b924e86858d7f944f7ff212419`  
		Last Modified: Wed, 06 Aug 2025 08:10:46 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abc31b8a1b381450d565c31f8d17e103acbc8de79308e39c8c955f21dbfaa6a`  
		Last Modified: Wed, 06 Aug 2025 08:10:51 GMT  
		Size: 1.5 MB (1525015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8d4df32386234c7b8fc78341763fdd8475d3f196e5d1dfcc783aaeccc0d914`  
		Last Modified: Wed, 06 Aug 2025 08:10:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:eb09360a6cf4f01bfe1f3791f164b431fd85a27e0803dac564e43e926ea515fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c01fa226eae4e2abd3644ca43c6007a5bc93733de9ab8e566ab5b2d058ce8e6`

```dockerfile
```

-	Layers:
	-	`sha256:734acce910a3e916109ce45f06d8f0916f517a229341edb9ff4bf7c574b63a10`  
		Last Modified: Wed, 06 Aug 2025 10:14:30 GMT  
		Size: 593.4 KB (593353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151e444d2545d4736f6c742f4eaf95d2105ba01d0661da6c82b8e544915aecbb`  
		Last Modified: Wed, 06 Aug 2025 10:14:30 GMT  
		Size: 43.4 KB (43377 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:bcf4984062477eb6516748d51ae42c7f4e36e7345654609669af0ae04bd10480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64470199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefaba44c9d064561b7cda2b79eb3f07b16f21acdd67827bfbd2dd88dada8443`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:89f4aeed31ff4295df269a7268512a0d78f7ff35c390b0df731eb9a6f59b209b`  
		Last Modified: Tue, 05 Aug 2025 00:13:49 GMT  
		Size: 12.2 MB (12183556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97317b1323b890e402368564b0a3d853495c568eb013b4fb56fb9aa889cd91f5`  
		Last Modified: Tue, 05 Aug 2025 00:13:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae329820c324679f69eb7100b4849da54c7d4f695994c67f271415996256627`  
		Last Modified: Tue, 05 Aug 2025 00:13:49 GMT  
		Size: 17.1 MB (17147217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7237498d0655a3b55e06e6f6a22cdd2eaba12350845dbc4b799d3d8b527017`  
		Last Modified: Tue, 05 Aug 2025 00:13:48 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13762af09b4b29e95a34ea1ebeaf74837356bf58f9b6050321f2ab6077b7dcf`  
		Last Modified: Tue, 05 Aug 2025 00:13:48 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3a0cb9d69d8b5e149c43e0a6ce9deecc2a0b6ed0adc8140738b4b291d4a57e`  
		Last Modified: Tue, 05 Aug 2025 00:13:48 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30763c83d56213fcc00d4205f8a044c806c5ece2de99638762f4c138b41c1d2`  
		Last Modified: Tue, 05 Aug 2025 02:42:52 GMT  
		Size: 12.4 MB (12425252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8696651667f42a65dc5c8a3bb374a34df66faa3c86bd4506c1400add1128008`  
		Last Modified: Tue, 05 Aug 2025 02:42:51 GMT  
		Size: 13.8 MB (13819910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d27f864a914f82395f941a8db5af245fd23667a69e76538d2de0da6e3d1f27`  
		Last Modified: Tue, 05 Aug 2025 02:42:50 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852cce063654650d34180e08f005931cbe846e10e4cc3d10437cda6e01138c7`  
		Last Modified: Tue, 05 Aug 2025 02:42:52 GMT  
		Size: 1.5 MB (1525004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ce17784fd9e5914db04fc3db2354c6f18c8830669e61d0c3c9e8146a26543`  
		Last Modified: Tue, 05 Aug 2025 02:42:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:16a3bdc58ca12e61faf09e7e28dbd001d4e01a6c560a0ccfdd415652e0828a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.6 KB (636602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905782b26060e6df76a6c9d2b7f7ef70cceeb2263f7b2751ebb38720ae3a78df`

```dockerfile
```

-	Layers:
	-	`sha256:9e25a3c1c6dbba0f7415319181180b3401ad84d34349365e4f19937048975a4d`  
		Last Modified: Tue, 05 Aug 2025 04:16:47 GMT  
		Size: 593.3 KB (593299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd887bc468add364f96512d299d764bceab5928961788db4db7d026a668e755d`  
		Last Modified: Tue, 05 Aug 2025 04:16:47 GMT  
		Size: 43.3 KB (43303 bytes)  
		MIME: application/vnd.in-toto+json
