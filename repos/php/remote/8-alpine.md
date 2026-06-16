## `php:8-alpine`

```console
$ docker pull php@sha256:6943c701c2b6b205467ba6db29252c5efc71b8ea3456cd3924bb057eabc70691
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

### `php:8-alpine` - linux; amd64

```console
$ docker pull php@sha256:1f3fed598de47fb4bb1814bb1a4c63771b7348c997665d32b509a66deb0257f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44562601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379af6f332a0a3941799219dca45f771e0f43a365fa217ec70bb693bf4f6e435`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:15:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:15:18 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:15:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:15:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae20b0196840c9219c177aabca741da366995c4ce495b225be380b49cdb8d78d`  
		Last Modified: Tue, 16 Jun 2026 00:18:54 GMT  
		Size: 3.5 MB (3466812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2dc5f499cb55a871afc820e4afb0db9c9cb3587302d3ef3d158163623bac3c`  
		Last Modified: Tue, 16 Jun 2026 00:18:54 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4fc3ef053a7bd87da959daab82651dbdffc5d4fec23e6866b91fb53189091d`  
		Last Modified: Tue, 16 Jun 2026 00:18:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceab19d95ef2cbba5e7bb903c6c66b5de34b329b4d4337f9e94179e92b8aef5`  
		Last Modified: Tue, 16 Jun 2026 00:18:55 GMT  
		Size: 14.4 MB (14421107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf59e36bac85247912667d49a6e33fdccc7a90b5019ba66e26c6a89ec4a0d602`  
		Last Modified: Tue, 16 Jun 2026 00:18:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4435e97c27dd2c49e1cc244a77b920f94ce815cbd318eb74d046dca9b8825312`  
		Last Modified: Tue, 16 Jun 2026 00:18:56 GMT  
		Size: 22.8 MB (22801861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1265107809d4f53c64c4d44a93f82586272af89ca31522ad6135a4e3a1ec249`  
		Last Modified: Tue, 16 Jun 2026 00:18:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2cf110598fe0b845560c0c70d72349456c71fec8c7283f6e3eb226aaeab895`  
		Last Modified: Tue, 16 Jun 2026 00:18:57 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:bdb88bbd74a2740c80dc1b4b53b7f97ba323f5e07eea52d17fba0a0af3454e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 KB (303198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37e14c30b4bb66921ae44b64e8061bac68fa84d846021f3928223b264112846`

```dockerfile
```

-	Layers:
	-	`sha256:2536fe8f787afc7427e018c840260b0d683afb8cdf0454935859e34421126782`  
		Last Modified: Tue, 16 Jun 2026 00:18:54 GMT  
		Size: 262.8 KB (262830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bac3adbe373e3c348ca91f3dd0d320454db2e479e2e4c09de75cb00e459bb78`  
		Last Modified: Tue, 16 Jun 2026 00:18:54 GMT  
		Size: 40.4 KB (40368 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; arm variant v6

```console
$ docker pull php@sha256:36a6b3ec14d28a9ee261a823d3ad2c418e4bcf796d93951c37e9d3f583385160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41170081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0717afc7aaadb3d7b754512039629cf0e60b9b2b5e23d197998b3da31bf6443`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:15:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:15:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:15:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:15:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:15:59 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:16:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:16:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:19:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:19:06 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c10de85c13c58b183c64161e67fdfa82f923d753b7e05f902234079cd4d3f8`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 3.4 MB (3416707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9d77ae9c06df0b69072d91593dc532182d4f0e47c549c24091022fd3c6cbc0`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030a168a72ea13500d7287d96868c0ae350aa176be903db9e7f336d42ea01771`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf7afba15cd736bb18fc36b9436e6d7be137ed38183df8735be51c0f80d2283`  
		Last Modified: Tue, 16 Jun 2026 00:19:13 GMT  
		Size: 14.4 MB (14421110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb3b74c79511bfd262d9d918151a3fbf85283254ceb60ed1a213d9eea52604b`  
		Last Modified: Tue, 16 Jun 2026 00:19:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb94fc21de846f57ea97c7039663b3b7e786cf1cf680b80e712ca32b7f510696`  
		Last Modified: Tue, 16 Jun 2026 00:19:14 GMT  
		Size: 19.8 MB (19752607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96270427f7ca071291a5070a7fee7138e9c1463cbc4b2ba86500297a6d0d7945`  
		Last Modified: Tue, 16 Jun 2026 00:19:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac854143235fa85ac5c73dcf5d849b7b9d8e709b518bc6df5d9a3857f198809`  
		Last Modified: Tue, 16 Jun 2026 00:19:15 GMT  
		Size: 22.1 KB (22125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:aa3d9c8f1b309f15faf57cc6b3d6044cbd15bdd35c445d875fcad30c5fb66f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50f32d06ef8dfd6ac3d7400e584be93bf3f07b350f10bbf1e93163c0e524a97`

```dockerfile
```

-	Layers:
	-	`sha256:3cb828b768797a795cffde289edd2e3b6ad7d7462aec4f4afbd67dfc76edf403`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 40.4 KB (40394 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; arm variant v7

```console
$ docker pull php@sha256:81d0b3140ab7a035157dcb79384a6542d91e7bfeb8c26c710a85ce6e7bb3c923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39580783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee7d8a751a7c5075a7ddd6877ce3572aa466998f5065cff7fdac4e33afd9ef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:16:00 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:16:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:16:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:19:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:19:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:19:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d01106095fcdb9e64ec0f122abb86ff10c18733dc6151a48899cacf6f02d502`  
		Last Modified: Tue, 16 Jun 2026 00:19:20 GMT  
		Size: 3.2 MB (3233763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb358e8c78f76a825ea232adf46d5f4bfb7214f0cac284591d6d0a9f920a81ef`  
		Last Modified: Tue, 16 Jun 2026 00:19:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff75ea9c9476cb4c99fbb11c923719a9a1e7e0a2d1c82ba77109fc4bdf1776e0`  
		Last Modified: Tue, 16 Jun 2026 00:19:19 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f437ecfba8d76ac3c1122df3e8bfc5df01f80fbbed2ad1ec6bbed5423ed27797`  
		Last Modified: Tue, 16 Jun 2026 00:19:20 GMT  
		Size: 14.4 MB (14421120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f7bb99f53f02a2f2a0a9eefa8e6e9b1bbc977026a180d122ca87b519d111e`  
		Last Modified: Tue, 16 Jun 2026 00:19:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe68f8e125b5948e9426161e3c8cf33e699d830153c8c573c0cb93297d5839fb`  
		Last Modified: Tue, 16 Jun 2026 00:19:21 GMT  
		Size: 18.6 MB (18639068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a810ce6e2101ff22318eabe887dee5eb741bb3749b35edd447d6585f6d08be3f`  
		Last Modified: Tue, 16 Jun 2026 00:19:21 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba19c2193b1eaeb95acff19ad9416f61875623f2d410f9845f10b4e04d1e945`  
		Last Modified: Tue, 16 Jun 2026 00:19:21 GMT  
		Size: 22.1 KB (22132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:7381bfa4fe54415c81d289ec69e27028d9101a7c8a0f7fef195df5fd78b5ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 KB (299931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e382d623d593c3d2557018019cca674615b5b39a685a5abd7451426766d60ae8`

```dockerfile
```

-	Layers:
	-	`sha256:d1aa8532910b3485fc45750770b7d7ea3e99429b96d8c4b2127b87d0c6255a7d`  
		Last Modified: Tue, 16 Jun 2026 00:19:19 GMT  
		Size: 259.3 KB (259322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203a2f1b931280e4bacdc40b1511693877803b31766fcaf515359c1a1e1c40be`  
		Last Modified: Tue, 16 Jun 2026 00:19:19 GMT  
		Size: 40.6 KB (40609 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; arm64 variant v8

```console
$ docker pull php@sha256:6abbc930234d16bad1540a2cc4e21b7e61502060d54d067b9bbc0a489d5ad5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d486ee14a07608f53940bcf93bfaefc4047fe072facc5824f0e5c07844e98c07`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:13:23 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:13:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:16:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:16:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:16:50 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2c4225b25422ed29531a6b5536068b314540cf863556399732aa427a6c3c3b`  
		Last Modified: Tue, 16 Jun 2026 00:16:58 GMT  
		Size: 3.5 MB (3475811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109df5f88e76f3e03e1d1ee831c783c0692dee3ec06a9f8f1c9858fd647a262f`  
		Last Modified: Tue, 16 Jun 2026 00:16:58 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddc0ae81e1d50682617e4f460c363ddb53cd1a5b165133c104166e8d28f2623`  
		Last Modified: Tue, 16 Jun 2026 00:16:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34777e0a4a9960fdb39bb4497ff1e1916fa5b97ed5ae4a49fae4644ee448eaff`  
		Last Modified: Tue, 16 Jun 2026 00:16:59 GMT  
		Size: 14.4 MB (14421098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbc24293c688e21986dc378ac5d824a855411a242d1e2ae772563e6389fd71`  
		Last Modified: Tue, 16 Jun 2026 00:17:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa1e34be36aa9dfade1196352e95e6cbcf493a7cfd0038b49fdebad9636ddee`  
		Last Modified: Tue, 16 Jun 2026 00:17:00 GMT  
		Size: 22.0 MB (21983030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f6a3c1b2888225700186f3cf175a4888b863c44827ca48bc73bb57d76f4a61`  
		Last Modified: Tue, 16 Jun 2026 00:17:00 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beff9da5c624e6a1883f05974354332e57c46e075f557e988e4c9d58f2b6f4a`  
		Last Modified: Tue, 16 Jun 2026 00:17:00 GMT  
		Size: 22.1 KB (22149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:8093d5f198d40fd278b117a8206fece967fb645f545351a5712fc0f27e28f981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3980c9e1735556986373009fcaefe664fca41c09d9544d318eadd86550c3a766`

```dockerfile
```

-	Layers:
	-	`sha256:14123284d0c520c0f4f0e86edef72cf824df16f8560dd9aa68785ae0c6bde983`  
		Last Modified: Tue, 16 Jun 2026 00:16:58 GMT  
		Size: 259.4 KB (259390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:385f722febc2eb333fe2011abddcceebaa2a1b7bee6916246c4b2b2cfa7b490a`  
		Last Modified: Tue, 16 Jun 2026 00:16:58 GMT  
		Size: 40.7 KB (40690 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; 386

```console
$ docker pull php@sha256:57be90b9e841a8681d19cb72464d7326378e91eee3d0212dd1c7022c7c1e7fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44872340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5713b2e8b7c33a3660a89ca9fa3ef7a5215b5c7c4317dcd2ec96941f15cab9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:13:28 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:13:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:13:28 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:13:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:13:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:16:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:16:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:16:39 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceb63463dd02114d0fd78eedac3258ee552439c52317c172967cd809efa9b8d`  
		Last Modified: Tue, 16 Jun 2026 00:16:47 GMT  
		Size: 3.5 MB (3497281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8386cbb1d4a049e5ce47fd54ca4888767e59f856b205ba77e077ada67346097e`  
		Last Modified: Tue, 16 Jun 2026 00:16:47 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f0b392afe9a26b84a1c54d95dd760d78b21c047ec83bcd11b850b913d79933`  
		Last Modified: Tue, 16 Jun 2026 00:16:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22002453fa86264092457cbd724b82383ab2b19a8f4a2fe92012b33e1a9560f`  
		Last Modified: Tue, 16 Jun 2026 00:16:47 GMT  
		Size: 14.4 MB (14421097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f9e947650b18c0fb45e3320c7b3f6d64da0014b8649997582c50b0e6083990`  
		Last Modified: Tue, 16 Jun 2026 00:16:48 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d298cd36acdd29f1579e87f0ae6de307d7247afd54757970afd65e7424ac9c13`  
		Last Modified: Tue, 16 Jun 2026 00:16:49 GMT  
		Size: 23.3 MB (23257385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5019a7919ab9520811f870091698d87daca1e68349767ee2387aa8c636b75307`  
		Last Modified: Tue, 16 Jun 2026 00:16:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57b37169a564ce17993fb2baf948462d0ea90b4311351a1346004aa5728789c`  
		Last Modified: Tue, 16 Jun 2026 00:16:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:ad08ab0611d69de682ec09a15f45eebb4a337b99150811e47d66fe2129159aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 KB (303011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c9ce1453909085c1adadc6795b8790f27371d4e66e85b4434f9eb6c498e36`

```dockerfile
```

-	Layers:
	-	`sha256:50d1d876d754983b29bfac137d85466cbc4844fffa30c87675bb3020b7e22917`  
		Last Modified: Tue, 16 Jun 2026 00:16:47 GMT  
		Size: 262.7 KB (262745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5001bfe1f14dd34437a796909a6776a8c6e1c8f9896b5cfb9af25bca1ed1fe`  
		Last Modified: Tue, 16 Jun 2026 00:16:47 GMT  
		Size: 40.3 KB (40266 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; ppc64le

```console
$ docker pull php@sha256:4c4b33de438da3787e5283f402bfdd253a625ca734d365d84091da7a6bd01d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44810118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb5095d89721b55064763a41fd0849fdbd4ae21bf6dca79ffeeff0bdb9066a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:17:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:17:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:21:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:21:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:21:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:21:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:21:15 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b9da4fa7a0b9d4db76eaa5e7475a9b26aebc92ecdbad7795d33e8c5862bfa`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 3.6 MB (3637828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72717bce2b969f044f4c03b530bca77062f0b0d4dfc1eb2f53b9a1459bcf77c`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecffaea7a9240f30a6d71b76e5cba5e41c27f6ab0409cce52536feeb7b55db`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38963ea696c0baa30897d72fa1c115b549abcd0ff8afabb7e64dff601dad030a`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 14.4 MB (14421124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdf993820811354bc778a92c8fe5650e39118fea0109698110c3a5470a1537a`  
		Last Modified: Tue, 16 Jun 2026 00:21:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde44406cc832a31515595adbe3cbdfa66f3287da614d0842bb808007f4955`  
		Last Modified: Tue, 16 Jun 2026 00:21:32 GMT  
		Size: 22.9 MB (22911495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93afb5d986b66ba6a4772fe88c04dc7464a59241fa9d566e9de44a0cd2905ff8`  
		Last Modified: Tue, 16 Jun 2026 00:21:31 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19439b6e66d0162cbe7b6fea221e4f12a3dc69073713306d54a9b32aadf45d68`  
		Last Modified: Tue, 16 Jun 2026 00:21:32 GMT  
		Size: 22.2 KB (22183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:b030edfe54629ac3f5ed9069fe0181a12143a6960bbc3220dae88a7dcd1369e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d8551266961b438a7a7fcbfee0296dc330cd2d935098599227d4beecff7eca`

```dockerfile
```

-	Layers:
	-	`sha256:f0c2372a45ee3fee37ac2666e073df02ba45d4b8aa8e16ee6f9062a98e6d838c`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 259.3 KB (259295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3519f297a92026b2b7e0f67dac4ba6681c71a4704fd14d3f0fc8037db796ba`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 40.5 KB (40494 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; riscv64

```console
$ docker pull php@sha256:f0ebf2876e63f944f3ba90c91953a24e51498cf85536541487dd4a6a657946a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44804328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c418c3fca744211f295a42c8c2b7fd8f66bd92bf49689398593e14ac33d8e596`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 04:52:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2026 04:52:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 04:52:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 04:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 11 Jun 2026 04:52:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 14 Jun 2026 09:56:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 14 Jun 2026 09:56:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 14 Jun 2026 09:56:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 14 Jun 2026 09:56:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 14 Jun 2026 09:56:51 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1dc2b0247d9ffb9aa950846edb9cd66b4f53852a8a9879e3b90eab1e6b59a`  
		Last Modified: Thu, 11 Jun 2026 06:26:26 GMT  
		Size: 5.8 MB (5791702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6ded20d49de2d129bbc9f97fb6b326363a5b54d9bd6c73e47dee306b314693`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f977f288e84989a2379a82f5f4195784dcdf513d90a9d1c0069a2c531162f0d`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c51303935734568446c07e9e6bb9eea9bf61706e0cde61759feda9703fded49`  
		Last Modified: Thu, 11 Jun 2026 06:26:29 GMT  
		Size: 14.4 MB (14421889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991c412cc8ffd7f1daa3164040df08522cce407cd4f6ca38b90f8487651e0d1`  
		Last Modified: Thu, 11 Jun 2026 06:26:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb389fb135d0622b28c780a8d37f73302b3ca61554ff99f637a913a709b31f3b`  
		Last Modified: Sun, 14 Jun 2026 09:57:58 GMT  
		Size: 21.0 MB (20971753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8c9375f64019c0380c823e0828a517bc8c877fdfda8614ee1d8e8924fddff`  
		Last Modified: Sun, 14 Jun 2026 09:57:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc71d87551e548019816820e5c15881f28f5bfb8877fc65045858e229c2234b`  
		Last Modified: Sun, 14 Jun 2026 09:57:55 GMT  
		Size: 23.0 KB (23040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:c8f38b2249988bb60f36afdbaf9cce6779cc8815a8e97a967174e7f9b8464769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 KB (316677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f5f92bcc467e92452a912c29f8ab816059582c7ffd2dc4177f967ed818c663`

```dockerfile
```

-	Layers:
	-	`sha256:9aa1739d0673e8eff6ec41cb195cbc12eb267fc9bb9bbbe89a5be535e1023427`  
		Last Modified: Sun, 14 Jun 2026 09:57:55 GMT  
		Size: 276.2 KB (276183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4310feddbb268cedc0064e09eef467d0d028157394c4420375947c51b1335f7`  
		Last Modified: Sun, 14 Jun 2026 09:57:55 GMT  
		Size: 40.5 KB (40494 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine` - linux; s390x

```console
$ docker pull php@sha256:892929426d874b991efb9cd9265c51cac8c1525c5a7ce604edb15824def5d7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43460572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07c745860928273bf7e2ae82b8aee935d2039157f63380e7990574ee6c5050b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:13:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:13:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:03 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1478be2c88d13000249832224bb580b87a524c10ccf140e1f65943cb33f59eb`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 3.7 MB (3651068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4532b14d23ad0cd16945b31df22f9a393cc7b3b64f7aa7fa62ade4877c52fad9`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d62373606e3c4c1b6fef638aa78a6674eda0089fb632b2f1eaa05c504adeec8`  
		Last Modified: Tue, 16 Jun 2026 00:17:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978d8397ff165fecf0755837044bb4c2224d9880d02afb6691e590bcfad94d3a`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 14.4 MB (14421093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eada8c4418666beed553a70283b1751e2dd51e01d02f3201a903d1e65b2ad2a`  
		Last Modified: Tue, 16 Jun 2026 00:18:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7250956ae1fe08ac913d2f3295b26009ffd0bdb5663fe89ddc793bb5a01a7`  
		Last Modified: Tue, 16 Jun 2026 00:18:20 GMT  
		Size: 21.7 MB (21652867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6e9cc114191002aeb110aaddf2e2e3a6317c6f437743da5fbaace474851ab9`  
		Last Modified: Tue, 16 Jun 2026 00:18:20 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afb7d92225ea4914b4498d56cf0c11e0c8bc1c58059f3687f623d6e7f1f7db6`  
		Last Modified: Tue, 16 Jun 2026 00:18:20 GMT  
		Size: 22.1 KB (22144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine` - unknown; unknown

```console
$ docker pull php@sha256:2b51dbf9f14589ce81e100bffbd840237148448b4f91f80e66c33c865fc3f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 KB (299557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be158196dae1cd5d89e5f88eec570596420ae4602b75068a3cb489cd5c4a277`

```dockerfile
```

-	Layers:
	-	`sha256:505343bf7d0664213d5bfcbfa19799f8022b48d18702adcf349d16480a597c7c`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 259.2 KB (259189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0d24f6633ddd785ee55d3fdf2d1de0d2ea26bc17d34b589f376d3a317057b1`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 40.4 KB (40368 bytes)  
		MIME: application/vnd.in-toto+json
