## `wordpress:cli-2-php8.2`

```console
$ docker pull wordpress@sha256:f347044c2f89f619dc7af5391530c6f3de1df7a1c3a051300ffd34f8d0fb4302
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

### `wordpress:cli-2-php8.2` - linux; amd64

```console
$ docker pull wordpress@sha256:04a33f93d6b8c232314d828ef770b33f775d6a6270c3f7b9c8bef79ab5f2bee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63678708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc677ec0bd7cd674c2a438d560eaa50d944ec330140f06198fa804a059200a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:14:27 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:14:27 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:14:27 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:15:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:18 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:15:18 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:15:18 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:15:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:15:18 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:18 GMT
USER www-data
# Tue, 02 Dec 2025 01:15:18 GMT
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
	-	`sha256:12338e337f403e3d3d0bd405e368698b64177e0d144507eb8ae3e0ef7f8275af`  
		Last Modified: Tue, 02 Dec 2025 02:40:03 GMT  
		Size: 11.1 MB (11076282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60beaf7052fc8af777b3ab82a59991b4255dba9e8f4237cb6da442b7ee017096`  
		Last Modified: Tue, 02 Dec 2025 02:40:03 GMT  
		Size: 14.5 MB (14512638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1436f61e127cd2d081864a90703316bf18fdb1a9c89b44035ec4dd39c10cc322`  
		Last Modified: Tue, 02 Dec 2025 02:40:01 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dfa998dbd894f1a70909271a96ec16f8d9e48d5f274955e5d969c31f6c0840`  
		Last Modified: Tue, 02 Dec 2025 02:40:02 GMT  
		Size: 1.5 MB (1525159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a948bab2b03ae2eaf8c889d9ada48bd92b991a44e79459e5f63df37d03b524`  
		Last Modified: Tue, 02 Dec 2025 02:40:03 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:64a5f1d57e9241d8beb7f831501b6b31fd6261a0df67b0fb556fecc585436c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e724a508fae9f0ff591837e6e68c254dd6d12be4e9f2543f45f95cd2ad8f25`

```dockerfile
```

-	Layers:
	-	`sha256:cd17b1756c5a5259c97312b481f5f9f7eb20e99e6d0444f9aa9c61ae9cd6f26d`  
		Last Modified: Tue, 02 Dec 2025 02:34:12 GMT  
		Size: 597.9 KB (597887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19556391f0aefb60f7e62d550c4d509e6417b69ad3385fce763f59366e9cbc98`  
		Last Modified: Tue, 02 Dec 2025 02:34:14 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:7fe77c4b5130af2cebd646420bb2e6f92142fa6427be0fcc54bdda948cd6ddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58380771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59089cb126fbd4db819ef283862033fd294217fdd9ce89803733dce978573958`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:11:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:11:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:11:48 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:13:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:13:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:13:03 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:13:03 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:13:03 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:13:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:13:03 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:03 GMT
USER www-data
# Tue, 02 Dec 2025 01:13:03 GMT
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
	-	`sha256:d4220b3adb2bbc0776850d827d88cf07e824a3c09c80ca7a271cb786e276c03c`  
		Last Modified: Tue, 02 Dec 2025 01:13:30 GMT  
		Size: 10.8 MB (10776191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b492b111d484562052d6b166436d663d8db9722c161d953de96ef63e38be579`  
		Last Modified: Tue, 02 Dec 2025 01:13:30 GMT  
		Size: 11.5 MB (11454839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ef7a8f8b20b98557d73a07ad7891750f1b08c7e59af0ddeea1ce3372525f4d`  
		Last Modified: Tue, 02 Dec 2025 01:13:29 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6032ea702cff7e994c97ae490f84d41e39bebd057f33a4ad3a598459cf6c6f5a`  
		Last Modified: Tue, 02 Dec 2025 01:13:29 GMT  
		Size: 1.5 MB (1525156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f9c0f0e864d0d197ab7c0b8df17bfe98b738c11adcee136fc91922e3ad764`  
		Last Modified: Tue, 02 Dec 2025 01:13:29 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:244fdc79f6cd95ed614c465a4644a6fda5274b6f810f5da2bd95111d7de21dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0781a0e878b3a41b183453c69a03da3e739f62d9f21f1769c9a871cb4cd83dc4`

```dockerfile
```

-	Layers:
	-	`sha256:60a346464542dd0d5b9340f379ba267e705237405ff1e9585a62bde53528decb`  
		Last Modified: Tue, 02 Dec 2025 02:34:17 GMT  
		Size: 42.0 KB (42019 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:93f7fc0fa9665c67935d17c33ec44bc2e366646e5566c915f1739688ec79eb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57500446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3acdaecfcf2bcd2c2c9a4f696b8701fe33dd7ce5f6157a097f4cd4e19748cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:15:58 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:15:58 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:15:58 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:17:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:09 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:11 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:17:11 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:17:11 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:17:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:17:11 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:11 GMT
USER www-data
# Tue, 02 Dec 2025 01:17:11 GMT
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
	-	`sha256:db6a80b4d7f4bb1d9f0ebf0a033ba69433b2399d95a554e68568a39a25bdd91c`  
		Last Modified: Tue, 02 Dec 2025 01:17:35 GMT  
		Size: 10.4 MB (10447593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d569a78bd1517f28f9ce2d84f2d0b32661f182a1ab123a1402f6f9099c3fc`  
		Last Modified: Tue, 02 Dec 2025 01:17:35 GMT  
		Size: 12.3 MB (12295598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b6920e4620e71126062f88027e4aca32041f9e72f904b8424eb499164e95aa`  
		Last Modified: Tue, 02 Dec 2025 01:17:34 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d37615fa07d8e3e5a5a18fecdbc191ec69dd3533c1dc82cbda1665511e809a1`  
		Last Modified: Tue, 02 Dec 2025 01:17:35 GMT  
		Size: 1.5 MB (1525124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b31c4fe9f21704d8ca77cebe4d167bf0f58fb3717e62630a1d788efa18381`  
		Last Modified: Tue, 02 Dec 2025 01:17:34 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:eb2b1e40e9c266116d9c32261c6f5cbbef5243406feb42fcd0de9dea92960750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec919c9acc9715003ef4233bcc340fe9a34a15830b2e4fcf784cb97429dd2fe`

```dockerfile
```

-	Layers:
	-	`sha256:723f4b0acf402f9b608b3374ad1aa9381aaaf9d0b30a735fa2566cb5450acb3f`  
		Last Modified: Tue, 02 Dec 2025 02:34:20 GMT  
		Size: 596.7 KB (596679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f208d0ae8591aa76b452f9c80ea88b84caed7ceaa28e61aeb6dca10c4d628b`  
		Last Modified: Tue, 02 Dec 2025 02:34:21 GMT  
		Size: 42.2 KB (42233 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:12398c15f077ba7697cd21c1822acbddc32f38cbfbc9c4904c5185520e558e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63634934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bc6e882a0a04f70604b2b483795816173b9acf3a5d0680261598b9fdd2962c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 02:15:19 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 02:15:19 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 02:15:19 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 02:16:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 02:16:24 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 02:16:26 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 02:16:26 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 02:16:26 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 02:16:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 02:16:26 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 02:16:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:16:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:16:26 GMT
USER www-data
# Tue, 02 Dec 2025 02:16:26 GMT
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
	-	`sha256:e43aae135a14f0b6ecb947a33098a572353c652d679a9e12366beb59eaef2733`  
		Last Modified: Tue, 02 Dec 2025 02:16:55 GMT  
		Size: 11.1 MB (11080235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6041cb8d725888dc4142abb75b0b57abd61e64da733e501e5bf91f13676aebf`  
		Last Modified: Tue, 02 Dec 2025 02:16:45 GMT  
		Size: 14.2 MB (14207284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7db510443c8dac3356457263205370034e358ff0fa3ed6809ac8d3aa2f026`  
		Last Modified: Tue, 02 Dec 2025 02:16:41 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d26c76f1844910a585cf87f858ad099e7605701e93009bca49047ff4dbe6f6`  
		Last Modified: Tue, 02 Dec 2025 02:16:41 GMT  
		Size: 1.5 MB (1525138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0178073b0500b910c876389a20f90ddea6c2c8438dce82575df752511adf408`  
		Last Modified: Tue, 02 Dec 2025 02:16:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:9fd6eb1b9fbfe1efc69b56228bf8e3b71ff027dfb0368ec75516d18dd2667026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (638965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075675c417a8bee2b885a9d0ebbaa228d2f594cba6aec6d796ed85a9c5d5e45`

```dockerfile
```

-	Layers:
	-	`sha256:81fded19c47b8dbf316fc072948a340f5bf0629dc1437bbb3c95a400170c5841`  
		Last Modified: Tue, 02 Dec 2025 05:28:12 GMT  
		Size: 596.7 KB (596699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e37583c48d4d2798138dde453f265e5659bdf6c4d9b3c4b2f6652202c591aed`  
		Last Modified: Tue, 02 Dec 2025 05:28:13 GMT  
		Size: 42.3 KB (42266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:4cd354c5536d1240b5115d72966a666fb65d666082caf56e126f79cd8b5667ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63029540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b95411469a5e65744595437ed39db77d22a4c3c72e3f4274231fc9054e6c625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
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
# Tue, 02 Dec 2025 01:11:03 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:11:03 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:11:03 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:11:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:11:03 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:11:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:11:03 GMT
USER www-data
# Tue, 02 Dec 2025 01:11:03 GMT
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
	-	`sha256:db943e2b11b99dbda81ce132b6a1f576815272ba4d71468ae6ddb6ecf83282fd`  
		Last Modified: Tue, 02 Dec 2025 01:11:21 GMT  
		Size: 11.3 MB (11274927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c751783fb4b1b75c7939637e18871085f2263009042fe5b96c1df75124c55fdd`  
		Last Modified: Tue, 02 Dec 2025 01:11:21 GMT  
		Size: 13.4 MB (13352112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735d51a98b863d901cdf8093b4ec3e40094e0cb5eb46e0403fa797900174b0e6`  
		Last Modified: Tue, 02 Dec 2025 01:11:19 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b61557ba144426406dab31a5101928d2b8f388a2d7f247fc89470255b76c72`  
		Last Modified: Tue, 02 Dec 2025 01:11:20 GMT  
		Size: 1.5 MB (1525136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd5074f2ba6bf619fa44c8cc889d8f34477de32a57e1e60dab36a17aaa7d5f2`  
		Last Modified: Tue, 02 Dec 2025 01:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:f1645f3e44fa3768fd3887251de50b1d7c50026d297391890649ecef55752e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca23828c293a36acb04567ccc3966c71dc9343684b94f62f919547280210df6`

```dockerfile
```

-	Layers:
	-	`sha256:5b4366ccadf7cfb93c489d3c4621535b7daadae4bf765e5305cb1883ec0b010f`  
		Last Modified: Tue, 02 Dec 2025 02:34:28 GMT  
		Size: 597.9 KB (597862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507e7d7cfa2fd3cf97e64ac0ab616618434b3b8e74bf734e2c1b73f503167c95`  
		Last Modified: Tue, 02 Dec 2025 02:34:29 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:0c08cef622ec1040ec3108516dde3a6965722f5585d57536947783d8aee1afa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64832819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41580f0bb763c6842e664bcec22165e7202b4301ecea10126af1424b930f45b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 02:16:43 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 02:16:43 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 02:16:44 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 02:18:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 02:18:15 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 02:18:18 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 02:18:18 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 02:18:18 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 02:18:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 02:18:18 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 02:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:18:18 GMT
USER www-data
# Tue, 02 Dec 2025 02:18:18 GMT
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
	-	`sha256:2366352666e4dd557dd7d6eacd17b46c7e42c50c724fbfccb0adfe0124e5f334`  
		Last Modified: Thu, 09 Oct 2025 02:01:34 GMT  
		Size: 12.2 MB (12183657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73282ba125c1b3ae777455c1347cbdd413abccdec275b5f14354238014866d31`  
		Last Modified: Thu, 09 Oct 2025 02:01:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0917746a8fc89942e41b18d04bd4a2d51801f5ee10b7a640efdf3cba7b311150`  
		Last Modified: Thu, 09 Oct 2025 02:01:35 GMT  
		Size: 17.9 MB (17911733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2e6ead17ffe457f82f3de4c7ffbd3e387c0ed949efb85c8cea9240539ade3c`  
		Last Modified: Thu, 09 Oct 2025 02:01:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebb5bdad2780ee25d55d07cfe6af262ea220bee955237b0283aad50d6290e82`  
		Last Modified: Thu, 09 Oct 2025 02:01:34 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab38e11b75fdfb40c297d248e34d3d6c8f9cc9dcbf937b26ebc35f816e76e34`  
		Last Modified: Thu, 09 Oct 2025 02:01:34 GMT  
		Size: 19.9 KB (19869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47df2902bc398720cd9b326e995b5ffe6d1abbf816de908975183046c3d84a78`  
		Last Modified: Tue, 02 Dec 2025 02:18:48 GMT  
		Size: 11.7 MB (11690193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590be19e1f31ce2fcc673fadff4e0c74189601ad4df1bbf655f20a66654931ec`  
		Last Modified: Tue, 02 Dec 2025 02:18:50 GMT  
		Size: 14.1 MB (14130486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d3ed7f203d8c6d1808f3c32c68e411bf10d9e0974c51c75d0caf0a0ee0aa00`  
		Last Modified: Tue, 02 Dec 2025 02:18:47 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273e84f94b7f9d079deb6e38ef6859a1e8b4bca73ff7751559d1191d5be1ce6e`  
		Last Modified: Tue, 02 Dec 2025 02:18:47 GMT  
		Size: 1.5 MB (1525135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704410fd33cffc24cdd49ddc1d80c0b5fdf010f0000f3e196468e316dcd60355`  
		Last Modified: Tue, 02 Dec 2025 02:18:47 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:d72a1044fc697acdcd4a8186912b66055dbfed38a7d7fa0a129559ce60db0d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 KB (636880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d249676d898e048d094252a501a13be4d0a402d445953edc6af8060dac071755`

```dockerfile
```

-	Layers:
	-	`sha256:2d14fc16eb95b7b458521553d3be6813d5bee18b7b79c6e7abc04ca4f1669374`  
		Last Modified: Tue, 02 Dec 2025 05:28:18 GMT  
		Size: 594.7 KB (594726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6d5f58cf89913cafb6e682092973c47cb5ce83e60606a2f1e99d01bf304d61`  
		Last Modified: Tue, 02 Dec 2025 05:28:18 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; riscv64

```console
$ docker pull wordpress@sha256:a13be21709623c72e9a4e088060e0eed337bf863a465dbd0b945f517c77c10a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60563258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77255e25434a6d69cf9ec9dbaf29e6a328d487dbce35080b441e6523acfe6a15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 06:41:44 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 06:41:45 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 06:41:45 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 06:54:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 06:54:47 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 06:54:58 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 06:54:58 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 06:54:58 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 06:54:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 06:54:58 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 06:54:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 06:54:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 06:54:58 GMT
USER www-data
# Tue, 02 Dec 2025 06:54:58 GMT
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
	-	`sha256:5e488044b38fedf2b0c5a42fee0d7f8266277e151bbc0aada6a071b34ec2fcfe`  
		Last Modified: Thu, 09 Oct 2025 23:00:37 GMT  
		Size: 12.2 MB (12183652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccad6f0a1f0db89e61f61fa65505f5f655a026a9c873b83bbbd58c9526e7494b`  
		Last Modified: Thu, 09 Oct 2025 23:00:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f77ff3e558a41b1523465a18a137851fd9938a8cb358de62b9493ef9e803ce1`  
		Last Modified: Wed, 15 Oct 2025 00:38:01 GMT  
		Size: 16.2 MB (16241932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ec90dcdff294062eee93c5da6fa2a41ba059923e53062630be6d1ae2f5d50a`  
		Last Modified: Wed, 15 Oct 2025 00:37:59 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b022a0d80ae9c203b3f1ab372ea604ce61c0bf1430642cdfc7f3ca728ff4699`  
		Last Modified: Wed, 15 Oct 2025 00:37:59 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6de4bd59b1e51d224780e4b9f8ad06851525912d241503fcacf7eb3ac40fad8`  
		Last Modified: Wed, 15 Oct 2025 00:37:59 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9653935b124dd999f81497d841c1f5f751c7a7b4ffaa79682ca6570a450eaaaf`  
		Last Modified: Tue, 02 Dec 2025 06:56:31 GMT  
		Size: 11.6 MB (11571123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35d3092a3b1b5be344d7d15f271d6bb97114073a9c160e7f757944940c7b607`  
		Last Modified: Tue, 02 Dec 2025 06:56:31 GMT  
		Size: 11.9 MB (11881207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0856e4069b215761ca89a8d99313539681d1563cb1e21b6f7c1af8fbd891fbd2`  
		Last Modified: Tue, 02 Dec 2025 06:56:30 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fa437d80fddf7012e42880843083b6082cb98bf2a2f8c995e0e928d1354f74`  
		Last Modified: Tue, 02 Dec 2025 06:56:30 GMT  
		Size: 1.5 MB (1525145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8682a9f8ebe7b22e5f477d7742e5b291c68c56f592f76c89c17cac56def2d69`  
		Last Modified: Tue, 02 Dec 2025 06:56:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:58e76a801a607f98779bd47133581ee6396d45d80d4929ba74689b81ccd5a941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 KB (636876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f444481a33a0e00dc5b423ec82928f7f7d8220f0825f8ce6cd2612bc6e0e48`

```dockerfile
```

-	Layers:
	-	`sha256:c16da3903833edc463d649e000b183a424eaa6ddad3d901fcb6763524b6347c0`  
		Last Modified: Tue, 02 Dec 2025 08:18:16 GMT  
		Size: 594.7 KB (594722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cc9509c91b7fd76263e08a4f32b19ae1cebeff2b4be2f3ed0762c34e185f36`  
		Last Modified: Tue, 02 Dec 2025 08:18:17 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:f951d4da264ee83281bf765efec5bb96f168fa246a749441689e911c524fd61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64511285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8605aa98652c8d7fe44c549591327fb34b2439d494e3ad7a0ae7c9a0a28cda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 02:32:17 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 02:32:17 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 02:32:17 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 02:33:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 02:33:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 02:33:56 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 02:33:56 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 02:33:56 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 02:33:56 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 02:33:56 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 02:33:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:33:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:33:56 GMT
USER www-data
# Tue, 02 Dec 2025 02:33:56 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67516b8f02966476a2ac367f1c1762ddfb0d00c7ee8d7c61e93a4513d64874b0`  
		Last Modified: Thu, 09 Oct 2025 04:59:26 GMT  
		Size: 12.2 MB (12183674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1503a156a632da17ed8630b68eb6ef4a3de869be2e9a5e3b159a000ae826cf33`  
		Last Modified: Thu, 09 Oct 2025 02:31:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4070a56889cc63d4c08fef57130b05fdacb2816097d4a2328f9e1f78dbbacecd`  
		Last Modified: Thu, 09 Oct 2025 14:30:19 GMT  
		Size: 17.1 MB (17147273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2e0e56be120c4d7d04c4e114fd7f8ee6f87497fe5d1fcfad85e5a3ac23f01c`  
		Last Modified: Thu, 09 Oct 2025 14:30:18 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2bb6eb3f16b36dc9ed233f5d62fff38b516676b45acc24810b0d401dd832b9`  
		Last Modified: Thu, 09 Oct 2025 14:30:17 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33142020b2c64c290ecbe0f705adaf47e6487ecdfa246f5e123898f792e4e74`  
		Last Modified: Thu, 09 Oct 2025 14:30:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5b163a2e01daea51f4fbc1a6a7698f1250a636d5d94b7a6f8cde016493793e`  
		Last Modified: Tue, 02 Dec 2025 02:34:22 GMT  
		Size: 12.5 MB (12452445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe68296cbf2e4cb89eb6653ba1848b683bfa7b1fd1b676a9be55b5384a4533f`  
		Last Modified: Tue, 02 Dec 2025 02:34:21 GMT  
		Size: 13.8 MB (13816048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548aa913fbcb6bc8d1c233f48c15973d22877bb7eea7504949d02c2574ea8cd0`  
		Last Modified: Tue, 02 Dec 2025 02:34:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c6743f45fe0bd51f57150bdc8334b0226e5b1b93a364852d7df34646e4bccd`  
		Last Modified: Tue, 02 Dec 2025 02:34:21 GMT  
		Size: 1.5 MB (1525185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73361406d18173914eb84dd12b459c55c5a5fb071c71054cce58a32b272931d3`  
		Last Modified: Tue, 02 Dec 2025 02:34:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:ba7582dd47f6070ff13cb341c874eecfb042b7c65be7a5426f9e13de41d954b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99042be3d5c7e8968fe619328570bce50fafe79aaf94ac456e4c6e3694891d94`

```dockerfile
```

-	Layers:
	-	`sha256:4896351462b8380831e600f76b2565251db98000663546493ac1a1d790d293d3`  
		Last Modified: Tue, 02 Dec 2025 05:28:23 GMT  
		Size: 594.7 KB (594692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6c3e5ec6a64db28fa196ce096f2d5c10a038c210eae0e1ae4c2eeca6e4f537`  
		Last Modified: Tue, 02 Dec 2025 05:28:24 GMT  
		Size: 42.1 KB (42101 bytes)  
		MIME: application/vnd.in-toto+json
