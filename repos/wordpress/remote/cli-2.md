## `wordpress:cli-2`

```console
$ docker pull wordpress@sha256:78619fa37a14e7b7fb1344daac7e6ec7790852b2caed413d93927619d70e7625
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

### `wordpress:cli-2` - linux; amd64

```console
$ docker pull wordpress@sha256:abbb6149afcfd07ceb9e8ee08d8c9d6259f58a542e4f5196c6dd1868eeca96d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67093070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e8592177ed65b1dea80990ccb7983b735a85117edcc7b4f83ece10af8cd22c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99979baa6760dc40a927f812328a1431e3870d0f166b035365166ef2cf8d4`  
		Last Modified: Tue, 12 Dec 2023 23:24:24 GMT  
		Size: 2.8 MB (2755737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47536423e0797b82f7a737a4efeb29297c96a33e8662ddcd121d728a01eac477`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6d4fc569fcdbdb835c5ee3607367e6ba4779809c0fad97de75045144220f8`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2014613d03d8fe8c5fcb9247e745c45be8a1adc3fcd3188d3d45b07004d61992`  
		Last Modified: Tue, 12 Dec 2023 23:31:39 GMT  
		Size: 12.1 MB (12090156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af6c37b7e867bdbc0acd886998dc079cfa438f1d303751f4ce00674cbce9f5c`  
		Last Modified: Tue, 12 Dec 2023 23:31:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7926b59062ab2065d2a28b55496e61bc0931f4ccec188d86adca8d4710ed1774`  
		Last Modified: Sat, 16 Dec 2023 06:51:24 GMT  
		Size: 16.9 MB (16904612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cfee82d2911d1dc4c02aeefdadf5e6ad3a2eb73090fe56ba8c26f7e965f74d`  
		Last Modified: Sat, 16 Dec 2023 06:51:21 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf6a35fce595e85c3d64cfa084186b3046998aef530ad018f04850d50b66616`  
		Last Modified: Sat, 16 Dec 2023 06:51:21 GMT  
		Size: 19.3 KB (19288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a441c9e110164ecb22e4c57819078b3ded31de266a4829c9b86fde85bf6c07f`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 20.5 MB (20497380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709d91ae54cbb7b56100132aadde5eea04796ee10e98c27c68bf566014e65169`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 9.9 MB (9890370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab63cd424e5b9253c0f260fc438e1d55a6e196fc4fb7a6a4c7fb736158314f8`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c1d5920653622451112d8f413e443a1516b72e565a7cf92c85152af2ab5245`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 1.5 MB (1521718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed456384bb29591763690ae63cd444a6acf2a8601c949580baac4b78f3a6cb`  
		Last Modified: Sat, 16 Dec 2023 10:50:34 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:721e7e5ea59bb63dbead84ed3008dbcc3e2eb7393e890bfe8eb72bf45e74c456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1220203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65aa90b58b2c91a2fcb7cdefcd8a5bd72a7a2d283da2afe5c55929fcc4b53a3c`

```dockerfile
```

-	Layers:
	-	`sha256:a9db496cf5eb431d7056a713fe4de090a86b09d75c066f19198d84967957c55c`  
		Last Modified: Sat, 16 Dec 2023 10:50:32 GMT  
		Size: 1.2 MB (1176742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506b642f5f4d0772ace34113b20cc74ea7f2fb47b5a83f19321d4b5c65998b28`  
		Last Modified: Sat, 16 Dec 2023 10:50:31 GMT  
		Size: 43.5 KB (43461 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:31ff04066b755c2695dfddfe906ffa4c5a83665089fba08389123c8e1443f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63598472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2551e7db94e7cb2f81a1841590bf8fef12b366df05e301ec85e4937a6f2db398`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6157a5053a6ba5646a1361153760014335e77813c8792b60d226dedefbb229`  
		Last Modified: Tue, 12 Dec 2023 22:10:24 GMT  
		Size: 2.8 MB (2761045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682a06d9f91bef66466bcb1b37715dc344282ac9f062ffff8405cf448d71f51`  
		Last Modified: Tue, 12 Dec 2023 22:10:23 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982a61382f7fcec3d428935d516ac99bf603d105e72ebe0c2952b860f329675f`  
		Last Modified: Tue, 12 Dec 2023 22:10:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cfc74e071164015a40af0336b51789ffe5d9d7942ee6cb08d3d6d3d7f885e3`  
		Last Modified: Tue, 12 Dec 2023 22:16:29 GMT  
		Size: 12.1 MB (12090177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a98bf0644268ec323c4c4116f61ddd5bacd0f008ba928386585df253bf0956`  
		Last Modified: Tue, 12 Dec 2023 22:16:28 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457aa82d530c03dd6e8fbc719149c9a571caf0b59c8e8943069ce8c62931b0a3`  
		Last Modified: Sat, 16 Dec 2023 03:37:34 GMT  
		Size: 15.4 MB (15439814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a673108e37cddec8571e0e47404dfc0d6b2c6b69140bbe71fe2b646ba01842`  
		Last Modified: Sat, 16 Dec 2023 03:37:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1caa5d2de89fb35c3de7ed108da7979548eefa8e821794312c20361d3b532c`  
		Last Modified: Sat, 16 Dec 2023 03:37:31 GMT  
		Size: 19.1 KB (19126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989c03678ac7f62552dc528a290191330fb5f2957b451f9a0a0f22006a4a021`  
		Last Modified: Sat, 16 Dec 2023 05:25:24 GMT  
		Size: 19.4 MB (19445796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b63d538733a511d1279f2b25e3bdeb0bae61040a672020d0a328d0df280cf1`  
		Last Modified: Sat, 16 Dec 2023 05:25:24 GMT  
		Size: 9.2 MB (9150324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e88935f80cad1a2a83b7a9320f6310c920ddffeb997810f2065f65532c2b88`  
		Last Modified: Sat, 16 Dec 2023 05:25:24 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e807b6e436f21c2c337548942e133c659c34c96ae7edebe52ac44d4556cb8071`  
		Last Modified: Sat, 16 Dec 2023 05:25:25 GMT  
		Size: 1.5 MB (1521713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164c0426d7772e06aa02ade6cfa2b901bd1bd2f43af21cec2af20cf8f30cc5`  
		Last Modified: Sat, 16 Dec 2023 05:25:25 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:c3f04c3b2985b2c3acae544cf7a583879b70a63a24d5d3d49f2071f9e8a4d2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49523ed209540c44744ec0d848633c520551ccbb3614204f17d2747615c9f249`

```dockerfile
```

-	Layers:
	-	`sha256:8259fb251e9c353a792705bab3132add16673109b815eb16afe5d67c1e40fce9`  
		Last Modified: Sat, 16 Dec 2023 05:25:23 GMT  
		Size: 43.4 KB (43400 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:3406fe292224b0569d35501cf2a06495be27b688c9ae898c5ce7f30fec7a8791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61376873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84b92f19200fdb5572f108aa996021e13db0353839b622c774331281c86cdc6`
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:0c65211b61938a0940051b6ce59ad29ca8a7200357f40ad9452e6ae7d914b913`  
		Last Modified: Tue, 12 Dec 2023 22:43:38 GMT  
		Size: 12.1 MB (12090170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1b3dc38d0ffe5184ffad35d36c235136c92c4712d11fe66e6428c25951a1b0`  
		Last Modified: Tue, 12 Dec 2023 22:43:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a08f87c3a71cf8940d8fefc2a209d42d974b2f43375fcbf511c78220e14e189`  
		Last Modified: Sat, 16 Dec 2023 06:22:38 GMT  
		Size: 14.4 MB (14443870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efa67b247ca58c28635bf8e48a42416c169fbedeebc7165b64f4bc7f64836b`  
		Last Modified: Sat, 16 Dec 2023 06:22:35 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2acb9b86a307489682a09e167842c513824d7add152f74d475f4baa84f254`  
		Last Modified: Sat, 16 Dec 2023 06:22:35 GMT  
		Size: 19.1 KB (19104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf3d02b5fd372e5336dc0e025a743501778d1b455725ae69d0f761030003dc0`  
		Last Modified: Sat, 16 Dec 2023 11:38:17 GMT  
		Size: 18.9 MB (18938790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd6a6baaeb828e202146977b144a1bbcbafba0d897276bd3bd5effdabd67dca`  
		Last Modified: Sat, 16 Dec 2023 11:38:18 GMT  
		Size: 8.8 MB (8830557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32696db14f267b663d93abde6026baae26064c6531e24ea49af1c116e2fb1ec5`  
		Last Modified: Sat, 16 Dec 2023 11:38:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56363159ec339f3500b703ff1e1be9d53f064333f25db3b6efbcb30489367239`  
		Last Modified: Sat, 16 Dec 2023 11:38:18 GMT  
		Size: 1.5 MB (1521690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330c4af095ed18fe5e074a511c9e395fd73a2d0f6c155dfe83b1e2bfd0216a6d`  
		Last Modified: Sat, 16 Dec 2023 11:38:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:6d7681f96e053f9abd0700fac0e4e360fd2e0ffce21d36ad87e4e3feba56f7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1220425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc32c94c6ad17dfe44e6cc7e448131a91a4099bedd6ca9e7bfa65b794ab6217`

```dockerfile
```

-	Layers:
	-	`sha256:ded88f8181d7ce0deb39b21c4aea98280642e7ff9c15df522c24222c4ea1a8aa`  
		Last Modified: Sat, 16 Dec 2023 11:38:16 GMT  
		Size: 1.2 MB (1176810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bbfe76f13fc526161342925acb955fc02c9a353e3f48fcd42a64544e0308959`  
		Last Modified: Sat, 16 Dec 2023 11:38:16 GMT  
		Size: 43.6 KB (43615 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:8a71e2e9b0bea5a13436c0e1361afc5ca4af832a2c9fe9b2cdececb58cf79094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66952588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcaf547d56dd2d37eeb81a0f398280b00c51f33256608e182ec70275a0dfa292`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a19b0853c69aaf4e0a33f42601f1bddea728304bef39e2fc08f66f3d518576`  
		Last Modified: Tue, 12 Dec 2023 23:00:29 GMT  
		Size: 2.8 MB (2810204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ba87116831a71587816ab8564d1a2b7137e1163524eb7e5abf40966e6882c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a9508fcdd73dc8c678f841adc3269e9919da38f14917ddaa2162b636d4661c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371cc9613e96a0b678d6005da8aec79b82e9039eb064ffa128145d90d4ca2945`  
		Last Modified: Tue, 12 Dec 2023 23:07:39 GMT  
		Size: 12.1 MB (12090159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edcfe1e56d30b58ed518948af0662b3b60bbaf92e1ab9f1af292c0f4a5312d1`  
		Last Modified: Tue, 12 Dec 2023 23:07:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47fe5ff29e7df2a5cc18f62ae71a2784438c189cf939076851f809d44696a1`  
		Last Modified: Sat, 16 Dec 2023 06:08:51 GMT  
		Size: 16.9 MB (16899974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb20976c08b4f21fc85aa5120e623527d13efee824607c1f593e535754cbfc`  
		Last Modified: Sat, 16 Dec 2023 06:08:49 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92e105ad21df901919175d6cc323b8f0d46161853ea7a4afc7b92aadd7d2cdd`  
		Last Modified: Sat, 16 Dec 2023 06:08:49 GMT  
		Size: 19.1 KB (19079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b8f414bf75011c36cde8aff06f5fc45a99cff55209b6e643dc2d440113986`  
		Last Modified: Sat, 16 Dec 2023 22:17:02 GMT  
		Size: 20.8 MB (20792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188f981f8f7abc2e88edcfbb5a67fc863dff27bcf92cec88ddb22bb8a223e54`  
		Last Modified: Sat, 16 Dec 2023 22:17:03 GMT  
		Size: 9.5 MB (9466255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a335cc4970b4fc791a4143c29c58362ae0ca8ceed6c0b0519beba6ec30eacd96`  
		Last Modified: Sat, 16 Dec 2023 22:17:02 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250356268148b5172bbcaa19ee57eb5954070ce8960497dfcfab6a831b2b7a01`  
		Last Modified: Sat, 16 Dec 2023 22:17:04 GMT  
		Size: 1.5 MB (1521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf847a80ff8e79f398cf82de47908a4a4804ebad234abdf10369416a3061859`  
		Last Modified: Sat, 16 Dec 2023 22:17:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:f56206417e63ead32b6e6c95ea7d3f1efba09f556126bcfb2a4cbdafe860e248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1220240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95d399e183cf3b7fb3233de994c4697feb65a2ba2039d1382864250b3ac2292`

```dockerfile
```

-	Layers:
	-	`sha256:1173dd7f829db2c55eaf45808fafc3f495debe11bf8c801d714c9fa26650fd93`  
		Last Modified: Sat, 16 Dec 2023 22:17:02 GMT  
		Size: 1.2 MB (1176761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c46c3657f613fd2efe9999d0c53735707d26ff354937a3c00962614e9959cf`  
		Last Modified: Sat, 16 Dec 2023 22:17:01 GMT  
		Size: 43.5 KB (43479 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; 386

```console
$ docker pull wordpress@sha256:a3d6706deebfc5d6b9db758e2e45886a8d95200bd3c3e92102a7d895e0fa6ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67249072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb4cf44741ad29bdaed6bfe1faf2e1aac5c72b8990009f8d32bd4dfd5235cae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35c853c51aa63c9f21d6c91fa6948b8160ed6a90764a48e7b1891c38e016590`  
		Last Modified: Wed, 13 Dec 2023 00:34:22 GMT  
		Size: 2.8 MB (2820917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6af7fb9ea0ea850c653027fa7b1b18f1d4c405aade35df3c3ec2151bb8251f`  
		Last Modified: Wed, 13 Dec 2023 00:34:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233674231d3f63e2099e1d4253bf67fd488ef3d4fcd72e3e741ffb7a41f385e`  
		Last Modified: Wed, 13 Dec 2023 00:34:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e9acdb959f9ba883235e2640f8488a98ecc65cf8183d7232d24d0f695cdd8`  
		Last Modified: Wed, 13 Dec 2023 00:42:21 GMT  
		Size: 12.1 MB (12090164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa95acc71a1a9c941ace8a2567783b36323fa4c5edfcfa733c042472876a216`  
		Last Modified: Wed, 13 Dec 2023 00:42:20 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b3c29a3d27ee105aebba809b1b78d3f1e9333880ea31c87d6a3ff2aeaa42f6`  
		Last Modified: Sat, 16 Dec 2023 10:16:50 GMT  
		Size: 17.4 MB (17374704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094cea7d500f1c09da647db5e060c934905292c33cd6642e9a99233f997fa398`  
		Last Modified: Sat, 16 Dec 2023 10:16:45 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d95c65d35fa24c69b965365f6da79cdd76e5cb9c888f8961949e405e69ef53`  
		Last Modified: Sat, 16 Dec 2023 10:16:45 GMT  
		Size: 19.3 KB (19292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25d39616be090006a7b7b42dbabb38bddbb9f38ec11a304c72dda0ca88981ab`  
		Last Modified: Sat, 16 Dec 2023 21:50:33 GMT  
		Size: 20.2 MB (20159218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b21ba40d984b11b778d7c25aabf88c803c4fb20793cb4f02624a92ce381abff`  
		Last Modified: Sat, 16 Dec 2023 21:50:34 GMT  
		Size: 10.0 MB (10013648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c853d282bc424ff88cdb501981d5f4c3fa13bdf98a31c568702cca39d813e`  
		Last Modified: Sat, 16 Dec 2023 21:50:33 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9341bf2026fae76200375e09f16c4703fb5a4a62950c16d9ea181f6b846bf`  
		Last Modified: Sat, 16 Dec 2023 21:50:34 GMT  
		Size: 1.5 MB (1521685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4bcdcfc3c118b555f570ad644d646dfb8f55e5e72f363421874442877d68e`  
		Last Modified: Sat, 16 Dec 2023 21:50:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:a57e535a942f5029eea5a192deda88211e36a4a07aa919fb1d9ee6d929ff4273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 KB (43191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4311ed817d79ec60ee09fc74006f63031cac7a7d2a2f3e4069b86177b1ce85`

```dockerfile
```

-	Layers:
	-	`sha256:737a40afaaf6ae606cd99b84ac45e272bb94ad43f7c8105344ae6ddf898048e8`  
		Last Modified: Sat, 16 Dec 2023 21:50:32 GMT  
		Size: 43.2 KB (43191 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:fe3c8e1cbdc7fde6191948bb54fba9e43e0ee5b09ec63a95579f54116c7dafc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68914030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891d85ba94711603b278fb5c39e686e37b02a65c665638323b5a7a4b74d74dcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89935d2f947cbd3585545f82639d347027ef82fbbf413f8684101953ea74bd6`  
		Last Modified: Tue, 12 Dec 2023 22:41:51 GMT  
		Size: 2.8 MB (2838539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208bea042d5cdcbe6436f88d2f7ea51b03a91df91ae099118f57b644b87bdb2`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb83a14858379fd485cb474c02417cd209b148b775365e9bae3ab90f5fe798`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeffac13ed5bef6d24f5ba054e8716cc8c92493af87d27d6df2c9583da018a1d`  
		Last Modified: Tue, 12 Dec 2023 22:49:56 GMT  
		Size: 12.1 MB (12090172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f411bd600c78bd58a0d95fe29fecf63567ddb6a794b99a4cafe4b05a1b4a0b60`  
		Last Modified: Tue, 12 Dec 2023 22:49:55 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfae359d48144950e212bb4a82aff46df4b30ce5a29876d233fb1bd073c5a492`  
		Last Modified: Sat, 16 Dec 2023 06:18:16 GMT  
		Size: 17.8 MB (17779668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ebcb199d58078b2ee2395c8095e35f292274fae3cbf4f138fa48877cdad075`  
		Last Modified: Sat, 16 Dec 2023 06:18:13 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd9bc01b932c6b21e4d304232821d18dae5c3c2b39e4c88926875318cd4c0ce`  
		Last Modified: Sat, 16 Dec 2023 06:18:13 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac5b74e1c91873f98ddfda9d3ec0798189e73e5c181e8a64cbc030c3b397f95`  
		Last Modified: Sat, 16 Dec 2023 16:41:39 GMT  
		Size: 21.3 MB (21340984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3490b5ea39ec36963a4bbfc352c2b9297c7db502e7a27cb8d3bb46bb178f61b2`  
		Last Modified: Sat, 16 Dec 2023 16:41:39 GMT  
		Size: 10.0 MB (9960303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50219308807867b2e92098ae4a7490ba8ec22c149040b5415d8cd2abda0121`  
		Last Modified: Sat, 16 Dec 2023 16:41:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa67da0392846413d107feb2409b3873a35104239b810fb464df106837a32dd`  
		Last Modified: Sat, 16 Dec 2023 16:41:40 GMT  
		Size: 1.5 MB (1521687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ccb78fd3453e66adbf6e5fb3462184f1d42278be9785a317ed8143f0948604`  
		Last Modified: Sat, 16 Dec 2023 16:41:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:bc9a902b4b0ec50665775c76ba7b3ffb07c0e993ea72bc4ce115f90923d9a47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1218695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e7b240739ac0f33470a6e329482db239f152d5ecfa9f8d8ccf326a7a28470c`

```dockerfile
```

-	Layers:
	-	`sha256:3fde15673f6f4c346d91629a1af42265bbe94cc82acf3027db980125f3eb2fb6`  
		Last Modified: Sat, 16 Dec 2023 16:41:38 GMT  
		Size: 1.2 MB (1175164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca507442114be881953e079d78f52d2118ad32c9ec754b1d493ead5a8ec44de`  
		Last Modified: Sat, 16 Dec 2023 16:41:37 GMT  
		Size: 43.5 KB (43531 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; s390x

```console
$ docker pull wordpress@sha256:f4ef5050396a420e98719171d546210f5c8d42673fc211da4cebc5f0fbfeb1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68815701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484ed9d52e80aa7c38e1c8e543d3de49c7b1ff01a91097dbc1466530de615c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 25 Oct 2023 13:03:13 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
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
ENV PHP_VERSION=8.2.13
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.13.tar.xz.asc
# Wed, 25 Oct 2023 13:03:13 GMT
ENV PHP_SHA256=2629bba10117bf78912068a230c68a8fd09b7740267bd8ebd3cfce91515d454b
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 Oct 2023 13:03:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 Oct 2023 13:03:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0180a7268e169fa6dd82fc04f9270dbd4fe716cf09b03fc82f84618025bad4`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 2.9 MB (2937974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecaefbf268f4b1e4d9f16c5d67523f3b76e72db0c3fc7a2f3fb6fd7fbdec547`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f0d18e8f1067fcb105dea2ad180f140d138c6d99310025696d1aaa322017db`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf9b7e6a055250d1d84ef17cb540aae3e06ee7b28a00da6108c18b0d2839d2c`  
		Last Modified: Tue, 12 Dec 2023 22:12:20 GMT  
		Size: 12.1 MB (12090173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b12250fc26321f92a34dcfafafe6c4b7945bfe44c9fdb126ad964f2ab4a9`  
		Last Modified: Tue, 12 Dec 2023 22:12:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083718ae6fd17c6298f5f5a54508ea10f8318b2b9ea36c4eab1b28594198f371`  
		Last Modified: Sat, 16 Dec 2023 04:59:55 GMT  
		Size: 16.7 MB (16665506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f61a363ff288b996ec6f3ebba46cc1d29a96afbded3aff44703fed2a990e7`  
		Last Modified: Sat, 16 Dec 2023 04:59:52 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c0999a0bd83006fa66253320d72726a35ff35047ca0935aeb4d13d3c70335`  
		Last Modified: Sat, 16 Dec 2023 04:59:52 GMT  
		Size: 19.1 KB (19103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3b5380f2942081b1f55504adcf525a1d92cd885f480b47ac84bd2c809c9b3`  
		Last Modified: Sat, 16 Dec 2023 11:55:50 GMT  
		Size: 22.4 MB (22407059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2d52cd0c2922db6376fe81b991ad33b1b64bf6b0af14c642c947ce39f34762`  
		Last Modified: Sat, 16 Dec 2023 11:55:51 GMT  
		Size: 9.9 MB (9926522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9851eea507ac624f66b36b6a312a6c16a5d770cbe97b16aed79c2531530f71c`  
		Last Modified: Sat, 16 Dec 2023 11:55:50 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4064ca440f90cee2c7c2024c69aff200c956867efaa644a42b7441b9fd5abc2`  
		Last Modified: Sat, 16 Dec 2023 11:55:51 GMT  
		Size: 1.5 MB (1521703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fa0e1c1f8e46b2ce574bb60b000de647a697ba029b7884ee2d9248b96cc34`  
		Last Modified: Sat, 16 Dec 2023 11:55:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:fec1d7bc0f3afa77826f043c3a7398ddccbbe8a2f9c8e7a39ddef90bc3e5cde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1218567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e505aef2a3f7e78ab55a0b6d39d327288e23aa5c7f3b4ac9065e87e7231b706`

```dockerfile
```

-	Layers:
	-	`sha256:b5bd0876d2c297733d689fcfea9eb255c8ca3baf9e0e93e471f5369780fc3cf9`  
		Last Modified: Sat, 16 Dec 2023 11:55:50 GMT  
		Size: 1.2 MB (1175106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2b9b032e917d3da34b28cb1cc0f8fc9ccb0b80a4754b05fd87ae5ba5d31a18`  
		Last Modified: Sat, 16 Dec 2023 11:55:50 GMT  
		Size: 43.5 KB (43461 bytes)  
		MIME: application/vnd.in-toto+json
