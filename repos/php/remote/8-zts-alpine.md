## `php:8-zts-alpine`

```console
$ docker pull php@sha256:1d55d61a32092cbab93645094df150595f134569132f22338474c71890d1fe2e
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

### `php:8-zts-alpine` - linux; amd64

```console
$ docker pull php@sha256:8f973e0ede0737ec3d208fd8f1ca16364e0fc67cdf006f6da1138fde6626cac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50402479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe4b4f32397f81c312352a95fc1e3948c8dd240774b4df6cfcfab3e591e2c54`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:04:28 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:07:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:07:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:11:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:11:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:11:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:11:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:11:15 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6041417428d5cfce129b74aae8745630ff58c34d61ca388e9572d29394b2e2`  
		Last Modified: Thu, 04 Dec 2025 01:07:46 GMT  
		Size: 3.6 MB (3591356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2886ef94aa547ac73283f51af96d3708fee0e37700d15ba66f1c51fd13d628b`  
		Last Modified: Thu, 04 Dec 2025 01:07:45 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecf7c011f36278523cca508879858b6b91609820c72d5a56f8aa11c8a8684c5`  
		Last Modified: Thu, 04 Dec 2025 01:07:45 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532a6d7796b6f93e1a61b2ca478972bb75cd67107eb9c0de1dbf2b2ab884e7a8`  
		Last Modified: Thu, 04 Dec 2025 01:11:33 GMT  
		Size: 14.3 MB (14339209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a79555eeba761f2bd7bb1b549b864e6e6b83ad84db5a25a39e9b653b061d3c5`  
		Last Modified: Thu, 04 Dec 2025 01:11:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d4ee0591d341e54ab7b78963ae1679d573888431ea69caa7b2dd85ea08a52c`  
		Last Modified: Thu, 04 Dec 2025 01:11:35 GMT  
		Size: 28.6 MB (28585021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c1312e953484209557bd25fe93cae11e437ae9c0ad4389a219898e11dede5`  
		Last Modified: Thu, 04 Dec 2025 01:11:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d63ada92701afcabca80cc8e6e2caa562151015e510ff40dc7b6b03b3ce10`  
		Last Modified: Thu, 04 Dec 2025 01:11:33 GMT  
		Size: 23.5 KB (23496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:6526e7b489b77deb6a038c8086b7aaa97743018123964e414fd20c4e8010e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 KB (319176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2131670fec6f1ac4a5474a49d3ce2ff863508fb4181c6121c81461e621f085a`

```dockerfile
```

-	Layers:
	-	`sha256:7bc84427efa076603ff7c8b6c327562d5aed0a9d65fb29abdb965286b99a85df`  
		Last Modified: Thu, 04 Dec 2025 02:56:09 GMT  
		Size: 280.9 KB (280912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb54cc2ee0af36104bc8e481a1ed575bd0d832a9ccbf30f7a37eef89611f6c12`  
		Last Modified: Thu, 04 Dec 2025 02:56:09 GMT  
		Size: 38.3 KB (38264 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; arm variant v6

```console
$ docker pull php@sha256:bda17a164714121777555ba9c95e1d771e4efa20487351b68e81357aba47074f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46370183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4464a6aacab7467f65fcef0b433b16b5adb578000e588441ef947478d3a7c71b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:10:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:10:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:10:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:10:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:10:01 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:10:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:10:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:13:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:13:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:13:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:13:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:13:20 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b4638f97ec4aa06e79e198961fac4a6d3b5210d1f60c5dccb620f4d2006fbc`  
		Last Modified: Thu, 04 Dec 2025 01:13:39 GMT  
		Size: 3.5 MB (3547606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3926205bc3865c02ac000eada2f5a1a431d46f65618fc83024b9e26e91a453`  
		Last Modified: Thu, 04 Dec 2025 01:13:38 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c8ca03967331f568df5ff75b0a18aa53e33fbcf4436c5171c81e69ab7e4a8`  
		Last Modified: Thu, 04 Dec 2025 01:13:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6439b9069efa273c3f8210d28477e8d0fc8378c7bc2a8e06b42012780a099669`  
		Last Modified: Thu, 04 Dec 2025 01:13:41 GMT  
		Size: 14.3 MB (14339255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1c6a31c346ee7171b4dcfb8a1de2c19654729f585e1ac284bcd0b9848e20c1`  
		Last Modified: Thu, 04 Dec 2025 01:13:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a51a0c1f4da499a141ed0409e36cf44653b57f3452e109d1269106f919dd8cb`  
		Last Modified: Thu, 04 Dec 2025 01:13:44 GMT  
		Size: 24.9 MB (24888015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aa2349b0ca475f039df1a0ef069f85a4d2467709f951c943ff48cacedd5a47`  
		Last Modified: Thu, 04 Dec 2025 01:13:39 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86e94c8395bee4489fe6b37eb0273c776b299c3aff5cbf4c5fe6df95d11aa9c`  
		Last Modified: Thu, 04 Dec 2025 01:13:39 GMT  
		Size: 23.3 KB (23330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:40bbc88eeb47a8a7db648f4c0ce0b9867cbfe51b2e2d2ea1ae8f8460a5c722b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccb3cbc87531f4fa7944e8d6140023f186bf8369c120d4deea0aca1d3ce14ff`

```dockerfile
```

-	Layers:
	-	`sha256:3c8e4990847cc5dbef5840135db0307c1bc9ecc50540d8bc049ff6c32735f6c7`  
		Last Modified: Thu, 04 Dec 2025 02:56:13 GMT  
		Size: 38.2 KB (38226 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; arm variant v7

```console
$ docker pull php@sha256:2fc8a29e61b4ab7f1cbaa04348e556f9d560b6ff818ac9fcf035b84da49b14a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44430798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adc525461df6e56d28278f8d3a3a232e2f8e1192bc8192b8193cbba62510d68`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:03:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:03:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:03:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:03:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:03:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:03:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:06:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:06:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:06:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:06:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:06:36 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd894f51e3764736bb05301b970f25645c1cf3e4f8c635b1c60a852a93f7ac8`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 3.3 MB (3346525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9259ca1939c2345efa94c49afa3bb7114bd93157c3c12c9d71e12b61fb659030`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe771a7bc75ff2477d17a4e1e5f8a78571610720921b5a8e6b761dd954c99c`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed9c0a39c94eb9747613fb99fafe521eb6d9ed3e5879b8c3406a8c661495ba`  
		Last Modified: Thu, 04 Dec 2025 01:06:51 GMT  
		Size: 14.3 MB (14339221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f843d7b9f4a40b0cd0a93bb11b1c50e1ca1f78561ff1c0f30ef582e8dd55fd4b`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50361410e0aef455e74cdeaf206a30410c50001a755c46e77cbf2702084e4683`  
		Last Modified: Thu, 04 Dec 2025 01:06:53 GMT  
		Size: 23.4 MB (23439178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bab992199cece222e2b1dec29add8f2ae52727baf1503d60b126213ef9e30c`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5716a08d0c1f2dcd53834b9e2f112c72692651849669088b8af3a5c41bec49b`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 23.3 KB (23332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:4052c0c1d06cdc21176603811638648754010dd03278f27fcc52d273e5cf0a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.8 KB (315781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ac0837fd5899ceccfed46eb632ae6d425a0a274d981fa38e7d90339887d15d`

```dockerfile
```

-	Layers:
	-	`sha256:00d6ff768b98e0413fee16a5c062f38d6bc913cc08f252189680820e4d10a4a2`  
		Last Modified: Thu, 04 Dec 2025 02:56:16 GMT  
		Size: 277.3 KB (277340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04550f9f99dbb46fbcd63c925e21590f285edeab0997eb7f89cdbad426feab3`  
		Last Modified: Thu, 04 Dec 2025 02:56:17 GMT  
		Size: 38.4 KB (38441 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; arm64 variant v8

```console
$ docker pull php@sha256:bf3ea225677d41d038b1345c6687ee5528c58707c05f53e83ff56b178e2bc9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49706474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba660b188614ff4e5284ae2c0ec93c1480f9edccc85f801c3c7fbd3dd0d3533`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:05:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:05:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:05:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:05:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:05:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:05:14 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:05:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:05:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:08:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:08:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:08:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:08:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:08:54 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269acaeaa1d3677168cb09c69795922d3d16b5ad9cc6f9f4b200c6514385768b`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 3.6 MB (3600575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792b53aaabf2972766c93a554ffd96afd7419a39d2b718b9fdce8133f2105201`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c96ccd24f63306922b51cef7432d7dd4f63849f5cc83289c59c8ff028f83a9`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9accf9df7b8e9e55022cacdc17adbb9b42213eb0a0357c81c19f06ef524c4167`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 14.3 MB (14339213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd47ff8fc8f246f42640e24962f3131042091308ea7d8094868c2469730726b`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f95bb5015b66f01fef679d635a3e5ef065a329275f99c758a65f61391471`  
		Last Modified: Thu, 04 Dec 2025 01:09:13 GMT  
		Size: 27.5 MB (27544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842b4cf3b84991528bb03d4342c0c8b5ece535f31a56e1b0a54215bd83f4271`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf198ce410c7a898db81cf37c7064b08d03ba92d87fde588ad7f108c065a91d`  
		Last Modified: Thu, 04 Dec 2025 01:09:11 GMT  
		Size: 23.3 KB (23327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:d7e3595b43c39eb9d5ee122f0720eb0585e1057323c9b977017dff690ab0aab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.9 KB (315867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0faff1d93a882e8537c5bf8ffd0fdff9f569ad92d98de38af377b352a2ab775`

```dockerfile
```

-	Layers:
	-	`sha256:a78ce8519410cc9918326def94c34a472ade7adf2a5a8002b3fcf75163a33daf`  
		Last Modified: Thu, 04 Dec 2025 02:56:20 GMT  
		Size: 277.4 KB (277376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4549db552bb8cd860013a367149803a8e5b77d239fe612208c7c9a4090316b70`  
		Last Modified: Thu, 04 Dec 2025 02:56:21 GMT  
		Size: 38.5 KB (38491 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; 386

```console
$ docker pull php@sha256:a8132ecfd090087ab08250e55fee541db12e0efaa4b1a7c44f86c4aca63d628c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50731833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e3c913d7f91d17bcb820088e61aaf8815cf9a168d2c6e69d9a33cd090ea0e8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:04:01 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:04:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:04:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:07:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:07:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:07:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:07:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:07:52 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7902450dc5080c4d81bf87529d0d365a845307203c724ae7f69aa2eef2a689`  
		Last Modified: Thu, 04 Dec 2025 01:08:13 GMT  
		Size: 3.6 MB (3628300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076e602c2d79fb003faf47ff65d319d7ef46fdc33180d3f7941f3ea63d722a92`  
		Last Modified: Thu, 04 Dec 2025 01:08:12 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2748f76b7b3d5da812017efce965903f673120308aa385b55c0350fc1f48e72`  
		Last Modified: Thu, 04 Dec 2025 01:08:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce5e7b60b36bdf48618197f66df4395ce82b5690ed70c55a043ebf1ccaf26b`  
		Last Modified: Thu, 04 Dec 2025 01:08:14 GMT  
		Size: 14.3 MB (14339217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba026d3ea473ac5e201e95a5eb0c0fd05ec072eaab3b8dd6ebeb09f8b2d68079`  
		Last Modified: Thu, 04 Dec 2025 01:08:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ddaf7162c23de3e6511a3cdf8eef9050eeb09c4d612d1d90baf83d031661a4`  
		Last Modified: Thu, 04 Dec 2025 01:08:16 GMT  
		Size: 29.1 MB (29050883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef224f99e0c781c2282f70d32df1f5ef719b26e06b09aab559583e0dfbee6010`  
		Last Modified: Thu, 04 Dec 2025 01:08:12 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a612dff8f71668d2bfb8011d2203ad3aec2aa56cbb1596e3cbb7acf46a7290`  
		Last Modified: Thu, 04 Dec 2025 01:08:13 GMT  
		Size: 23.5 KB (23497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:8131753702900bb4f4bc65d164d9c04b9177fcb154a55033109c8bd5c08d7372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 KB (319069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ae35bc9efba91753bce802c2cc3050d959c9610d7372952c9a11ae244764d0`

```dockerfile
```

-	Layers:
	-	`sha256:d78bdb2f698acbc5ced953fda51d7fbc61a103fb03cb8375bf0042eb39dea671`  
		Last Modified: Thu, 04 Dec 2025 02:56:24 GMT  
		Size: 280.9 KB (280867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2edeadd4119ff7577f7081f5fe0849c2b4864ea5067b9f1f0bddf134dbb3615a`  
		Last Modified: Thu, 04 Dec 2025 02:56:25 GMT  
		Size: 38.2 KB (38202 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; ppc64le

```console
$ docker pull php@sha256:da849df2d685138a79a743db23c2317c41d62e75c3be5e420c40dc99e0d5e5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50661577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a15c091c8f7fd2aea657d1ae3cf1d269a9a07a623a654bda9fe90d5924262c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:04:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:04:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:14:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:14:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:14:52 GMT
CMD ["php" "-a"]
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
	-	`sha256:c70ed10e415fd1d8fb8291a94bec41018550290a091dc20bd6a2b4c9163bc3ed`  
		Last Modified: Thu, 04 Dec 2025 01:09:57 GMT  
		Size: 14.3 MB (14339204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35318a7e2707aa852dbbcc2e19441879f6d5a50914ecadad1a0fd390fcfbafff`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2878d3e7fb5f093944ac53f5a49e3214f072b3a29d818f547670145dc532b76`  
		Last Modified: Thu, 04 Dec 2025 01:15:33 GMT  
		Size: 28.7 MB (28699048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36017d006798d130dcc1ee2ec7e5289be8540953c545cfc3213a3eea8c7ecff1`  
		Last Modified: Thu, 04 Dec 2025 01:15:29 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e47646ff2521a84ec957d5f04eec785a6c37ce58ba482b187f380f78bf00d42`  
		Last Modified: Thu, 04 Dec 2025 01:15:29 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:c4ddab31d38d57832ab02ff1ce765f0c62299c4a1f49725f4dec45289bbe1d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 KB (315670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b1ef0645fe8db7222b3f881485fd7220d71bb414b6625d0ba6ca9e711fc14a`

```dockerfile
```

-	Layers:
	-	`sha256:92df61ae8b75688ed541433577759c8cb5eecf1a07905db5c13e844e7fe530be`  
		Last Modified: Thu, 04 Dec 2025 02:56:28 GMT  
		Size: 277.3 KB (277329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccf7c3db18baabee1a70080ecbff8c71fe8417986183b68ae2d95c42b14206c`  
		Last Modified: Thu, 04 Dec 2025 02:56:29 GMT  
		Size: 38.3 KB (38341 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; riscv64

```console
$ docker pull php@sha256:22ad8c5be784eaa632f488ad960eeb825a085ce4fb06ee5f3453496ba8358b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47826361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422e33310801607a064287cd002b14f4f132d7d7be3461e2271d8c742e2fe671`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.5.0
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Fri, 21 Nov 2025 18:11:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 21 Nov 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:13:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 21 Nov 2025 23:13:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:13:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 21 Nov 2025 23:13:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 21 Nov 2025 23:13:08 GMT
CMD ["php" "-a"]
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
	-	`sha256:7b78145f828236da92cae404b7a86a1b9977547aef9cacd9db35b1f67c9b217a`  
		Last Modified: Fri, 21 Nov 2025 22:12:17 GMT  
		Size: 14.3 MB (14336681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830fd477687fc32a534de40617e67d6f74459e4e0fb3f069e7687225a4b56466`  
		Last Modified: Fri, 21 Nov 2025 22:12:15 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be9078c3b31b6b4165fe6d271d1e60495c57b645ed3ab2c7295466b6391bc79`  
		Last Modified: Fri, 21 Nov 2025 23:14:40 GMT  
		Size: 26.4 MB (26350210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f534b35b5f3626b008515bbd2c0b437863ae43bf3ebef08cb4a749c7b57d7220`  
		Last Modified: Fri, 21 Nov 2025 23:14:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eae6cac06b78df9883f009baea7076f31c539422182cfbab1e4a48c64bc7`  
		Last Modified: Fri, 21 Nov 2025 23:14:38 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:581418ef9ce692c6c55183127d329195bceb4c2cbac05d32a446c3e9540cb447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.8 KB (312763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ec91b730375a88c4f2ff0b563ce1bbed42c300caab574aa4487834849e83d2`

```dockerfile
```

-	Layers:
	-	`sha256:97fb7dd5b978ac9e0dc6a843d038331ff94c726e48a73e1fb3715c6e5fb78535`  
		Last Modified: Fri, 21 Nov 2025 23:55:10 GMT  
		Size: 274.4 KB (274422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ca333043de69e3ddf319ea912ace654d9ee71ec6e103feff574714f98ece61`  
		Last Modified: Fri, 21 Nov 2025 23:55:10 GMT  
		Size: 38.3 KB (38341 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; s390x

```console
$ docker pull php@sha256:4a2cbe31ca9f024b08ba475e2d761c7456e38add47521d68ddadc16eddc46098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14be95a6815ea4259a41a8fd623b89f813191d90a2446a7c655a29dc8ddbf3a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 04 Dec 2025 01:04:06 GMT
ENV PHP_VERSION=8.5.0
# Thu, 04 Dec 2025 01:04:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 04 Dec 2025 01:04:06 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 04 Dec 2025 01:04:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:04:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:11:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:12:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:12:01 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86a469d48aee3179f6f6e8c068e4bb1a90377bd0c168b6ffd611a5e9bd97207`  
		Last Modified: Thu, 04 Dec 2025 01:12:26 GMT  
		Size: 3.8 MB (3793981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122ca20d96ec260e1bd3832160d7637302ad1839c3a45c36076fd573e28306c8`  
		Last Modified: Thu, 04 Dec 2025 01:12:25 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd264404b0fa956c9ca7df65d13955606b2ed3c59522b5a0f52b5275b9d5994`  
		Last Modified: Thu, 04 Dec 2025 01:12:26 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a759743db94e853b2c6458a61a35314c52f11b24190492f27bf106e411285`  
		Last Modified: Thu, 04 Dec 2025 01:12:27 GMT  
		Size: 14.3 MB (14339211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5afebb32971e4fb81538f62b9406f0b4867ac534e645ec0bd1c68a88e86eee`  
		Last Modified: Thu, 04 Dec 2025 01:12:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa9e25e77b051a7c1e7ace9149c04c987b356224a3c2b01eaad3c3f9a415b89`  
		Last Modified: Thu, 04 Dec 2025 01:12:29 GMT  
		Size: 27.3 MB (27342632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d13c75632c1c0c4d214e34fb5a29ba2f991e51016c3b8e3b7f683974878a87`  
		Last Modified: Thu, 04 Dec 2025 01:12:28 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df764eb1b74b47ac0e9b9e5fd2267c34f50d61d46088b94882cc046b8d68bdb2`  
		Last Modified: Thu, 04 Dec 2025 01:12:29 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:e28b7677994c53b318b2972dd03d143f18360977074416ea2aa6e72ae95284d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97d720b665238285eb7b8bb04998ec7ef6b1ce837a69fe7db6565eb4cfed6d2`

```dockerfile
```

-	Layers:
	-	`sha256:118983cb96804ff0125e341aa24f79b0c8d0a188277dbabefc4ac0a2d4b5c78c`  
		Last Modified: Thu, 04 Dec 2025 02:56:32 GMT  
		Size: 277.3 KB (277271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9240af5d8cfb6b8cb605f2ff2c8e4c484215525c47378ef3c7eafb67426498b5`  
		Last Modified: Thu, 04 Dec 2025 02:56:33 GMT  
		Size: 37.3 KB (37313 bytes)  
		MIME: application/vnd.in-toto+json
