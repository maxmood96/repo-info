## `php:cli-alpine3.21`

```console
$ docker pull php@sha256:fbaae9d17cbcb784a92be5e6de7b39848e306b221ef0edb218c832418797c8f7
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

### `php:cli-alpine3.21` - linux; amd64

```console
$ docker pull php@sha256:6338c0bc70c8a8b1699fafac1cb0cb15d71825b2b8e7b131989d6f239daa8615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41455397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feadc38ef62c7eb5a19002088e19da0d7809bae64fa215f4fc1b1a3e13191d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d7388c5fe6514bb942543c558c7cd7c24b4e81b2cf5be0c9e371d6dbecf63`  
		Last Modified: Wed, 11 Dec 2024 23:35:56 GMT  
		Size: 3.3 MB (3335081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adea0a37ec01acd4f78beb104975511fa18adcbd7e5e3ea0b22b6141501ee62`  
		Last Modified: Wed, 11 Dec 2024 23:35:36 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef563a2c247d9c4c35317d6d1f400451fa3de0f63ce71780b9b8f4e1ed7454c0`  
		Last Modified: Wed, 11 Dec 2024 23:35:36 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5beeb7f186ecf038d48430751b5fd79fc98c421354f88bc4b09bf34339e1b0`  
		Last Modified: Wed, 11 Dec 2024 23:35:57 GMT  
		Size: 13.6 MB (13573068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c24c159ba3c264ccd5428dc940f4840b8775eb4af4f781356941a3daf674e3`  
		Last Modified: Wed, 11 Dec 2024 23:35:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226d772baf39e742d08876b0538d1948968b130542e5aeb6b988e3cb21c7888d`  
		Last Modified: Wed, 11 Dec 2024 23:35:57 GMT  
		Size: 20.9 MB (20878650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1608480e0d28756ab41d47c7a95ca6256ee1a35905ca4a657e0aad6aa749315`  
		Last Modified: Wed, 11 Dec 2024 23:35:57 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaa50ef877d0f2856bf591cd5b463f44053fdd7aa02e53ee2b28116bc2ca45f`  
		Last Modified: Wed, 11 Dec 2024 23:35:58 GMT  
		Size: 20.1 KB (20065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:d401f64e121dadf7a9044262ebb918ae8900328ec835913eab9ec822e469ddfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 KB (312364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e20cd72ed5a8b03673c5a00d8fa039025091a00b86ea97864ca8095c24308a3`

```dockerfile
```

-	Layers:
	-	`sha256:90a96e789a8e6dc41b7a1f5e2c584d79a8213373dd85e83afca814be8506c7d1`  
		Last Modified: Wed, 11 Dec 2024 23:35:56 GMT  
		Size: 272.0 KB (272041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9495efc832c7b1c8553e28cf2d90f5dae2afdd1c057987d23ac55023bc2045`  
		Last Modified: Wed, 11 Dec 2024 23:35:56 GMT  
		Size: 40.3 KB (40323 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull php@sha256:2705243f656b3ea75f3e3a33cbcac2dff267d51d6653d69f22ad10891fee99af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39288742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7ba272a0f3ad884cc884f05a056feef4932067cebeafe5ce8a01171da3495b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626ecd80716f5c5a684662046769c61c669d292084ebe6f9300b07542470fe7`  
		Last Modified: Wed, 11 Dec 2024 23:46:06 GMT  
		Size: 13.6 MB (13573094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558011eb01fafcdfc6d1a5db0174996f259d322e58c6bbe550960e2b86d1844`  
		Last Modified: Wed, 11 Dec 2024 23:46:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bf72cf55221fb1b2f81787b0af76afa6254a8acfbb7f7a8cf9633586af75c4`  
		Last Modified: Wed, 11 Dec 2024 23:46:06 GMT  
		Size: 19.0 MB (19021593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55da406a06928e7e85f34ec4e5f86abe0f0fd366088b780ed1b3af5d32acdf7`  
		Last Modified: Wed, 11 Dec 2024 23:46:05 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41ac1df5cb451d60623567c2995e597d2b57e90aefd508e88c441048ba7b157`  
		Last Modified: Wed, 11 Dec 2024 23:46:06 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:a0ca457533c0ff62f939a40b215312cc6c0dc02d8afd87266786e3d3480550e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899abc6f2e23d775d7ee147736e07cd54f0688e70ee44cbe92ab5689039c336f`

```dockerfile
```

-	Layers:
	-	`sha256:87fb9b9f933a93d9340fb1773e763fa71192cb01a18a88b0f4ac40f1261e150d`  
		Last Modified: Wed, 11 Dec 2024 23:46:05 GMT  
		Size: 40.3 KB (40343 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull php@sha256:718204c59b4fc77216a1e0e1d0828e7121de35160974c2702f04f66903729fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37832954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448818d74ce8894e367e3c7494e40a3f5d1da07141cedaafad73fc1fd444bfd0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46234f84a591182641b5590fe4e04a71ddd05a47082e61983e6d868dcc79cdfe`  
		Last Modified: Wed, 11 Dec 2024 23:48:08 GMT  
		Size: 13.6 MB (13573104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f3109f721f75e7b84cc380538d75d2799a5dd2df9204d6c2fb3347e2e4cb1c`  
		Last Modified: Wed, 11 Dec 2024 23:48:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1032e4e0d1857a66f1db76b6b06bf00fe9bcb67eef14cdf966e348d41fe4b4e1`  
		Last Modified: Wed, 11 Dec 2024 23:48:08 GMT  
		Size: 18.0 MB (18007586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e89a7b585564ab7b084767bf03a9052f4015367c5ae3d17854d425dc320d99`  
		Last Modified: Wed, 11 Dec 2024 23:48:07 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47c402044ea9703c4e6fef3fe4d19971835ccada29ab91a3ddb04f4d520b412`  
		Last Modified: Wed, 11 Dec 2024 23:48:08 GMT  
		Size: 19.9 KB (19896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:63e7aa4c61fc0c25e98287e11a37e6081ad9d3fbe8cbbd9e5e8297a0616d2ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 KB (309917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48df1a14c1d4ad5f6def09dc8153857a0ec36097214b98aea9e31f12716d260`

```dockerfile
```

-	Layers:
	-	`sha256:1b0250ccc8e2dcc43304b420b970dd2ef73bcae8729422d7f98e6b5afc2dfd9a`  
		Last Modified: Wed, 11 Dec 2024 23:48:07 GMT  
		Size: 269.4 KB (269357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790973d693b2b90ebefa626ed2b9e64612af24eec5098780ffd773a25abe653c`  
		Last Modified: Wed, 11 Dec 2024 23:48:07 GMT  
		Size: 40.6 KB (40560 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull php@sha256:bed0be47eafec1214bb66d7b280a44678b89cadae25f95ee98465b6f96a41f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41353247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b20dbcfc007ec34195339e52fbcdaf5864d8a965dc19cc60d3b9424560e0df4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:a6ecec5e4fe733d58ecfc6d3da08be13be94b6bf75fdd64d80a278e2542b0fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 KB (310071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f100ad1b59e1ec9777591bd46eebd5fd77075a6349b6ab288af3d12d89fe15`

```dockerfile
```

-	Layers:
	-	`sha256:50aaf6eb65fb3ad3f764f898607ce4abc2d9773dfdb23e208e1269fc3d425982`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 269.4 KB (269425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894d3de607f30dd2955cf9ee2783aa7cb8a91904b07bc0cc7a3abe8666ca5366`  
		Last Modified: Wed, 11 Dec 2024 23:45:42 GMT  
		Size: 40.6 KB (40646 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; 386

```console
$ docker pull php@sha256:e25b0f79d0277df91ed88e6743d3ca3ae62745aa90d41b88946856fb3b5e6c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41832338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e477eb21640875b04d1c38c87adde4bb9fbab0a5aaf59d717eabe9160b164dc7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130200741b6916fbd8d40aba0be3416844d352e81080484726c5d93484cdd78`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 3.4 MB (3376215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d530c0e6934798b4dedf2bf65c3370d88f2cdeb0557d47303a7cece6539428`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb82371a0c17328001566c01f034162e8c082082318b31c52940a8a5906dcae`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c9b22a7ff6ead8a489159b7505cfaef4ca2cfa78b567febdfab08299862d0a`  
		Last Modified: Wed, 11 Dec 2024 23:35:44 GMT  
		Size: 13.6 MB (13573035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5101d76cde2d9f131eeef9da812184f04b55517d769c7020f90d644e5887c40a`  
		Last Modified: Wed, 11 Dec 2024 23:35:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c227d195b793d62ec981e0cfbde75fd55e53f31aea9d86878abf11ba7d4a0a6d`  
		Last Modified: Wed, 11 Dec 2024 23:35:45 GMT  
		Size: 21.4 MB (21392844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925807cef5f2d0130364adf66277f09eb0d3d86c2c500568364abe46f8969012`  
		Last Modified: Wed, 11 Dec 2024 23:35:44 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c52a6b3ef279541a18ae310efa6b2e327338ba80a5f3030e06e61aa0bae534`  
		Last Modified: Wed, 11 Dec 2024 23:35:45 GMT  
		Size: 20.1 KB (20066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:c2a63faf8613b3f0b01bd763331ea3be3a6dd8f39b10717fc2e4fdba05d5ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 KB (312177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97d3dc4f7082f740b2e913dcfae91502452fd0238f8bc52fb26a941fada4143`

```dockerfile
```

-	Layers:
	-	`sha256:c41e70b217c48eb123711913dbe35b169f5d5c669daa1a39740432fb9cc254c2`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 272.0 KB (271956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d6eca1652e9dd1e34c9a073490e99668c3535165e643b591247fe7723a337a`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 40.2 KB (40221 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; ppc64le

```console
$ docker pull php@sha256:c7b92fad372147c4fcb69b2c6e092b7454535ba7251493b11ed6d8dab5075a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42441930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccf2d738c78315a74e4becb52d90f0531bb2c640f0556f54ca6fa0bf0e5c89f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3708563094bdeb69b89124b79d07a1f082713efec0e595c079930180fb6d4955`  
		Last Modified: Wed, 11 Dec 2024 23:42:30 GMT  
		Size: 13.6 MB (13573079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a7589b163bca027b4edba09f13de85c98ca7f239d8d9502595b0aff0e783cb`  
		Last Modified: Wed, 11 Dec 2024 23:42:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548da7d6eab64d478fa836008ecc7f95ebd4a4aa71d2b6da4560b0e0cc46da36`  
		Last Modified: Wed, 11 Dec 2024 23:42:31 GMT  
		Size: 21.8 MB (21793490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534019866156f0b17387cf5bc520db618ab31433a048838bcc739ccdc5c2b390`  
		Last Modified: Wed, 11 Dec 2024 23:42:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bd21e46907d930fc62044fd41a7925f4ebdb1a5462a6638c80fd1cec3b451`  
		Last Modified: Wed, 11 Dec 2024 23:42:31 GMT  
		Size: 19.9 KB (19890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:e47726e2146a01097d5c06a400507d406f2b6487b2bed19895023474409ed8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 KB (307826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3e80a53e35458b3345b7577056d7113ac03b01198bbd228d1c90e9013355a9`

```dockerfile
```

-	Layers:
	-	`sha256:f4be6d4a1d183e676d24ad885fee35a26b5312951a3f12cb3e27f3b8aa4fc7e7`  
		Last Modified: Wed, 11 Dec 2024 23:42:30 GMT  
		Size: 267.4 KB (267377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75bf2fb87eff2526670c664b5ad77eebd01de58a9a6a82fe5f14f0b7c94ac281`  
		Last Modified: Wed, 11 Dec 2024 23:42:29 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; riscv64

```console
$ docker pull php@sha256:ee150f8982406e213959e50d3a451115621cf0438c71c2ab19f312b1d49958a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40710611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee60d920f2f47d3b2602c76beb8b363f144458645c75e0ff734429ab52f2080`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:9e0f693f8ce218098f1dd4e5f68544270a03f5f684085e97b9456fc5eead8fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 KB (307822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28b5c7b71551e128245d7d8533540fe39bf859d41cd8f20e5e483ae710a6efc`

```dockerfile
```

-	Layers:
	-	`sha256:fa8c710532ff60799284e1e09fc68d0b2e405d52d80a8b7a433a69f03edb16a0`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 267.4 KB (267373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82ab09bb7a0972306e20fd7c5c45dde92391436f549ac5451f30a46e4b61591`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.21` - linux; s390x

```console
$ docker pull php@sha256:7becc73c27ad5e33d93ab4864f6bfa9135b33b013fcba4687f1a62e42af487bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41990437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17116a76d955393ec1701d54694d37c334c44c14b732159237e2a876c75596c5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:ab4ba23deeaa2fcccb479d5300ff38481a3b15ef219d1774cf3759189deffdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 KB (307593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb124d628a7a28346e7c48e464ecbd9e49f6851655b86e2e18d247bf2ca7b924`

```dockerfile
```

-	Layers:
	-	`sha256:43d3455b12297e5705ca07ba2fc9312d222197eae54b0d11e79bb1218860c951`  
		Last Modified: Wed, 11 Dec 2024 23:44:52 GMT  
		Size: 267.3 KB (267271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ec8184414e564530515e39a89fc52c3e4adee50a2884511b581902358218e1`  
		Last Modified: Wed, 11 Dec 2024 23:44:52 GMT  
		Size: 40.3 KB (40322 bytes)  
		MIME: application/vnd.in-toto+json
