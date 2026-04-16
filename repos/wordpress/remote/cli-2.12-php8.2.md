## `wordpress:cli-2.12-php8.2`

```console
$ docker pull wordpress@sha256:f8c0f721ac8c2378d9f18826dfe9c8f55ccccd6fd80108c060bb37bd858eb8b7
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
$ docker pull wordpress@sha256:b87e23b93acd6b6e0f4b8ab4be6cec962f352ff6401a1413ec13244fddd880ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67785550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb92f8674a453073df6e1fa8de6c7cfb01e3d2330af7481c8120d5124ed1b1b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 20:20:34 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 20:20:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:20:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:23:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:23:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:23:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:23:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:23:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:23:13 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:20:26 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:20:26 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:20:26 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:21:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:21:08 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:21:10 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:21:10 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:21:10 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:21:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:21:10 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:21:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:21:10 GMT
USER www-data
# Wed, 15 Apr 2026 21:21:10 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09946db3488ff71fb1ed25fa87d14646495ac5aff70952a82b65667350fb9c68`  
		Last Modified: Wed, 15 Apr 2026 20:23:20 GMT  
		Size: 3.6 MB (3587452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a777f13f4e079da717ef449ba4d2a4b98aae5225e2095cf97c89d175e319fd5e`  
		Last Modified: Wed, 15 Apr 2026 20:23:20 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd7e3e11a75fd2916b1fb9d5bb44c8ccc3780d241d9f62f8fbebbe3b31728cd`  
		Last Modified: Wed, 15 Apr 2026 20:23:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21a93c396c8d1f7729e7488873f98d7db590db48a00ba98b938158da342ecf`  
		Last Modified: Wed, 15 Apr 2026 20:23:20 GMT  
		Size: 12.2 MB (12177833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339bda7c7265b18f8cf8428f9bbbc9107c5fd3142eb3c5da4b0cfc608c564304`  
		Last Modified: Wed, 15 Apr 2026 20:23:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8ac9d686be65c47a8397c03c5b9174eece9628d5aa214e109aeb1d1c56713d`  
		Last Modified: Wed, 15 Apr 2026 20:23:21 GMT  
		Size: 17.2 MB (17200203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919522c552e92884b65ba8ff99b729f9e51504294a7e7f0d778f21b81db5e9a2`  
		Last Modified: Wed, 15 Apr 2026 20:23:21 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5823a66f83f4da673be2cb69cc91c9a1e1170a7aec4be5220c07af3078edca`  
		Last Modified: Wed, 15 Apr 2026 20:23:21 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f1da26177473fe6b8ca1a17e3d2a93a65b02a0618fd1083b9a846f530a67e`  
		Last Modified: Wed, 15 Apr 2026 20:23:22 GMT  
		Size: 23.4 KB (23416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b508af1d35706ebc8f8847e04a00cf7f9e538c497af06ee6ad524ae566ebcb0`  
		Last Modified: Wed, 15 Apr 2026 21:21:19 GMT  
		Size: 11.2 MB (11154439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9578e37602f246b79689f0990bff173a482f4104ca385f619528bc1f08360d46`  
		Last Modified: Wed, 15 Apr 2026 21:21:20 GMT  
		Size: 18.2 MB (18214105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8630fc0d30e7b3c44905646d88a39ee3237d631f73e345789317f72d98ea5b2`  
		Last Modified: Wed, 15 Apr 2026 21:21:19 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d483d94f3b031a406445d07546b5386b51d4789942bd331074da9f577056ba`  
		Last Modified: Wed, 15 Apr 2026 21:21:19 GMT  
		Size: 1.5 MB (1535574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6e9c51df185ec0d1bb2fc1baa66c7bd44ee106f0b672d454961f110e6e2e36`  
		Last Modified: Wed, 15 Apr 2026 21:21:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:477770fe4cd76fae132661765bcef20fbee14ff5f41dc55716349f58ecc2f820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 KB (681196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649a52ee03f1eda515a2c5e5e5917a0e18e7664f80979794ec553a811a739b8d`

```dockerfile
```

-	Layers:
	-	`sha256:69f22a4961752f748105daa6997d5eabca735ce9add606f283c153354547d53b`  
		Last Modified: Wed, 15 Apr 2026 21:21:19 GMT  
		Size: 639.1 KB (639094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94982fb11f5a919cbec36ab7a6f664db162df3d04541b734df5d5b22c6f45fc`  
		Last Modified: Wed, 15 Apr 2026 21:21:19 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:2a905878ca5cc5576d5806c6b75b2ec7f3ec90d4010e8b361e03e4b184927d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ef6a8f4eeae83c148b3e48a2942f0cb4d4d8fb9c1dba3a754ebec159c13c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 20:16:16 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:19:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:02 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:19:40 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:20:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:20:49 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:20:52 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:20:52 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:20:52 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:20:52 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:20:52 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:20:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:20:52 GMT
USER www-data
# Wed, 15 Apr 2026 21:20:52 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acc069fae3b28b51bb1ae472d8f03e6ffce9d7e7c41adee292111c9577d4e23`  
		Last Modified: Wed, 15 Apr 2026 20:19:08 GMT  
		Size: 3.5 MB (3543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40971e1694a61f993d377bda480d72527bfd195acc847501026d71b22d620ef9`  
		Last Modified: Wed, 15 Apr 2026 20:19:07 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466e7145a23f86b8c1014d099e673ac7a98559dd2edab681f281d13190cdb531`  
		Last Modified: Wed, 15 Apr 2026 20:19:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55092fc540cdaea934758858f57cb3d8a4dd1a7be0201386c70312d58af64888`  
		Last Modified: Wed, 15 Apr 2026 20:19:08 GMT  
		Size: 12.2 MB (12177833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cddb6933d7062ddb681a25cc321ec11f1daf5e18521c81cc73308895fa6e0e`  
		Last Modified: Wed, 15 Apr 2026 20:19:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebef6da59ae7af691c22c183e86e3781b384ed1f02181a557e870d55c844920b`  
		Last Modified: Wed, 15 Apr 2026 20:19:09 GMT  
		Size: 15.6 MB (15609796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c221a70906978a642cae0b53ac46e67b3c23238be85ea4cd8d6bd10915d2f33c`  
		Last Modified: Wed, 15 Apr 2026 20:19:09 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1dcc8d3537aca8c8402450081dfb9ff73472c4ed6d38993823617e2cb5ce01`  
		Last Modified: Wed, 15 Apr 2026 20:19:09 GMT  
		Size: 23.2 KB (23205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ce89b9929e02662099c4d8e186dd5f5a19ee193e7b4dc17587ab47cd9d3b49`  
		Last Modified: Wed, 15 Apr 2026 20:19:10 GMT  
		Size: 23.2 KB (23226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abaa93020eb1b9b1b4f36773e39191788f10e27928546ed7a3a50d9ff18e908`  
		Last Modified: Wed, 15 Apr 2026 21:20:58 GMT  
		Size: 10.9 MB (10882817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02bcd18be6229e17ab0a2d5b791a994d6b7cc02ec40ffcb684b363bfc577755`  
		Last Modified: Wed, 15 Apr 2026 21:20:58 GMT  
		Size: 14.8 MB (14807011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce0ba7c20afd1660ba6b1d6f88eb182ad684a8a1335bcc7afcfa43476b23b4a`  
		Last Modified: Wed, 15 Apr 2026 21:20:57 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445003dfb9b8338e568e25093a999f62bc077ab3cb7a372f832b875ad028dec`  
		Last Modified: Wed, 15 Apr 2026 21:20:57 GMT  
		Size: 1.5 MB (1535602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1226f4b1f9867d59d51273ef68036fc870bdf96ebe772d640a60f2de0f6cbe`  
		Last Modified: Wed, 15 Apr 2026 21:20:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:f0190ee24a48ac84c66796c9f852161e62ae7d05e18dde7986b0135cdfd199be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2fa11938ed8f223c761d5dfe857ac91e867683ac7fa228d334161b14114d53`

```dockerfile
```

-	Layers:
	-	`sha256:5845e48c015ab5ee70316fd0f3b1e3a65b60420488043802f6139e96ac655d83`  
		Last Modified: Wed, 15 Apr 2026 21:20:57 GMT  
		Size: 42.0 KB (42019 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:d2e709cae58e02d1b1760ee1d798ebf73bb06643b9af27c4c605f60f212c4159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60869190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c770084976c50828ef2438f80ab6ccf730bc1a4c94708696cab330b6e08a4248`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 20:25:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:27:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:27:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:27:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:27:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:27:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:27:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:29:35 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:29:35 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:29:35 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:30:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:30:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:30:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:30:48 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:30:48 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:30:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:30:48 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:30:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:30:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:30:48 GMT
USER www-data
# Wed, 15 Apr 2026 21:30:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1809007c646ae5266bca7ed17bb48478c4dccdf9341b6dffdfc44520ea382aed`  
		Last Modified: Wed, 15 Apr 2026 20:28:05 GMT  
		Size: 12.2 MB (12177847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f356d35b5d82f1e5a59322c3ef9b13f0328db8fd33e3d326adb814c5d8a2c1`  
		Last Modified: Wed, 15 Apr 2026 20:28:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be3e26c45f4b0fa6c583ab53290bb6877b441bc9f753a6929d8267a706b231`  
		Last Modified: Wed, 15 Apr 2026 20:28:05 GMT  
		Size: 14.7 MB (14677845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22f5d139ccbed04da11791ea2f687a4438f71b13ddea121cdbf04db50fa4ec`  
		Last Modified: Wed, 15 Apr 2026 20:28:04 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ff64d2ed3fb3bb931bea218715cadfa698a62320b57929b2d6fbc7f6986669`  
		Last Modified: Wed, 15 Apr 2026 20:28:05 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee797f24db3c2343daf7f460b334c937cc6aa56c418cb21d98891fbb6740e2fc`  
		Last Modified: Wed, 15 Apr 2026 20:28:06 GMT  
		Size: 23.2 KB (23229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111ef0244886a865395585a90072748f1f6184f6b61c9232f14334243a9ae574`  
		Last Modified: Wed, 15 Apr 2026 21:30:57 GMT  
		Size: 10.5 MB (10536198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b76be5a89dc7736f01b354390ce9c1049371db12fa1b71fad591517c3d546e`  
		Last Modified: Wed, 15 Apr 2026 21:30:57 GMT  
		Size: 15.3 MB (15263870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca101af7c5b3129e31d5ec5e5c2ac2199462d6550a4ca5389b1bf19e492576ac`  
		Last Modified: Wed, 15 Apr 2026 21:30:56 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d119666ab3e3ebae2ea489acd771e0f5bd05804f5fda3de81dcda0ceea90a164`  
		Last Modified: Wed, 15 Apr 2026 21:30:56 GMT  
		Size: 1.5 MB (1535579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26cfd32881ef53e06508d7863093f2f3d7967d614e89c9f7ba22248e4e531aa`  
		Last Modified: Wed, 15 Apr 2026 21:30:57 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:35b6d15fa01ec601172d58f3138dda5e89f2644e5ce07922aac40eed0c2909a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.5 KB (679470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9bf6fc63c7f0624214f164227bc2300377d6cb048c5f801affc4941038beac`

```dockerfile
```

-	Layers:
	-	`sha256:720dfce726ad7bfaf91d1eda5e5859c1dce48ba86a47df71bb52e8e7b709d2d8`  
		Last Modified: Wed, 15 Apr 2026 21:30:56 GMT  
		Size: 637.2 KB (637236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45be2b27bb73e39ccb5c7d6e6257cb78480870bad0a9b1fa46aed803139fd118`  
		Last Modified: Wed, 15 Apr 2026 21:30:56 GMT  
		Size: 42.2 KB (42234 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:dd21f0350e90f471461ad26a66f0a9372a18d081ccbf876dc1cb32384e46020e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66864944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966a9f30c0364f64a6907b400003778072c289a29e159de703456f12759ffef3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:27 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 20:18:27 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 20:18:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 20:18:27 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 20:18:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
# Wed, 15 Apr 2026 21:35:56 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:35:56 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:35:56 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:36:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:36:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:36:50 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:36:50 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:36:50 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:36:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:36:50 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:36:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:36:50 GMT
USER www-data
# Wed, 15 Apr 2026 21:36:50 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969ef7d4d2832b655d1c47225b78d9bd116ff3c1fcbe544763d7901e38d1ce5`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 3.6 MB (3596147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ad752f1843f09d2c799be39e8506bb6c7ec0586ee1b5a96c69b59a726a59fb`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc155e2a5c974ec9b1077c72f47537d362790237fbfef4d2097c9a2fb8cd985`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8064171cbfb71f6badac1c12ed2084b51f4cd5585f49a24115265759a60229ba`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 12.2 MB (12177836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c9d24089c392566dc0e2a6bceb943cb406d9aef6d685d7cca17fdf91910616`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975ff94f1292b46256b4714daaa148f987a0555734a426006f8127930e88464`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 17.0 MB (16978250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0142424a30a087d18db3d050dfbae5e7e833fc913fea92c333dab3b44546b01`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83738071d2d28804211be9939d2f5d7f127bb3a42e1303e0d8bbd56b37584e62`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 23.2 KB (23214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d706166bd4a2b29d5ce15a265d663be99023dfe35b5e846097c78b24ea3941`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 23.2 KB (23232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bc2ae36920657cee11312365eb49ec302fa5c288832722444e51d2123d7a28`  
		Last Modified: Wed, 15 Apr 2026 21:36:58 GMT  
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
	-	`sha256:234741164c9f032565596ab0d518dcbe0af9ccb565363926f2693665f934dd45`  
		Last Modified: Wed, 15 Apr 2026 21:36:59 GMT  
		Size: 17.2 MB (17227597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad477e5da36e82e1ac9540d39d9a23af6f9665bc96b30bd0487b475637787a8a`  
		Last Modified: Wed, 15 Apr 2026 21:36:58 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb53993d3a0e76d6de8a0b80dee6fdc4c2bb425ca64a276bf64d6e0107eca63`  
		Last Modified: Wed, 15 Apr 2026 21:36:58 GMT  
		Size: 1.5 MB (1535630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f48528e7965cc02d36d93a2b5fd0bdae242d4a317e5fdb66a467854ad5476e`  
		Last Modified: Wed, 15 Apr 2026 21:37:00 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:789ab0ed87946a62c2b7164b17b05b7b8819ed8dfae6fda1e0bda12da4997630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.5 KB (679522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200a0590f71e2309611d0c0921fe973917d6f8d9a0614b5086f013d03b4165a1`

```dockerfile
```

-	Layers:
	-	`sha256:f2862ba6f51a9e6e60c5980cadc33a423756fbfd4baf803baaae7648f342cad5`  
		Last Modified: Wed, 15 Apr 2026 21:36:58 GMT  
		Size: 637.3 KB (637256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918654949f083f5c109460dd6f57d53c69c59f6e087d8c034667d989fdff6ea0`  
		Last Modified: Wed, 15 Apr 2026 21:36:58 GMT  
		Size: 42.3 KB (42266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:495ccdf9fb76065b503a961e38eff325ade5c071c1d59d1854be175b6e90b9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67259954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1333f9438bf029667d4ed43f62297558287fbdef7e60893313aef7c030ab3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 22:23:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 22:23:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 22:23:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 22:23:45 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 22:23:45 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 22:23:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 22:23:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:26:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 22:26:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:26:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 22:26:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 22:26:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 22:26:50 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 23:14:53 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 23:14:53 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 23:14:53 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 23:15:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:15:45 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 23:15:47 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 23:15:47 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 23:15:47 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 23:15:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 23:15:47 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:15:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:15:47 GMT
USER www-data
# Wed, 15 Apr 2026 23:15:47 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4f322ba47d151b842839c5b48431d6dbf660b2c66014e6df7131a5fed9feb`  
		Last Modified: Wed, 15 Apr 2026 22:26:58 GMT  
		Size: 3.6 MB (3625724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cca78f8d7ed0eff6ac5a0d0c563e6ca6a0de3cc2cc47e26b0bee5837a04bbc`  
		Last Modified: Wed, 15 Apr 2026 22:26:57 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a974624a947bdd00b29870baccf9fb9dbbc29dfab45fb91918942c4e0cc34388`  
		Last Modified: Wed, 15 Apr 2026 22:26:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5f9693a80a9c71c30d3c2418e4c80f3c865a5309063e7bb6d5936bb060d508`  
		Last Modified: Wed, 15 Apr 2026 22:26:58 GMT  
		Size: 12.2 MB (12177819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea9a5db29a60eaf7f19319354404dc5b92c0f41b8933a0da38b2d7093797e4a`  
		Last Modified: Wed, 15 Apr 2026 22:26:58 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e14f8a691d820d8fca81b0ee2e72510e860c24634b48eeebe677d9c3358e09`  
		Last Modified: Wed, 15 Apr 2026 22:26:59 GMT  
		Size: 17.6 MB (17561024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00700ec4966e429fd6f166d042e8b7bb621b96c5be9e1ab56478b5b9a9fe56ab`  
		Last Modified: Wed, 15 Apr 2026 22:26:59 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be41650e01b8c879d4648630c66d954c49e43c86ae1bd95f0ee2190254d1dce`  
		Last Modified: Wed, 15 Apr 2026 22:26:59 GMT  
		Size: 23.4 KB (23393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db60b1f43085e614c21b8e136b3af415b4582012f4955f271233e13179445e43`  
		Last Modified: Wed, 15 Apr 2026 22:27:00 GMT  
		Size: 23.4 KB (23418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a725bc23e3f77f9a7a7b578aebd628721f6761daf214928bfe7ef27874d4255`  
		Last Modified: Wed, 15 Apr 2026 23:15:56 GMT  
		Size: 11.3 MB (11339283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e0493c6fe02da056507367f20a27f30f5a0db0de55cf9483894dfbca15b3fa`  
		Last Modified: Wed, 15 Apr 2026 23:15:56 GMT  
		Size: 17.3 MB (17278346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c67e009d4cdfab04b304960d8f7a16b1a93b246808f66cd0b911e9b7c00f60`  
		Last Modified: Wed, 15 Apr 2026 23:15:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a577c7d5f229f5cf33c72b44d3ec51533f0627f4752f26e0d1778c3b35067044`  
		Last Modified: Wed, 15 Apr 2026 23:15:55 GMT  
		Size: 1.5 MB (1535561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb80be85bde209805faf42169a96f71b4c2dbadfe4ccfd81361344405e18781`  
		Last Modified: Wed, 15 Apr 2026 23:15:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:ea04d7fc5999600f0fffa491cae3cf566f286d5d532aa4c2f68cf7035eca81f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.1 KB (681131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc94fcb319814c948d9d43c5993a5f0ac739432a240942cb7066d470beb2e79`

```dockerfile
```

-	Layers:
	-	`sha256:892cee7edfcbe044179eb381fb31057aa6ab63a6a069fbfcf7d7fa7432dc514f`  
		Last Modified: Wed, 15 Apr 2026 23:15:55 GMT  
		Size: 639.1 KB (639069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e1829e10629eb9b163466d11b098cc0200a2a02a0546af145e4b79bd237039`  
		Last Modified: Wed, 15 Apr 2026 23:15:55 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d53765e55e35ff20875f2ab1aa21ee784c018101fea0de083680ff6dc5fc7937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b48a88ec1e25ce3fa109f4fc0e91af8afe6c3a2dbfeca75a070ed59005c5c6`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:48:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:48:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:48:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:48:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:48:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:48:59 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 23:59:37 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 23:59:37 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 23:59:37 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2026 00:01:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 16 Apr 2026 00:01:17 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 16 Apr 2026 00:01:20 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 16 Apr 2026 00:01:20 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 16 Apr 2026 00:01:20 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 16 Apr 2026 00:01:20 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 16 Apr 2026 00:01:20 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 00:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:01:20 GMT
USER www-data
# Thu, 16 Apr 2026 00:01:20 GMT
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
	-	`sha256:ddc3ce727f205a16326e590d73c3841d424ed040a810a7ab7acc764931833361`  
		Last Modified: Wed, 15 Apr 2026 20:49:28 GMT  
		Size: 12.2 MB (12177848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a26180da828f78e495a3a0cffc3537f462eb49474c165db8b5997a9580ad558`  
		Last Modified: Wed, 15 Apr 2026 20:49:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9703221501321e4518c5976c9046c68f7ce650d697598b5d1c0d871fdade569d`  
		Last Modified: Wed, 15 Apr 2026 20:49:29 GMT  
		Size: 18.1 MB (18148337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8740cd534473129b829885e58949d08b1a47264ecbd100ae9b05d985c405b8`  
		Last Modified: Wed, 15 Apr 2026 20:49:28 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116927e3a6dca8cb0d19fca380dadd977f9997cd081503b8c8b9a75bec38c95f`  
		Last Modified: Wed, 15 Apr 2026 20:49:29 GMT  
		Size: 23.2 KB (23225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65b09960fc5eb29913780d6896b20cb5c7a00d3ddaff0c88a7b0c07f1030c2`  
		Last Modified: Wed, 15 Apr 2026 20:49:29 GMT  
		Size: 23.2 KB (23243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32de231944f1c336370e4d25acd2895ec1702534dc2d95d27555cca610ef3b1`  
		Last Modified: Thu, 16 Apr 2026 00:01:40 GMT  
		Size: 11.8 MB (11817818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4ac4d2908a94bffcace7cfdb9ddaddb2a5721c9c0cc50e8b973f63476ebdac`  
		Last Modified: Thu, 16 Apr 2026 00:01:40 GMT  
		Size: 18.1 MB (18104780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0ff2c5908baa1c24b88d15c234a6b4bc51b683821783f0712178a317956bf`  
		Last Modified: Thu, 16 Apr 2026 00:01:39 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc25678464ff3bf82a884c9f37c7fd2ad91b688905298fbfe59b521938073a8`  
		Last Modified: Thu, 16 Apr 2026 00:01:40 GMT  
		Size: 1.5 MB (1535630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c128f5e2119013bd398264d2d928483f34382c23ab9931a52384332f593d1ff2`  
		Last Modified: Thu, 16 Apr 2026 00:01:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:5225499a3d60432ed8578e9462da4df2fd4d374e8cbbee3f50255fb906ab622c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.4 KB (679386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64286d7d5e40482a1988ad927d1286c8be5fc1034c810e4aff7a89613a4d0087`

```dockerfile
```

-	Layers:
	-	`sha256:cc07ed6f0e565db2c4a2ce2b9df4d15a1280c65abd37ec9c058576aefcc91532`  
		Last Modified: Thu, 16 Apr 2026 00:01:39 GMT  
		Size: 637.2 KB (637233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c550167df18f7a9f6ba218895119ffae7b15af2aad98a898decbbcb7edf06902`  
		Last Modified: Thu, 16 Apr 2026 00:01:39 GMT  
		Size: 42.2 KB (42153 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; riscv64

```console
$ docker pull wordpress@sha256:bf714d69af89394c5421506fcd7ece05bf166bc87d43530177bcec34795eeb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64400222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7817344979ad6e6168bdc97869ed33cb24e7edcfb29e2afbd8cb3a15a0991ad`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.2.30
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Thu, 29 Jan 2026 04:58:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 29 Jan 2026 04:58:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 05:45:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 29 Jan 2026 05:45:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 05:45:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 29 Jan 2026 05:45:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 29 Jan 2026 05:45:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 29 Jan 2026 05:45:13 GMT
CMD ["php" "-a"]
# Sun, 01 Feb 2026 01:16:12 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sun, 01 Feb 2026 01:16:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sun, 01 Feb 2026 01:16:13 GMT
WORKDIR /var/www/html
# Sun, 01 Feb 2026 01:29:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sun, 01 Feb 2026 01:29:28 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sun, 01 Feb 2026 01:29:39 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sun, 01 Feb 2026 01:29:39 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sun, 01 Feb 2026 01:29:39 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sun, 01 Feb 2026 01:29:39 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sun, 01 Feb 2026 01:29:39 GMT
VOLUME [/var/www/html]
# Sun, 01 Feb 2026 01:29:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 01:29:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 01:29:39 GMT
USER www-data
# Sun, 01 Feb 2026 01:29:39 GMT
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
	-	`sha256:35b59d9f9a60915a1a7fb3de16f38e8d1701466db7614906de7bef2cc7a12673`  
		Last Modified: Thu, 29 Jan 2026 05:46:19 GMT  
		Size: 12.2 MB (12177929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3e31c7c9552ea5df074a9383432e4b58ae9437a200300a99c064c291fb0b4b`  
		Last Modified: Thu, 29 Jan 2026 05:46:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3fb33b64d60745715d19fbbb70264f7007e2a9c9f433cc872b90902d30762e`  
		Last Modified: Thu, 29 Jan 2026 05:46:19 GMT  
		Size: 16.3 MB (16268869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3309521118709088a30de2d306d5004b577ff258bac040826c61fd8b4583dff`  
		Last Modified: Thu, 29 Jan 2026 05:46:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf38f6f4e16ffebcc1db288f63775b148e1c1118cbd635e59f38b84b44798c0`  
		Last Modified: Thu, 29 Jan 2026 05:46:17 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0a4cb800f4e0059011bbb22cde9f72e4f5c7db5b2490abcb68d10f3d980a36`  
		Last Modified: Thu, 29 Jan 2026 05:46:17 GMT  
		Size: 23.4 KB (23351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48137d0cec36da3d13790d87a01c37acd0f2442b685238efb07576d23fd7324`  
		Last Modified: Sun, 01 Feb 2026 01:31:06 GMT  
		Size: 11.6 MB (11599370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c658befe8a53dd9f01a7473c1babbbaca50e88f368a5b020fed0f4c9b606e38`  
		Last Modified: Sun, 01 Feb 2026 01:31:07 GMT  
		Size: 15.4 MB (15440417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669dce5d5477763b24f4ff2214b56816a0c5a25edec5d02679092782f438174f`  
		Last Modified: Sun, 01 Feb 2026 01:31:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657c631a2091b8862ce4446a4b1ba047effefbc982447e60cf7eebf03c622da`  
		Last Modified: Sun, 01 Feb 2026 01:31:04 GMT  
		Size: 1.5 MB (1535709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464cb6d31e9971fab01bea4b40f1d8b3eb36471aa974b2772fc8ccf73aceaa2`  
		Last Modified: Sun, 01 Feb 2026 01:31:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:cb59dd933a6816d179b47b05bf377189dc4cf65f6fcfb9321d479baf93a4688b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 KB (681338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd95e230c7dadcb4668fb5c49b1b001b23225c6bac3287111934d7db3da11c0`

```dockerfile
```

-	Layers:
	-	`sha256:d5144385ee5a70983f7eb3066dd603b30bf6e9a2650781310e17181e6489d9a0`  
		Last Modified: Sun, 01 Feb 2026 01:31:03 GMT  
		Size: 639.2 KB (639184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce6e4de824bd637e6a1d74d3b8096d69b8413f5407f65afb0be5a6c9e7f6766`  
		Last Modified: Sun, 01 Feb 2026 01:31:03 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:c4c0071ffe072bb9d378ea48183a3af0a598bf8f985415eefb5ec5f38a11830d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68446104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78472754a39927a174a4a147461a44495586ef62fb5aa76226a5b8e8e4876e5f`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_VERSION=8.2.30
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Wed, 15 Apr 2026 20:29:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:29:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:33:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:33:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:33:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:33:29 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 23:44:33 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 23:44:33 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 23:44:33 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 23:45:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:45:54 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 23:45:57 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 23:45:57 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 23:45:57 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 23:45:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 23:45:57 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:45:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:45:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:45:58 GMT
USER www-data
# Wed, 15 Apr 2026 23:45:58 GMT
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
	-	`sha256:a3f4e57cc32de14d0bc70fed4de7815a3d73f2d19db5f964376b9c49bd26696f`  
		Last Modified: Wed, 15 Apr 2026 20:33:49 GMT  
		Size: 12.2 MB (12177853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2c3fcba3aedd38f3a0d025929b20dedf7106ba63c8e3904f550c1525253d8`  
		Last Modified: Wed, 15 Apr 2026 20:33:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d34cd07cd90af92ef55817530d1bf1d095db4990c74eaae5b6a35602c0113ee`  
		Last Modified: Wed, 15 Apr 2026 20:33:50 GMT  
		Size: 17.2 MB (17163441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bc9d1607d2016edd935b460983f0162104b580ccae20eca8770ea79a4092f0`  
		Last Modified: Wed, 15 Apr 2026 20:33:49 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94d0f6add9fec7e2a5b26f85f8ed17f220c119b6aff0544c04ef78a36e62b7f`  
		Last Modified: Wed, 15 Apr 2026 20:33:50 GMT  
		Size: 23.2 KB (23229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9354d4a7830b201b6e332ac371a7a15c7bf4f1ce045ebd1edd7f83c08453ca66`  
		Last Modified: Wed, 15 Apr 2026 20:33:50 GMT  
		Size: 23.2 KB (23247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ca22e03c89323e994c7891596fe1ccc05d544ab824c5bdb245785712bcefd`  
		Last Modified: Wed, 15 Apr 2026 23:46:19 GMT  
		Size: 12.5 MB (12527264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484be1dc20555f4c1648a235df21d7edba4ca5e96408941ecfb67f5f75f68342`  
		Last Modified: Wed, 15 Apr 2026 23:46:17 GMT  
		Size: 17.5 MB (17476982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdce0d270b8a0d98bb49488c2fdd1caf0e9f9098482cfbc2501f87e17c714fb2`  
		Last Modified: Wed, 15 Apr 2026 23:46:16 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a3a4005051b3b88459cf5da7a8820ea78ec568596b16e432584e4c426be4d`  
		Last Modified: Wed, 15 Apr 2026 23:46:16 GMT  
		Size: 1.5 MB (1535620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424137325c798dd94ecd6581bd6e6cbb8f7fa8457edee6687076008142581c7c`  
		Last Modified: Wed, 15 Apr 2026 23:46:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:5156dc7c1b8a2eca2af8bc11d8b6e9e272342d7c863e88bdff303270a64701a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.3 KB (679300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52209e90f60d7effb2c85a12abd40c6ef92a86074969db1fa9ca2adca4e5353c`

```dockerfile
```

-	Layers:
	-	`sha256:b23d1891c3af47687015af5dfd93498d38ae12ce7af8d589cf8c0eeab819de2c`  
		Last Modified: Wed, 15 Apr 2026 23:46:16 GMT  
		Size: 637.2 KB (637199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1843c3b42e61e03458685054dd1d818d3a2269a399b317ac9740c42af2495b`  
		Last Modified: Wed, 15 Apr 2026 23:46:16 GMT  
		Size: 42.1 KB (42101 bytes)  
		MIME: application/vnd.in-toto+json
