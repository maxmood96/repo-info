## `wordpress:cli-php8.3`

```console
$ docker pull wordpress@sha256:14d4d1176a987cba67427654e73e5f593a7eeaba40bb49f536c051a8fe403479
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

### `wordpress:cli-php8.3` - linux; amd64

```console
$ docker pull wordpress@sha256:6c137233cd89e2fefe4595364b95761b6fd34d881db53673e6fc2ec4c2eae158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67659828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1705424835c7f0e736885abf0a4b22cde24ec77ce3e05e57296f26d6d5f048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 11 Mar 2024 23:23:48 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b8f5633756ac1ff66cd8b50ce912d6973d6c837ac6b1d095a338e82b62c7a9`  
		Last Modified: Thu, 23 May 2024 00:24:15 GMT  
		Size: 3.3 MB (3267774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a3c078331cb090d048b896d0356bba473cec2eef2ea60b28fd417683378300`  
		Last Modified: Thu, 23 May 2024 00:24:14 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140bcc3b043e8d9a36c45a8f4eef10bcce2d2148d5de519bd56574ec436b271`  
		Last Modified: Thu, 23 May 2024 00:24:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f008510e803bb0c80ed92257ed7efaba32526ae0764b79cf42a2e7d768e9eab2`  
		Last Modified: Thu, 23 May 2024 00:24:13 GMT  
		Size: 12.5 MB (12476838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8cee413b7587c0d86c31b50fe1277b4a89eeb8a3572a04a0ca78d0b59ad728`  
		Last Modified: Thu, 23 May 2024 00:24:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8863006f518805ec6c67426bc4436bd11db5af3d886991a0a546f858d427125`  
		Last Modified: Thu, 23 May 2024 00:24:15 GMT  
		Size: 17.2 MB (17209191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901027c54fb253d4fc01a13b86938bfd81aaa10cd94c4f2d77112815595029a`  
		Last Modified: Thu, 23 May 2024 00:24:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d58fa2a6b9dc5cef1d451c499ca62764abc44c70edd2eb97ea265f7c5c4f88`  
		Last Modified: Thu, 23 May 2024 00:24:12 GMT  
		Size: 19.7 KB (19680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff406a2574965a7fd46824e105095ea42f2c811fc26c066919d629ef80b120b`  
		Last Modified: Thu, 23 May 2024 00:52:06 GMT  
		Size: 20.6 MB (20552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef3687c9022cbb955c727897465471f9512d13e163349f7bf5c6291fa71af3`  
		Last Modified: Thu, 23 May 2024 00:52:06 GMT  
		Size: 9.0 MB (8976561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4d711849257ad6a7c5825d4203d1f123c3a91fb9037d999eabafe8af0b4fb`  
		Last Modified: Thu, 23 May 2024 00:52:06 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47c15e2cfe1904f7c6a494f05b03886b0dddde0c57c533d6b3f97aa3ba2c22`  
		Last Modified: Thu, 23 May 2024 00:52:07 GMT  
		Size: 1.5 MB (1529815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af279d60aff60a4b54af0f1fa771300a3194937e6c9d2a97f0c0e868ea05157f`  
		Last Modified: Thu, 23 May 2024 00:52:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:5c15a17aba8e4dac44e7c735c650db9c87f3c307d5bb8a51e280d2c4b851f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1435995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2c203f4ccd973ef2227f53b6937a9e5649b9c66779e5b6a9ec88cd78cd5ec2`

```dockerfile
```

-	Layers:
	-	`sha256:1194a7f2aec33aecf42582ef832e324edff01162cd77448a12cbebd1b0b3748e`  
		Last Modified: Thu, 23 May 2024 00:52:06 GMT  
		Size: 1.4 MB (1391723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a0018cf5bfa6ac18f1d59023e8bb4c3c7783340da823861fd3b68787c7aa4d`  
		Last Modified: Thu, 23 May 2024 00:52:06 GMT  
		Size: 44.3 KB (44272 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:5ccd779b0d389a779bdb425cf9ea351d08530ceb89e7e142f044d42a8156d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2b98651d5656b21d3965efaff2c37d25e630f93e5c4a9746c6d130bed82f8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59be61bd2ba9f18af71b96c422917e0014880c902aa3ccb7f8257383b11b69ac`  
		Last Modified: Sat, 16 Mar 2024 01:01:12 GMT  
		Size: 2.8 MB (2764506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95722804161331c4c8c5fb5c67c2930e7f200746da0b87efc2cc1ca230b2bdf`  
		Last Modified: Sat, 16 Mar 2024 01:01:11 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9405a5b710e6142fb5b24b32edc3d286164167c9a50bc8d571a93dba40d73564`  
		Last Modified: Sat, 16 Mar 2024 01:01:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd082fb9aecc61407c5433f220851fb4a28cac73c81ca4b4261adfaff35f4dd`  
		Last Modified: Fri, 10 May 2024 21:40:42 GMT  
		Size: 12.5 MB (12476752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143d173a472b475dbc2c4f320b4c1c7da02970ac12aa5bdcf022dede4c152b56`  
		Last Modified: Fri, 10 May 2024 21:40:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dedf95487205706bcc1c9b1f0c8341d1421d1ccc750c1008a3fdd168f180a7`  
		Last Modified: Fri, 10 May 2024 21:40:46 GMT  
		Size: 18.0 MB (17976812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d760af5a109d2000b8efa124c89339587a678a61d103b903a23f338cdd01e624`  
		Last Modified: Fri, 10 May 2024 21:40:41 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1bb8b0fe5871d96f0d5256bbd95a1cdabba12d8a73ce1fdd127bde8e3fb661`  
		Last Modified: Fri, 10 May 2024 21:40:41 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eb7edcc06590c0363f065ecd645566ec7fc7c93f30c54a4262adae02bdf133`  
		Last Modified: Fri, 10 May 2024 23:07:21 GMT  
		Size: 19.4 MB (19444859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36af4fab80359d69eee60cb403f434b1f51b45dcb1ff30f6c25104dc56d810c7`  
		Last Modified: Fri, 10 May 2024 23:07:21 GMT  
		Size: 8.6 MB (8629578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0f42fbafde8fa543898bef82621520be9e6b4781eca1f71f3b7ff65f72acd`  
		Last Modified: Fri, 10 May 2024 23:07:20 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129746778ba49e5fe269734418cabb6ab2dcf46fe3619e9bf3963846f641087e`  
		Last Modified: Fri, 10 May 2024 23:07:22 GMT  
		Size: 1.5 MB (1529753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dceb0d244e12a94c17670622d84a450685ca42caf7dbc01998ede71a980325`  
		Last Modified: Fri, 10 May 2024 23:07:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:9041637ad39810da76b96b1376601ab526a6d2bfafb192b5aeb9ff53a1702faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 KB (44185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f639b895c3a7e17a7b2a8eaae15b7befe67f84f72f7486d682c2264466468779`

```dockerfile
```

-	Layers:
	-	`sha256:8e9ac0e24b9b1cb60c2cc0c3c47f596413106364c3ce6ce7028d05291655064a`  
		Last Modified: Fri, 10 May 2024 23:07:19 GMT  
		Size: 44.2 KB (44185 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:d6abdc29f1886f09a61c79c98fe7f144fed2d7ee13c4381135a5c24e7a990c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63629287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8908e4a7197adc05f4acff1acc81b0e0123d8a783425d1b4fded0e9e6a8640eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24a3155a604085efaa4c70bd2859739b6141d4fd0670fa3e15fd67cab1a2154`  
		Last Modified: Sat, 16 Mar 2024 11:00:26 GMT  
		Size: 2.6 MB (2612666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bbcf35c6eddf26fa13dc8c811f2ac147d03bba1af2fa37c43084f218a04ca`  
		Last Modified: Sat, 16 Mar 2024 11:00:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb37d0aeb5ad8612608d36edcbe0f65f4004674effbc82dceac7fda7895b9f1`  
		Last Modified: Sat, 16 Mar 2024 11:00:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b522e5e94cacc3456e93722ce08878762b88706247fa94613a94bd25fc28fc12`  
		Last Modified: Fri, 10 May 2024 22:43:23 GMT  
		Size: 12.5 MB (12476743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404a1899432700ccdc9ed943981592be468943244af5be4a47ec12808071c997`  
		Last Modified: Fri, 10 May 2024 22:43:21 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac3cf441eafd17aa83d0f4c13fe868327ea024625d9e337021f3cd8533d34c3`  
		Last Modified: Fri, 10 May 2024 22:43:25 GMT  
		Size: 16.8 MB (16818833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad63ae54c00e1c8a651d15d2f44e0b42f862cc618e4365d7897467ed1a8728`  
		Last Modified: Fri, 10 May 2024 22:43:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d5d836c8ea22527f0d94956c3d1acb773070d361c1ce6293923d919912c0ba`  
		Last Modified: Fri, 10 May 2024 22:43:22 GMT  
		Size: 19.1 KB (19115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94715ce723bc862e8291dc27731c664fc1f5e942e65369b5046d6114d63afec`  
		Last Modified: Sat, 11 May 2024 01:49:40 GMT  
		Size: 18.9 MB (18938918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acb8c7aaabb85fb8a9113bc2666f1aa274bbf079bbf5a0c1a1d28a39dbd92b2`  
		Last Modified: Sat, 11 May 2024 01:49:41 GMT  
		Size: 8.3 MB (8309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27b4a5421d49eb6351baeddb263e7904fd57cf7877da7de684e988bc0e8034`  
		Last Modified: Sat, 11 May 2024 01:49:40 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b1c957cf7537c5ea8b8e258ed13d79bd1c5b76cb8780f9e3bc4b1d051ac6b7`  
		Last Modified: Sat, 11 May 2024 01:49:41 GMT  
		Size: 1.5 MB (1529743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bafd7e617892b147cc9ba9e59e9bcf680aa1e04c0ed7118c8e004a473a80846`  
		Last Modified: Sat, 11 May 2024 01:49:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:fc4b143c85fa12f38c69bb2d371960f88c1a3cd3e172e696a356774383db07af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1433976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470ed3f60bbde0560e5e946a588fe328d994c44dd5215812ee79db55e1d47cd6`

```dockerfile
```

-	Layers:
	-	`sha256:f2cae670b6e13086ff8ca0ababd1d15c7be3d303d501b24e316930e3616b30bf`  
		Last Modified: Sat, 11 May 2024 01:49:39 GMT  
		Size: 1.4 MB (1389572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32066b99de3c4f538a8418cab9d8d0a3996b92b0bce892462b5767edf27eca2a`  
		Last Modified: Sat, 11 May 2024 01:49:39 GMT  
		Size: 44.4 KB (44404 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0b7189268d583da4884eb8596634dcb5cff7c91ac41fb5bbea71136709fd1bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495263301878a96bdb9abcc09dac8133f4a9c18bbd5683b5cad8f2ad3701791a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 11 Mar 2024 23:23:48 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c1e324da27f4d6ddb1e9a92e83fa99f1c8e29cdcac64a1431bb85a8aa9347`  
		Last Modified: Thu, 23 May 2024 00:08:07 GMT  
		Size: 3.3 MB (3321192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56b82da1737e6e5a929f889995a1e6e4019d71f4a64ab0a1d3d5ec4a3819700`  
		Last Modified: Thu, 23 May 2024 00:08:06 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a70d7a8e6a41c0f3cb0db1f8dac34b60c865b6d79222263d5ada6836d09dc6`  
		Last Modified: Thu, 23 May 2024 00:08:06 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0745c87672ccaa0aa061a16f49fe5cff6fa9db93f82f443e4b519d10bfbb3bf0`  
		Last Modified: Thu, 23 May 2024 00:08:05 GMT  
		Size: 12.5 MB (12476839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1d0543bf402cf78865aedc958610618c3817915d6dd00bf8168229c95e3447`  
		Last Modified: Thu, 23 May 2024 00:08:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0d5281985cc37067ec2158b4c73ff94fe815bed24ec5de1b32c3f96db0eec`  
		Last Modified: Thu, 23 May 2024 00:08:06 GMT  
		Size: 17.2 MB (17181179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a685a482a558898618430ad3876951ef83c3f7750f8cceb8bc88fe4f55cd41`  
		Last Modified: Thu, 23 May 2024 00:08:04 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716b9588c5d1627db0cba5c2192330972ac649f8575e9ac598f0587c6c3272cb`  
		Last Modified: Thu, 23 May 2024 00:08:04 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7eadc166f7aa5593e7ebe912f2f1dbccfdce605341bb2008d769e992a5500`  
		Last Modified: Thu, 23 May 2024 08:40:18 GMT  
		Size: 20.8 MB (20773483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e471887774d815b555ff59ce8d79371155b8af1c8e2c573c4d6a780cda9a04b3`  
		Last Modified: Thu, 23 May 2024 08:40:19 GMT  
		Size: 8.6 MB (8578416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c33fa969524da4a59cc665e9a3f57183b6dc210d0e535c8dd31de30a84404b`  
		Last Modified: Thu, 23 May 2024 08:40:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83002a4c6302412c58dece13af25ca66e39005707a6cbfe98a3870c46c45f03`  
		Last Modified: Thu, 23 May 2024 08:40:19 GMT  
		Size: 1.5 MB (1529779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a879bc05748ca3e76725ac837a9363af230790a56a65dc0be5ee9265cf8e0e7c`  
		Last Modified: Thu, 23 May 2024 08:40:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:2ec7d7dba769cccd61508b28a2a314aa4a394054cb8b2fe9aa315046227f6172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1436017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ee348f745510097ea94a9a0c3c695ff08b438e984539f0fa8c303bc396bc3`

```dockerfile
```

-	Layers:
	-	`sha256:8e948bf49dde6a043ab80c2d94fc843c6e0d3b0fced2f27f2882b7157f973db3`  
		Last Modified: Thu, 23 May 2024 08:40:17 GMT  
		Size: 1.4 MB (1391734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9ae63fef5bf820172db7216c9501ed213013afda0195cb9102906181b2eba5`  
		Last Modified: Thu, 23 May 2024 08:40:17 GMT  
		Size: 44.3 KB (44283 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.3` - linux; 386

```console
$ docker pull wordpress@sha256:d6c8a64f9aacbf3e4f64b3e654e36ac9897e10b89652b052f9bf237c585155b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69809094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdab7dd2ebf0260569f934052fcba6446fb3fcfd7ccaa5c208cdef4dd5b8287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a52b85e4d8e4d0e4048cab06c149fd0b6d64c5a5f04ec3a3f7c0ab4d4a3d8e6`  
		Last Modified: Sat, 16 Mar 2024 04:58:57 GMT  
		Size: 2.8 MB (2825337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00dcc91f58845575e9487816e58609662888d41b2facfcf6128056ee483579`  
		Last Modified: Sat, 16 Mar 2024 04:58:56 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3264601b4fa42c37a2b6f6e47b5c8cb1c963b67ee7e15c2c18d17f2fd035a3fa`  
		Last Modified: Sat, 16 Mar 2024 04:58:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76877571f32313d3ad1bcd7bba165a4d692b4fb60113609b05d981461a5b85dc`  
		Last Modified: Sat, 11 May 2024 00:53:07 GMT  
		Size: 12.5 MB (12476743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b931546770df83ed3ac96545d640e484c5717725f460b13800e21bb5f85efcb7`  
		Last Modified: Sat, 11 May 2024 00:53:06 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1447cee22897c82ec692019674663a7dcb83ba55f1d1e91e85a901bbf02834ab`  
		Last Modified: Sat, 11 May 2024 00:53:11 GMT  
		Size: 20.0 MB (20031230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685ff148a3ebe4e527fd95b0790156ae563dbd33ce14387f7a302f1c2cd615ac`  
		Last Modified: Sat, 11 May 2024 00:53:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133a9a8b70ea81f1c93d37df5bcf01b049f5da5b5472e1c9124935f322eea5c4`  
		Last Modified: Sat, 11 May 2024 00:53:06 GMT  
		Size: 19.3 KB (19306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1f49b0e340d61d673caa2a06f14c85bb906099f22ddfc8ba9de7a2bd82174a`  
		Last Modified: Sat, 11 May 2024 01:54:03 GMT  
		Size: 20.2 MB (20161432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169c1a38010c64b1c0ed004567d6a2d9e435f5a2457eccec57e199549b0b17a3`  
		Last Modified: Sat, 11 May 2024 01:54:04 GMT  
		Size: 9.5 MB (9515896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb3b2e74fceccf240df6a793d47c47c1aaff401cc2ccd4517b3e47e6d9c80c`  
		Last Modified: Sat, 11 May 2024 01:54:03 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd21288682ab5b99fc81bdae821416bc830523e64893a9d3a9e7932bd8fab5c`  
		Last Modified: Sat, 11 May 2024 01:54:04 GMT  
		Size: 1.5 MB (1529730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646ffd7b77e50bbc276067673505b82c4320e42f689cff7bb4c18cf215eebcfe`  
		Last Modified: Sat, 11 May 2024 01:54:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:c7a7e30e8cbdfc9b64751367048be8e0febc316fa83095a2d288239152bc878b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1433756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1b434b548c01146ebfad25b876a67f8e2777ec636079b185a4cfe22e8c9f02`

```dockerfile
```

-	Layers:
	-	`sha256:0e64bf7b3d9bed13ffbb59f8580806dec01aac48216e0833573695cc94bf9e33`  
		Last Modified: Sat, 11 May 2024 01:54:02 GMT  
		Size: 1.4 MB (1389511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed3f8b9d49730b7f4429b99bef228091cdc0d6feabd98752e6b847b8597e014`  
		Last Modified: Sat, 11 May 2024 01:54:02 GMT  
		Size: 44.2 KB (44245 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:77e109a936742aa3d48d3335f416f4dc949d0a4f9e42a0b89b5d9cb7d3ebe7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71534138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcdc610aa61c866f4dbf125057707d32231b2537a8a2bf38df8ec2133922900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351cc51b7233ca6780794a860d1cb9c98abff8e8277d2b87c1fafd5d06239d8`  
		Last Modified: Sat, 16 Mar 2024 06:55:33 GMT  
		Size: 2.8 MB (2842850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83541649479862a60e6e0a63881477379ac3ebccf9b657c4646de7eb1d4dc0f7`  
		Last Modified: Sat, 16 Mar 2024 06:55:32 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b3f7fb8aafed95ce8f9c79f9af65ce6e4439edfd71c1ba169b88443d61e05a`  
		Last Modified: Sat, 16 Mar 2024 06:55:32 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3a8544d0cecb95e9470991d3fedbda61a3afa8ea341c51fcc240c07b5a2f11`  
		Last Modified: Fri, 10 May 2024 23:03:53 GMT  
		Size: 12.5 MB (12476744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7231eb0c6dfc550e6a412df06def17b1d9684ff60fc1f0c6bdc9879fa5c5684c`  
		Last Modified: Fri, 10 May 2024 23:03:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62dc4f97a7dbecdb1738d53ee47d37ab65fffa9a700f808b3d74ea79416590c`  
		Last Modified: Fri, 10 May 2024 23:03:56 GMT  
		Size: 20.5 MB (20517065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae687ef531475af3ca9e7bc8adb39d0ecd62e6dd9d60576183befa4801283ca8`  
		Last Modified: Fri, 10 May 2024 23:03:52 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8e27d3fa4c11a67041d8b6a536768825d93b53a72502d6886fbe094018a53e`  
		Last Modified: Fri, 10 May 2024 23:03:53 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69449bd8cc0869d206e93edca5dd1bd841ba470a5c93464643359408ed6c17a9`  
		Last Modified: Sat, 11 May 2024 03:27:56 GMT  
		Size: 21.3 MB (21346238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b92407299613452010141007f4653c65cc161164bc5e0f0f5348f74c9d9a20`  
		Last Modified: Sat, 11 May 2024 03:27:57 GMT  
		Size: 9.4 MB (9438706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888be03c2be7d9dfe731eac1fbaef7c9a0ea5fe723bbafdd20e565f0b5800523`  
		Last Modified: Sat, 11 May 2024 03:27:56 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e1011a8de0ebbfe6dd968d6117a14e50b90dffb8ff52648ac8fa9dab9e4fb`  
		Last Modified: Sat, 11 May 2024 03:27:57 GMT  
		Size: 1.5 MB (1529724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca73309ecd9f4d9216cc88bf5f3a36610cfd22f146059f38965971db524a7b8`  
		Last Modified: Sat, 11 May 2024 03:27:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:5b1e3dcb1ea794a03c5849a3233444d4a7398ca646287e68d55f8f7d2bbee2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1431943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432c2eb5d29b3e42e66d18ecbfd1d39ecaf3b3e9f81f484d0dde8eea18d2b4f0`

```dockerfile
```

-	Layers:
	-	`sha256:acb1f1d3302ecaaf359de7bda8a89a31e9abc6d4d97da2d7d03d0a18064348c9`  
		Last Modified: Sat, 11 May 2024 03:27:55 GMT  
		Size: 1.4 MB (1387616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1aae7df20ce4dff1cc9593d81e686433b9cb8ffa6aae159ee69f9729cc3ac8`  
		Last Modified: Sat, 11 May 2024 03:27:55 GMT  
		Size: 44.3 KB (44327 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:87bb228c13bfd074915012123b4336ee8f5514c7d6428c2d45af205c27fd483d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69358828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64945da7a62eedfa2dc28f66db418eb4f28fcb84a7cf374fdcd6d7ab54388ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 11 Mar 2024 23:23:48 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.7
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["php" "-a"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_VERSION=2.10.0
# Mon, 11 Mar 2024 23:23:48 GMT
ENV WORDPRESS_CLI_SHA512=c243265be520cd906f6dac767b56bb4e7dae9b6308db32b7e45ed8adbacad97bce987fd69b019d25478f394f0082404a0f44a93416f5e4d943cb32fd08f1feac
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
USER www-data
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36e9ed42d7e633f43d8fa04adfa4b70f99009699e11f68632998351cbbc3fd2`  
		Last Modified: Wed, 22 May 2024 23:36:18 GMT  
		Size: 3.5 MB (3462548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb7be78c0fcdc4c08c1104b13c57c9d6d41ab41b8980ffc2c8675d2e656a31`  
		Last Modified: Wed, 22 May 2024 23:36:17 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed5aec1eb926eb5b478d34912d40483a1a38f7f84e1b30040e03fa9e4a9627`  
		Last Modified: Wed, 22 May 2024 23:36:17 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228310f29287b9e4a54a237bd3f886a9b85000fca8034e29e59acd6c4af8ce77`  
		Last Modified: Wed, 22 May 2024 23:36:17 GMT  
		Size: 12.5 MB (12476847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f98995f9e735aa0c844fbdd1cb87df29dee50a778cc24e465d22d11b446d93`  
		Last Modified: Wed, 22 May 2024 23:36:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f7d5a5c0642f6f9859cb9cacb99c19d638096f8d5a11492154db8a5086b766`  
		Last Modified: Wed, 22 May 2024 23:36:19 GMT  
		Size: 17.0 MB (16961463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145a5703c0fdeefc1041f7af26b73853fe9df7cf7fa44230981120177e22cbde`  
		Last Modified: Wed, 22 May 2024 23:36:16 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4945efe0cdcf141c38dd90536a6c55681886db9d446c20bc28488d694dc85`  
		Last Modified: Wed, 22 May 2024 23:36:16 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284a4ee371f1bde57d8334ed7cafc325689801968210ae0548db9c06e665cdb3`  
		Last Modified: Thu, 23 May 2024 05:33:59 GMT  
		Size: 22.4 MB (22435353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eba13c15523efe85906f43f8d2e9515bd7219bfddd8aeb03caf73953b02068`  
		Last Modified: Thu, 23 May 2024 05:34:00 GMT  
		Size: 9.0 MB (9007945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dac86fe30b332abac0a29c8922fd26c4fbe19e9e94be1fac98a0d175ceb185`  
		Last Modified: Thu, 23 May 2024 05:34:00 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac07ddff3c8a211009b4c33ec015a7ea648ba90a18a979acec8dc6e1352895f`  
		Last Modified: Thu, 23 May 2024 05:34:00 GMT  
		Size: 1.5 MB (1529808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f8c1d65e379bd058251bb4fea1cde3648b5a328df48a64c8a1b235b573b21`  
		Last Modified: Thu, 23 May 2024 05:34:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:da255a6ba2a11744d2c92491bfc782bfec1d6bca7e2902590023f9a80d016e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1434042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84dc0e7f75d4ff4e39782ae0089068cb152f7a8d38784e3237ed1532abb021`

```dockerfile
```

-	Layers:
	-	`sha256:f45635f0f1a6ec3873b6d1d8ab1d9a2be43f24130d3671098f443dbb9b507590`  
		Last Modified: Thu, 23 May 2024 05:33:59 GMT  
		Size: 1.4 MB (1389769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384ad9a29b74c190f8a6cb38be1c0b19e86c9d7a8ab5ce6618d97224168e1f30`  
		Last Modified: Thu, 23 May 2024 05:33:58 GMT  
		Size: 44.3 KB (44273 bytes)  
		MIME: application/vnd.in-toto+json
