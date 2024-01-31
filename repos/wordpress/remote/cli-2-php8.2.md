## `wordpress:cli-2-php8.2`

```console
$ docker pull wordpress@sha256:c2d1d8c48f0dc37e7aa891f2608e03d8b8f25f424ddf3be5c2cba088e564713d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `wordpress:cli-2-php8.2` - linux; amd64

```console
$ docker pull wordpress@sha256:dc2ab81aa043f1cc2369dcccc06c1f278b4e6616c301236b7bcf4423064902a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67079185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ba8b91988514ed0795a5c479d0dcf826b627a42a9fb9097dfd55e0d3117cd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ef19a461f9d419fc91c59399a9daa1f3302d30f099065a185a8bfeea3c9a8`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 2.8 MB (2761515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2fc49c6a93ebf520a5ecba9c061dbdd22083df74d0de9dcac9011f3f927d9f`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a4aa92ed6361a95da0e916e30e661754a1edf38c0b8b15bee6872d055e3603`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdde487d2c3c481b0aa4cd0406254b43519751c01aa878faabca1606841a70b`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 12.1 MB (12096363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243db39c4f41b17d1f4c981d29228b0eb61f114ae253a3f4f129690393294e2e`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ef638f60d8b198190259a9c414de8d43da76f4d9e4df9b2b3320469a12128`  
		Last Modified: Sat, 27 Jan 2024 05:38:38 GMT  
		Size: 16.9 MB (16857316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5f523175bfa69fa0bdb6ef1a472af2814102afe64a92113c23e4312f5ed8c7`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13833c4952f93849a448a108118c1fec21e4035e2887b6b34a10c5a083daebef`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 19.3 KB (19286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e4acd10c233916c9a4052f6588ba078e1ec75a2ccd53b910a71d87e5a3b6f3`  
		Last Modified: Sat, 27 Jan 2024 06:53:31 GMT  
		Size: 20.5 MB (20509594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c33cd1838494d7485f8e3634b612eb61ff98893034b19b5a5d964170c91d56`  
		Last Modified: Sat, 27 Jan 2024 06:53:32 GMT  
		Size: 9.9 MB (9899363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2086863e4c1d2d0242affa99e83303cc5a4058f0a8f0b0d14546591823101`  
		Last Modified: Sat, 27 Jan 2024 06:53:31 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5183e9a9e63c97807998d813f58f5a32cf2e5f30c72b9385a2c52965bd5b38c`  
		Last Modified: Sat, 27 Jan 2024 06:53:32 GMT  
		Size: 1.5 MB (1521692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6c5e23ec0d3e96694b649aac07bbab97654c7fe38a3eae90a56f8868a1b21`  
		Last Modified: Sat, 27 Jan 2024 06:53:32 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:ac0effe02c9363566350f0cdd533b9a41dd772483971fa8141c16a0c718918e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da0fe1f13e354807dbce08f0f0dfdee5576fb661a995c661c4e6e1682ca40d1`

```dockerfile
```

-	Layers:
	-	`sha256:d28fc7f38361cbd7347a148dc9193fa1acd1189cfac857a5c3de1af3fd80fe38`  
		Last Modified: Sat, 27 Jan 2024 06:53:30 GMT  
		Size: 1.2 MB (1177685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac440d9f011e811fd7872fc289fff30eb46d4f70ab13a296922d2e0a57887ad`  
		Last Modified: Sat, 27 Jan 2024 06:53:30 GMT  
		Size: 43.5 KB (43459 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:fcd2bdce08171b9c95abaab18cdb1d185ebd12b119c7859f726015b37d6c333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63561465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcd8b1474923e8375115937d6fed678e8d00bb09c78f0ef35265a3b07246dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147d01edb253ab7eff347bb08482a430759361f869152a4c0a0ecdd946e0d17`  
		Last Modified: Sat, 27 Jan 2024 06:44:23 GMT  
		Size: 2.8 MB (2764487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b42f6e9b3a3a721beed37ea494f71a49e981f945e849780a3cc6a57bf1c0ed9`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136267c1932cb42af7ae697ecc07c459f4c5a75f3adf037cdfff9774f183ff3`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55005ed483beb1ca337359ab17a9675e229b931426997399767cc9d13937a3ad`  
		Last Modified: Sat, 27 Jan 2024 06:46:51 GMT  
		Size: 12.1 MB (12096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aedab67bb2ee246ae317cf484a9d5751a7fe4e6b2b339dedaa0cac726c5f706`  
		Last Modified: Sat, 27 Jan 2024 06:46:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7e27f2b4a7e51b4e9315691cc6fa9f5cab857358c03ced74f731d2650897db`  
		Last Modified: Sat, 27 Jan 2024 06:46:54 GMT  
		Size: 15.4 MB (15391469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945aa387dc42a2e26d776dc591a006a0681c06741b31987505cf6d32613278c0`  
		Last Modified: Sat, 27 Jan 2024 06:46:50 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfbe5d8f194673680f813a71566dad67d913560037594d384293921e0db8729`  
		Last Modified: Sat, 27 Jan 2024 06:46:50 GMT  
		Size: 19.1 KB (19134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6201a9e3cef623a04c4a63389617edc80fc56fdf5152325401385efe46fcb02`  
		Last Modified: Tue, 30 Jan 2024 23:00:08 GMT  
		Size: 19.4 MB (19444960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc14c7d24a6da70f11be523eabc6e164d85448f12c045cd790001fdd7b8312f`  
		Last Modified: Tue, 30 Jan 2024 23:00:09 GMT  
		Size: 9.2 MB (9152590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180dd91c274d3d815438931071983eabf81fddf38c9c1736249b9c8ad2173ce`  
		Last Modified: Tue, 30 Jan 2024 23:00:08 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8aa467a021473aa6459ec0fb45140a4e0990f9204315678fa79358fbd0dd31`  
		Last Modified: Tue, 30 Jan 2024 23:00:09 GMT  
		Size: 1.5 MB (1521728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a87812f0b62fdeac8f672338d8a96b13c41afad88620b92a5e1c7b9bb35f16`  
		Last Modified: Tue, 30 Jan 2024 23:00:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:1bbed5a66385391e93a06045a3e4851cf5c30b0bca5a21611eae14d05aaafa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb0064c51afe17a9941e0c9254f4507290bda078610727a7ca53160a3d86ea4`

```dockerfile
```

-	Layers:
	-	`sha256:83065e648fe67cefb257dcfb6bb80500f19ea12ef792ae23612da8f03c2169a3`  
		Last Modified: Tue, 30 Jan 2024 23:00:06 GMT  
		Size: 43.4 KB (43400 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:6da30aa1c04281e1be612c06fd24643512d7cccd55cdba283b806b2457682102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5917263a77c39782b003f5fda319b9975f8fd23ae5434daeac495d3cbf7b4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fcdc554dd7b708317247ba5731b0d76bc06dc68a48af57f662820d33c665cc`  
		Last Modified: Tue, 12 Dec 2023 22:36:17 GMT  
		Size: 2.6 MB (2608664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4717604343f2899832c4417228ef3cdb02080f72378a4152eb72083f09c96e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a6a05c32e2329e654bc633b417da36b7c74ed6bf626231bf0e900f912838e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07f131f27f224c80e5f595081eb7366881a06d5c84c536ab0e7d4c58145fb1e`  
		Last Modified: Sat, 20 Jan 2024 01:12:58 GMT  
		Size: 12.1 MB (12096375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a6dc7b339351a2d684e716ab2145e23ac32cdc4c7cf327cb69c17905471c17`  
		Last Modified: Sat, 20 Jan 2024 01:12:56 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008b2d772c3a948d4df40d356889da3f2897ec5683cf4d915bbeaa39e77e5569`  
		Last Modified: Sat, 20 Jan 2024 01:13:00 GMT  
		Size: 16.5 MB (16511402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8eb6f5b8d1f7edcd2192c4b53ef77c45f5aa9394882cce085f94c01d1dd41f4`  
		Last Modified: Sat, 20 Jan 2024 01:12:56 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00b2bf544e63bb6f9393a148c44e429aff8e08dc5d96205407ec74d1a1ebce8`  
		Last Modified: Sat, 20 Jan 2024 01:12:56 GMT  
		Size: 19.1 KB (19099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a864294feaea7d35b70eadc2d14c252334fa34ea619996e78d43994205860e`  
		Last Modified: Sat, 20 Jan 2024 10:39:37 GMT  
		Size: 18.9 MB (18938865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab77a45d2a0a3ef5e67aee93cccced243b00c92a598f7e54a9c61979cb7066e`  
		Last Modified: Sat, 20 Jan 2024 10:39:37 GMT  
		Size: 8.8 MB (8833493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2900acc891bced8cb5ee3106ef7d22a90353852546b5e910042bceec15ba49`  
		Last Modified: Sat, 20 Jan 2024 10:39:37 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011dc815288a70365b9016b954760480faab1c0086f665961f1eb815c65aa669`  
		Last Modified: Sat, 20 Jan 2024 10:39:38 GMT  
		Size: 1.5 MB (1521680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b67edf27c2b534d2f7ef9dbbd54bc0e002524b92164f25c26e227021219af0`  
		Last Modified: Sat, 20 Jan 2024 10:39:38 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:386e233c36c0fda781bc870c8a27eeeb173c1baaf68150200171863e84ef0031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb64a123edc56af7555db69c53b20ffe486cb9ba877457df399be0785a62526`

```dockerfile
```

-	Layers:
	-	`sha256:70eed104c39eb234d3b2eb0d9f6c79048c3e4e194cc14d4b9dd782420efdfa6f`  
		Last Modified: Sat, 20 Jan 2024 10:39:36 GMT  
		Size: 1.2 MB (1177747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a752edcf95c38824aa85645eb009f410099c1d63719e3defa20db4b1538f2b1`  
		Last Modified: Sat, 20 Jan 2024 10:39:36 GMT  
		Size: 43.6 KB (43615 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:b55ea5d5b148cfe83c9042f1c9a0e33368aa5732281862450bc02dd8af900786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66919074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa01ecd3dfd58c3cf22203b680aa114d4236c3ec9d4d9bd29cd66cad5186feb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f072bab4d3b766550992c322a39fcd900b329ffbe17cdcb1a7d74010688b23ec`  
		Last Modified: Sat, 27 Jan 2024 08:40:23 GMT  
		Size: 2.8 MB (2815760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537d23c253bc777c8630b1470aee1d7857122cbdf09144b5cb061bde634e0fbd`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65cde09541f81b6406c9aa0f33cd98ae9716bc8c625290248755e374475bda3`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7635cf7aef4c63fed820cf1a7d4016022d00a0480ceb121fb03561da21ed4c16`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 12.1 MB (12096388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdb20c879b0f1f0e303192e729f69ee98706f083dd82eb93e38de241a74bed`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca8c07d82d94433449f272d50bfece8b21f71c12f2ee66dd71164eefec84b4e`  
		Last Modified: Sat, 27 Jan 2024 08:42:46 GMT  
		Size: 16.8 MB (16849949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f222cd71d006262f80acfacfce2e81fb093fb75fb870d66ae450d25c29a4c`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4112464cb9330a0ede0e74206008fc6190bf801a305dba1edc1ce3d00d60e8`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 19.1 KB (19084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2ef5e5cbf8f857191d4a8a37c88c2af9939fffea4acc0a1ca489f70734bd51`  
		Last Modified: Sat, 27 Jan 2024 23:32:07 GMT  
		Size: 20.8 MB (20791834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4a24de8fee0c43c1df54b0b137bf7bc29c92858a4664a1732d5aba5848d078`  
		Last Modified: Sat, 27 Jan 2024 23:32:08 GMT  
		Size: 9.5 MB (9471385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64450a960552fc5a069391ee64471ca6f2dd42c42a729f988b99974826fb6a5`  
		Last Modified: Sat, 27 Jan 2024 23:32:07 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6886751524783ce2bc6097953b100f510214017f6ba99b111d043bcb19d5cf`  
		Last Modified: Sat, 27 Jan 2024 23:32:08 GMT  
		Size: 1.5 MB (1521637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ed19a9b787e1ee21883006f712a550314609fff4f3894da6b154e9feea2578`  
		Last Modified: Sat, 27 Jan 2024 23:32:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:6c41e1c41c9c824baa63785fa16e8e92cc98cf988ab839113711f643aee1c432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b01d701f3c82fe41ca6bceb78ec13bd5ec0297bc8ad61a5fcf252ac60f7bf66`

```dockerfile
```

-	Layers:
	-	`sha256:3fccfe9b3f344ff3d7e61e2a5507e8a71ec1a5b6941a8de4eead7a7d063aee35`  
		Last Modified: Sat, 27 Jan 2024 23:32:06 GMT  
		Size: 1.2 MB (1177704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4583396d3769ac38f5aa2ec97a829cf005345e9928ff2bddd85014fef5a83849`  
		Last Modified: Sat, 27 Jan 2024 23:32:06 GMT  
		Size: 43.5 KB (43479 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:318f6b496349f874909af4716749c946708fed1f57ad6164c4bed9692ebe20b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88dbd60514046a1d3d5998bb4c4a63b32171be16158858b4b15791315ed1cf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91a7316d2e2098b1a91882947964b19bab201421576e249c440063e956bcab`  
		Last Modified: Sat, 27 Jan 2024 06:46:12 GMT  
		Size: 2.8 MB (2825332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a5caaf92a60154c94967702a2fdee5954dec8352f776f8abc87659c4de67f6`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d170158e1d1cffac62a145eb90dbbfd417840d1e2a9a4ae707cafa0bcc2781`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b705d96a822720c651828184408f1a6c9eea23d8197c63f104bccb6e1d73ba73`  
		Last Modified: Sat, 27 Jan 2024 06:49:03 GMT  
		Size: 12.1 MB (12096383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bce88821860841ad9fb8f2aa35e55484bf761143949eab88642252b79cad41`  
		Last Modified: Sat, 27 Jan 2024 06:49:02 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c83f479e124cd0515c82e6eaefeaf99a0e142b30a481faad6f9c084545bcf96`  
		Last Modified: Sat, 27 Jan 2024 06:49:07 GMT  
		Size: 17.3 MB (17317778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4359e1309d7fabd9a5655bb8ec6a7f94c66e0f03081fb628a60ecabacf6bf267`  
		Last Modified: Sat, 27 Jan 2024 06:49:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4030d42d2f2fe2ef5d4de44431e2884ed502ce20380acad6dc9e36b17277c2ed`  
		Last Modified: Sat, 27 Jan 2024 06:49:01 GMT  
		Size: 19.3 KB (19296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5a25ae01020b7aed9ec2557e16deecdf625ef61e8040e532377fdfa978d55`  
		Last Modified: Sat, 27 Jan 2024 07:54:27 GMT  
		Size: 20.2 MB (20160634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f412bb7315a85b01edde1843ab6993fef80b6b7f3cedf58d359c8141ed4e0b9`  
		Last Modified: Sat, 27 Jan 2024 07:54:28 GMT  
		Size: 10.0 MB (10022341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216aadaf08754461e7f623403efc0a5e040eb9e761e40f79206cd2b437008d64`  
		Last Modified: Sat, 27 Jan 2024 07:54:27 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c457c1cc95c2a365d828a1a22448e79c94254dc690a0b2175804a58e37d2b81f`  
		Last Modified: Sat, 27 Jan 2024 07:54:28 GMT  
		Size: 1.5 MB (1521682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9b1dd8499cb337ee66704da1af6c9b349789d48fba0ac7ab87a2e2ecbb573c`  
		Last Modified: Sat, 27 Jan 2024 07:54:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:2f3c22ac251e280ee8907d264080c64f6cd091b8bda014850fa8739e6e6adda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676027a6b95761aaac7ff01e560e3849b838edb1ec918a5e9f86deb994936ba5`

```dockerfile
```

-	Layers:
	-	`sha256:8d5a94d32e39b39a7cc3104dc3a81e7d2caf0d188f5ebd48db43105a337fab23`  
		Last Modified: Sat, 27 Jan 2024 07:54:26 GMT  
		Size: 1.2 MB (1177640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66504ac670000052f9e82c7ec6eac7b9aace395d2fdd200d953feac654023b69`  
		Last Modified: Sat, 27 Jan 2024 07:54:26 GMT  
		Size: 43.4 KB (43408 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:3dcab5d52871f463f2f9b4b5790eb7041d0fe7cba845e1dace9b0724c1f817b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68882812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9010d476c28c80c9497a0e213f037d5917b9eec1d8d8d2ad0583a99aa70427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8953adc2ed89719cf332d6841a33f5396f09790ebe287db3934fd2327d14b7`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 2.8 MB (2842838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a412c6f832e805dac7f8f5eb85b03e9340bde010929c469a7aa203611edf867d`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ad5c29bf6c410c283dc6e7c4619fb7570382a7860ef5d8b6a00e3228ea8a03`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dfc65a6989d02faf8ba64268e70055439b4184c1af31338fcc69df9aa4f4b4`  
		Last Modified: Sat, 27 Jan 2024 04:24:19 GMT  
		Size: 12.1 MB (12096378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc874be9fcdd85b468fdcd00a7ac26557a1dfa6ce3d214db4870df31d7669dd`  
		Last Modified: Sat, 27 Jan 2024 04:24:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6043fd41cd539479ffa1a2d2786dcd75badf97ae8878ae956efbb60e52127e`  
		Last Modified: Sat, 27 Jan 2024 04:24:21 GMT  
		Size: 17.7 MB (17722638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d44f059140360355359eb71b956c157a7cd7d12cfdd6f61502c2b696c1e1981`  
		Last Modified: Sat, 27 Jan 2024 04:24:18 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dadda073d70374dcd89ce2c76b332dfc2f1bef2cc0c603b559b3ce5a1c8835c`  
		Last Modified: Sat, 27 Jan 2024 04:24:18 GMT  
		Size: 19.1 KB (19108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3f3245b37c8550e18a9e2af04bb935177364bd5c49a2225663f704f66ee30`  
		Last Modified: Tue, 30 Jan 2024 03:57:20 GMT  
		Size: 21.3 MB (21345747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13f9161d6bb638394908de163ff5696dde4ae71642ac367a57fcc48ab07984`  
		Last Modified: Tue, 30 Jan 2024 03:57:21 GMT  
		Size: 10.0 MB (9970714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2b9d7efb078455464ea21d28b33e9306da6aa94280af7eddc21507d35df9a`  
		Last Modified: Tue, 30 Jan 2024 03:57:20 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3279f6b8da934dc8df20d5912f1dfb20865fa63255733f50f45104b157dc627`  
		Last Modified: Tue, 30 Jan 2024 03:57:21 GMT  
		Size: 1.5 MB (1521705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ee0e68ca2dc1ab9ca08150c35ba0c41cebf24889f965fad8edcbf1d6d0e5f6`  
		Last Modified: Tue, 30 Jan 2024 03:57:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:bf7dea51bc6cd2c891932962c98360cee82ae0e15467ab6f71e64a2160ccf242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1219638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eebc55192b75fa840b6c2b3fdce97b101d266ac03ed5a723b55a1d64954a460`

```dockerfile
```

-	Layers:
	-	`sha256:b0d6acb7fdc364cb945039c1eb1f113701b3bd50c2b969127fa7c999cf4d5a83`  
		Last Modified: Tue, 30 Jan 2024 03:57:19 GMT  
		Size: 1.2 MB (1176107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994a633c7f86ebcba11ed6de698ed91483e6ce21b6c0765eb850d1a103fca4e1`  
		Last Modified: Tue, 30 Jan 2024 03:57:19 GMT  
		Size: 43.5 KB (43531 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:a7725d7172b162683029a1539c69493398e2929bf2647ea95f7ae726980b4826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68793278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c030246b0b34449e6d07a57c8fe989f5a3a57e2be712356543c6a97b4a7b0a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["/bin/sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Oct 2023 13:03:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_VERSION=8.2.15
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 Oct 2023 13:03:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["php" "-a"]
# Wed, 25 Oct 2023 13:03:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
WORKDIR /var/www/html
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Wed, 25 Oct 2023 13:03:13 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
VOLUME [/var/www/html]
# Wed, 25 Oct 2023 13:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Oct 2023 13:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 13:03:13 GMT
USER www-data
# Wed, 25 Oct 2023 13:03:13 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6de5ae65e656b2b4fa74ec7767361eaadc5cd5fe084c14430793caa205b914`  
		Last Modified: Sat, 27 Jan 2024 13:01:18 GMT  
		Size: 2.9 MB (2940559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ae336f1db4cf8874ad7a1c11fdd671f8cfec2f2870323c9d69be5c95f4dc84`  
		Last Modified: Sat, 27 Jan 2024 13:01:17 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641172590360f4af57f25f7e5069c42671cce55bb70bee9d82d9b5fb865e3edb`  
		Last Modified: Sat, 27 Jan 2024 13:01:17 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462cee53e581fac0e8347d52eed10b734f2a96ee657bf3cc72d33a361e73044`  
		Last Modified: Sat, 27 Jan 2024 13:03:39 GMT  
		Size: 12.1 MB (12096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae86ccd47b275d52ff8c597ac07ba00821d6a49f6a160672da08626ffb3e4ee`  
		Last Modified: Sat, 27 Jan 2024 13:03:38 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decf1c0e591c19056dff276a97fbc2d1067ba86c9c5beeca31457a493f542fc8`  
		Last Modified: Sat, 27 Jan 2024 13:03:43 GMT  
		Size: 16.6 MB (16619541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b7a63bcf5181c2a6d13080984708d4b989c32db8147e4dbfb161ba1e450f2e`  
		Last Modified: Sat, 27 Jan 2024 13:03:38 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e56b595a4ceb808930eedbeecbe23db7374b8ef396c4d89422c2223423e8800`  
		Last Modified: Sat, 27 Jan 2024 13:03:38 GMT  
		Size: 19.1 KB (19099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2bdc4d2cfd5c12f9f7c7fa2a2b3865ec8da03a931a1503653ffba895703c22`  
		Last Modified: Sun, 28 Jan 2024 21:21:45 GMT  
		Size: 22.4 MB (22415503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3387e13905ecb0869dd410dd72fcfc7b41248eeadb48976e6e402f4bb84464`  
		Last Modified: Sun, 28 Jan 2024 21:21:46 GMT  
		Size: 9.9 MB (9932514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cc404dbc8c37977c14b7db95c5ec9be2ac11ad79754f4cec8fc8ad4d56d3a8`  
		Last Modified: Sun, 28 Jan 2024 21:21:45 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419103ec86166b516a1aa17a66b48ab4f7783ade879c4a9a7cc7930441297ce`  
		Last Modified: Sun, 28 Jan 2024 21:21:46 GMT  
		Size: 1.5 MB (1521714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab744f6f8b998d0719793265107355e2fc71891d4650e54fbd7e4f056eb426`  
		Last Modified: Sun, 28 Jan 2024 21:21:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:7c5ce7e9d18162eb2c1796be7e9756eb3168beba28664bcda62a9c104b910136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1219510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eff2900e9d58b9bfbe2b692bdc9cab4745f95a80979b9984777b2d124c7edb`

```dockerfile
```

-	Layers:
	-	`sha256:467d4f8ea20b0bcca5f543d278d486ed8556296802bf7db31be2dd9b0227a686`  
		Last Modified: Sun, 28 Jan 2024 21:21:45 GMT  
		Size: 1.2 MB (1176049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b40677831d27554f354898a6e7bf737d61582aaa6740bef0b419ee0e533fc38`  
		Last Modified: Sun, 28 Jan 2024 21:21:44 GMT  
		Size: 43.5 KB (43461 bytes)  
		MIME: application/vnd.in-toto+json
