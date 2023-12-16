## `wordpress:cli-2.9.0-php8.3`

```console
$ docker pull wordpress@sha256:e7ae8b6689ff538dd23e2d11eb7d7b98adc677fe4e5cc8a75be373c3a1491e95
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

### `wordpress:cli-2.9.0-php8.3` - linux; amd64

```console
$ docker pull wordpress@sha256:773e8316de6a587447842c8ce20690bcda3ea87571f30eeb99bd8c0e541d7730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67797266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28ec8628deda144862a3e7c4b0caf5f349cad3198cea48e55e2efa53f542894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:d6970d99b9a10b135bc761aac8d5e43a8a1610cdec9eef9619fc11f567578fb4`  
		Last Modified: Tue, 12 Dec 2023 23:26:37 GMT  
		Size: 12.5 MB (12452290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621aa29822cea27221557011785bd84ebc6bc2de17474a67b0b9894da5724ed9`  
		Last Modified: Tue, 12 Dec 2023 23:26:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936cd71d98ae0d6d6b36582a9c0a89fa817c815764a2b06beb3a444f45c94b4c`  
		Last Modified: Sat, 16 Dec 2023 06:43:25 GMT  
		Size: 17.2 MB (17240063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4c41540b847de55ba8c21db96959148ccfd795bfd686ebbcbdff3a59f5f4d2`  
		Last Modified: Sat, 16 Dec 2023 06:43:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d714a88dbfdb65d4e9fa7b18777fae540c431a0b83b468a766ef90a710f5c`  
		Last Modified: Sat, 16 Dec 2023 06:43:22 GMT  
		Size: 19.3 KB (19287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23ddb3d681bed8ed94db227ecd442795561401a27ebeb8d81d33dbc7dfcebb3`  
		Last Modified: Sat, 16 Dec 2023 10:50:17 GMT  
		Size: 20.5 MB (20496706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c170394065a1d9f1fb730266e5909402ed3c103222d4b9c6ae70a5c7d07f5c6`  
		Last Modified: Sat, 16 Dec 2023 10:50:18 GMT  
		Size: 9.9 MB (9897661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b014518a1f0fbfe33c0086b6cd0762eeb32f37d08e19ae4a9241453899edc7ac`  
		Last Modified: Sat, 16 Dec 2023 10:50:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c2d39512378606f7e293171825790bd1a55e3f70dd308267ad14606789da`  
		Last Modified: Sat, 16 Dec 2023 10:50:19 GMT  
		Size: 1.5 MB (1521714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476fe0cb2a426e1528897b022535a1870fa09c351564e9c1a6dede1a2ddf8568`  
		Last Modified: Sat, 16 Dec 2023 10:50:19 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:3cba6b4001e0224d2c24b0c6fb840f34c13c393fac95eb2c4676917218d2d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749754bb0203d10ebf018d17418bc70dd3da195b049dedf5a4719f9151bc46c9`

```dockerfile
```

-	Layers:
	-	`sha256:5e71b60923b972d0177855237bf5b31f9a44edfe5d8ae8926b853dfec89896ee`  
		Last Modified: Sat, 16 Dec 2023 10:50:17 GMT  
		Size: 1.2 MB (1175524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1960f65d014b0e110dc0a6796be8cc87d7efc869191062a8a2f8216d0a002a18`  
		Last Modified: Sat, 16 Dec 2023 10:50:17 GMT  
		Size: 42.2 KB (42230 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:e6de1abcb4e38941661b3878aeb20f7c0b8f5884b176c0da3c9f74ab04d779dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64273884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73556605b14bb8dd36a6763ed15075a4eee0869077933af724753d9222a95c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:b685965178c3b16eb767adeac66568def914dac6c889e0a31d66eb02614bbcd1`  
		Last Modified: Tue, 12 Dec 2023 22:12:14 GMT  
		Size: 12.5 MB (12452307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac96e1f59001b1557c375aeb6f7585c80fe4b34bbbe8751fe83b065e104e6d07`  
		Last Modified: Tue, 12 Dec 2023 22:12:13 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab45c5097a1bb1319aad3dcc156376900bdf45c1b26fcc63082a288ca529bcb`  
		Last Modified: Sat, 16 Dec 2023 03:33:22 GMT  
		Size: 15.7 MB (15746401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f139a42fc3615770300f9d04ab21de1bda55d2716b35f7aa4cb2592169f7121`  
		Last Modified: Sat, 16 Dec 2023 03:33:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b78f2fe0a41c41095f2ffb91e90f3a25aadf66a7b6bc8ef5db010a38efa970`  
		Last Modified: Sat, 16 Dec 2023 03:33:17 GMT  
		Size: 19.1 KB (19125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f2439b8138434a429e0d4333da52bd2b49cbb56d5637c58b71733d4b52c179`  
		Last Modified: Sat, 16 Dec 2023 06:02:04 GMT  
		Size: 19.4 MB (19445781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23b1861eece16e8e1a895823d879adc6880ffe094abae0ca4cfa8c646f2237f`  
		Last Modified: Sat, 16 Dec 2023 06:02:05 GMT  
		Size: 9.2 MB (9157037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb71a078f80c57e90345491ecdbda895c07a8f633a73fbd8930de13fcadb8c6`  
		Last Modified: Sat, 16 Dec 2023 06:02:05 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb660220b78a11281842212604b6e20ee624122c1b9e9c3f5f8a1c82a8ca110`  
		Last Modified: Sat, 16 Dec 2023 06:02:05 GMT  
		Size: 1.5 MB (1521712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec4ede834bed918095e569de3a664ec9a67fcca5f0a67681d3410ce832c0a36`  
		Last Modified: Sat, 16 Dec 2023 06:02:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:ebb4856f4a0bbe3b542ed4eb2f76351a75df0f2f320f13d27684fd01eeb12d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2020e1e30cf5b7cab3f3f8c99728500e6d6e2629f3fe3d5c6c9418b3f981cda`

```dockerfile
```

-	Layers:
	-	`sha256:466fb20e508ad432005766d277397ab5c60cfc4e71f77e705c54a7ee5745026c`  
		Last Modified: Sat, 16 Dec 2023 06:02:03 GMT  
		Size: 40.7 KB (40673 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:95965a129ef348ba020f55c0ef0b04bf1aa48fac4e89f94f26d4cefadba1d31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62036791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7524589a62c197b4247de2ece94afcb250214063f5591db1848fad7ef457c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:4ddf5abc1a8a8bb146e597add8c4284e903d7f0a09f00292102e93e0e3fa993a`  
		Last Modified: Tue, 12 Dec 2023 22:38:31 GMT  
		Size: 12.5 MB (12452302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510df02f5d6b2d77584d0653e06fedb81b8cc5900ab00ca1e5cfd28c27760a9`  
		Last Modified: Tue, 12 Dec 2023 22:38:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c9a32de68b1d17752f1e673764a13c47fcdb6aed420b9ec720486afdb806be`  
		Last Modified: Sat, 16 Dec 2023 06:14:19 GMT  
		Size: 14.7 MB (14738071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec82162d045fc2923b419563c6b208fd0246e4c12c98e84e4836243a1f3e1c71`  
		Last Modified: Sat, 16 Dec 2023 06:14:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63407f96746eefa5c976028560e9690b5d9c16c442e5c1c7af6889312a020f99`  
		Last Modified: Sat, 16 Dec 2023 06:14:16 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce65ff3e6c631f83636b6be81d721b9cd2f2d391e9a38766ab8ced7c3055bd`  
		Last Modified: Sat, 16 Dec 2023 13:01:24 GMT  
		Size: 18.9 MB (18938839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b903d623441f9b97bdd7fb0cbf6b4ef2708adcb6570c7d96522b8cc248a4421`  
		Last Modified: Sat, 16 Dec 2023 13:01:25 GMT  
		Size: 8.8 MB (8834088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9532e641d58e4624782eeadd754431b55dafcc8ffff89d2ff22622b7feb3855`  
		Last Modified: Sat, 16 Dec 2023 13:01:24 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bef0416bafa0ddd211f41306e7c019a4bbda04c165dbb5bec141d52120cdf04`  
		Last Modified: Sat, 16 Dec 2023 13:01:25 GMT  
		Size: 1.5 MB (1521689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6dc12165d3369c3d076ae82af7c0cbf82917758fa74e089dbbc47969bb255`  
		Last Modified: Sat, 16 Dec 2023 13:01:25 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:d1cf4d7ca309f9a5f24480ac911552f0556f27f8aa1a1556b917c105d6224881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66073a31588207bcbada659b8265c0775facb78336a5ae5623bebfff42fab240`

```dockerfile
```

-	Layers:
	-	`sha256:cb335a79ea432686b0f39c47e5df2403065ea2eb02c79511add45f12b39967ab`  
		Last Modified: Sat, 16 Dec 2023 13:01:23 GMT  
		Size: 1.2 MB (1175560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3deaacc300b23a48fbb33b9c70f8d4b75b012f99e89bd88793b5925dde75029e`  
		Last Modified: Sat, 16 Dec 2023 13:01:23 GMT  
		Size: 42.4 KB (42352 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:61704e979874ccb4101a5eb91b4140571e42f4db089706696c23dcebb9499530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67629238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef65ff1a4c7eae2f0a2e6c6ab942a45c88bfaeb9d430f907eafd8667b8373c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:d4b6d892bc61713316e58b3b40ab8de5a7487c72df7536a64f2243b499b07351`  
		Last Modified: Tue, 12 Dec 2023 23:02:49 GMT  
		Size: 12.5 MB (12452306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07409f498678a1811f0c075d86d88701eff2478c5c034e1bfad340eab4b187f3`  
		Last Modified: Tue, 12 Dec 2023 23:02:48 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00222801a753010bf6ca435b0edb6df680deaf0b6ac54d88f110bd64d2a5cf5`  
		Last Modified: Sat, 16 Dec 2023 06:01:19 GMT  
		Size: 17.2 MB (17211460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fe6bb9ed6f8237d7b0807e3ded3f3f5c0c9e876fddd0f16af89794333aac59`  
		Last Modified: Sat, 16 Dec 2023 06:01:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28031130c5724b40094cd3d2d5d88ac0296681e2a1e3fc37de17c5b302c6af`  
		Last Modified: Sat, 16 Dec 2023 06:01:17 GMT  
		Size: 19.1 KB (19085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77d5ec03bc2c1de4a00dd7fc6dd418287b56bf2f43fd25b3d5f009cded5cd3`  
		Last Modified: Sat, 16 Dec 2023 22:33:01 GMT  
		Size: 20.8 MB (20792357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a1ab4d42b279df1295407194fae9b72f67f4801f3a902ac1365610461e88d2`  
		Last Modified: Sat, 16 Dec 2023 22:33:02 GMT  
		Size: 9.5 MB (9469050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8a70525be293624bb1f1f6fdeb6a239d2307825c024332a039b923fa370bce`  
		Last Modified: Sat, 16 Dec 2023 22:33:02 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ee2854e8a828336289724f3c8ff68dbad0fe98689b88d91220fc3a315637d8`  
		Last Modified: Sat, 16 Dec 2023 22:33:02 GMT  
		Size: 1.5 MB (1521643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3801c9454e20d11e348409eaee3b207339fd85002d42b86e2e535dbdd05a11d`  
		Last Modified: Sat, 16 Dec 2023 22:33:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:86812d207a42c7dd3c9e74a301e0b5d9127f671910cae5104adfb094a34434e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1216311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e09091800fd2e6ec96ac5c8f9bf2b56d1d130d8c6b4bb317aa98ffee2ea297`

```dockerfile
```

-	Layers:
	-	`sha256:c148b1d23cd62bd08c89398cbed4713785dd10ff8b7f4e7ff457e4bbcb2153a0`  
		Last Modified: Sat, 16 Dec 2023 22:33:01 GMT  
		Size: 1.2 MB (1175535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee8b9f08292fed3fdc5602cf7801b9540feafc121feafd3834de806733523c39`  
		Last Modified: Sat, 16 Dec 2023 22:33:00 GMT  
		Size: 40.8 KB (40776 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; 386

```console
$ docker pull wordpress@sha256:a6c177c99d05f6965e86314c6c242b221e563d0bd97e68bc99ed6b4bf69b8aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67910721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642e4bc49b6b601a3b41e23bd501b084db74e0a13e4eaed3e171ecb97054e9c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:e25570a3ea487bec2ff6666f653989c75aebe33565a52454485364190f01703b`  
		Last Modified: Wed, 13 Dec 2023 00:36:56 GMT  
		Size: 12.5 MB (12452294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1b56cb05998b29c1609da285a926cab06b1e91ec335a18e588621f69bc695`  
		Last Modified: Wed, 13 Dec 2023 00:36:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c054709cd1336216a44c84a2d5001b69d17d70deb33f5ca4090227929f1de0da`  
		Last Modified: Sat, 16 Dec 2023 10:07:47 GMT  
		Size: 17.7 MB (17671315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3212f3e12aeea50723b72e8aaec8a71486672f97c269fd12fabbb4a06c56b604`  
		Last Modified: Sat, 16 Dec 2023 10:07:42 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b40726a87702837c64654ea195ef7abebfb4a6e08f71d6ba51cd784efde7e10`  
		Last Modified: Sat, 16 Dec 2023 10:07:42 GMT  
		Size: 19.3 KB (19288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b343ddce9c94dd1c7e26b3a71b726929d099e735d91c3699532692c201cffa`  
		Last Modified: Sat, 16 Dec 2023 21:50:30 GMT  
		Size: 20.2 MB (20159429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd16bee90850467210c0e58aa4d02e371a8ad0285b87978ae2bdae1cb79774b6`  
		Last Modified: Sat, 16 Dec 2023 21:50:30 GMT  
		Size: 10.0 MB (10016363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabe05c55b6845861d6409c1cc7ee3f61b800a9b3c6efc555690a806c07a81b0`  
		Last Modified: Sat, 16 Dec 2023 21:50:30 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eed370fc56cea91966a7aa07092d680b5080c022aab6e2af82d4d149dd4e8e6`  
		Last Modified: Sat, 16 Dec 2023 21:50:30 GMT  
		Size: 1.5 MB (1521672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbb578e4022b73c19e24009dc3494463eb09db99e97d8871ab042147a170810`  
		Last Modified: Sat, 16 Dec 2023 21:50:31 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:80e4ff3fa858ab3d302ad368922674f8084b9cdf54c5c210feda552e05dcba8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (41982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd4ea08ce7b349c8851d20dd05a24ceecb8699dbaa9707d2599e3dcc1532736`

```dockerfile
```

-	Layers:
	-	`sha256:f03fcd4c73b02102029b17db1b68640c436a97d5c077812cc73e18a841884168`  
		Last Modified: Sat, 16 Dec 2023 21:50:29 GMT  
		Size: 42.0 KB (41982 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:bf4baac48c8fdeaf7d26a76740ceb786db74adfdde6b5d9b58353706a7873cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69617871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d545a745c5656ba616a626412c86c4e78a02b950e335968ffd7759b98212d57c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:f2c56763bbe66e30de393c4bedb62aaa78a18e5159b53a8290a58bef7a2324cf`  
		Last Modified: Tue, 12 Dec 2023 22:44:22 GMT  
		Size: 12.5 MB (12452304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aa011d78b3813c30fe283ee2bca58e38049e56fde0bece69b861d67aa6edf9`  
		Last Modified: Tue, 12 Dec 2023 22:44:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d289060da250bd2ac78a6f2fbc8270588d8f011a5435b9ffb5dc91a90634860`  
		Last Modified: Sat, 16 Dec 2023 06:08:54 GMT  
		Size: 18.1 MB (18114847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c40aff12c1a03e38fa21c9de2992b6315c794b94e4aa2e8d5d70e5240b3af`  
		Last Modified: Sat, 16 Dec 2023 06:08:51 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59e13505c56c5915c1b3cf5b35a5b4e4066af3dc7323626573c3966f077767a`  
		Last Modified: Sat, 16 Dec 2023 06:08:51 GMT  
		Size: 19.1 KB (19102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da079b7a88e1184ad6af506b5a3a3a8be11eeb78362e80d4df1f8d78f869580f`  
		Last Modified: Sat, 16 Dec 2023 18:39:49 GMT  
		Size: 21.3 MB (21340964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c0110408db8d785e567c876ea2305d609a3ca10ba4d1a87c2e9f55ee82d237`  
		Last Modified: Sat, 16 Dec 2023 18:39:50 GMT  
		Size: 10.0 MB (9966850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2412736d519bc357263ae4fc47e300584febd8c418553d1f5f75b61c54aba202`  
		Last Modified: Sat, 16 Dec 2023 18:39:49 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1019359414b07b4ec0dc0a3a1317eb27a83358ab60877d86ee4de5f2fca83b`  
		Last Modified: Sat, 16 Dec 2023 18:39:50 GMT  
		Size: 1.5 MB (1521697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5269e5d2ae2c9feb54dc8247cc35828518e72ae37b3e8f272c5aeef228b77e00`  
		Last Modified: Sat, 16 Dec 2023 18:39:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:3c99586182ba00285afa3473e5c29dfe3a4dde5fa2fa508bdd990bd45951630b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1214734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1201af45d53b2b3f743f2d756fd302dff9e9407fe02b3599a905282617b738e1`

```dockerfile
```

-	Layers:
	-	`sha256:474dcb8cda4c85f559a3ed5c163a4249043a148df4cf8511438262eed71bf968`  
		Last Modified: Sat, 16 Dec 2023 18:39:48 GMT  
		Size: 1.2 MB (1173922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9577f8eaf35b8c3225ae654828dac3530b138a39e57e778e8888ee4181dec528`  
		Last Modified: Sat, 16 Dec 2023 18:39:48 GMT  
		Size: 40.8 KB (40812 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.9.0-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:b167fa780a563e7afc1a0d97c9aedc5e019d5fdf98f4f27a44ae9bca880f7e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69510110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b07d7b4acf27a215e17a3006f95d0242d74f2d09af89d6e5528d6208b403799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 24 Nov 2023 12:37:46 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["/bin/sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Nov 2023 12:37:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_VERSION=8.3.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Fri, 24 Nov 2023 12:37:46 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Nov 2023 12:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Nov 2023 12:37:46 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 24 Nov 2023 12:37:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Nov 2023 12:37:46 GMT
CMD ["php" "-a"]
# Fri, 24 Nov 2023 12:37:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
WORKDIR /var/www/html
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 24 Nov 2023 12:37:46 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 24 Nov 2023 12:37:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
VOLUME [/var/www/html]
# Fri, 24 Nov 2023 12:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Nov 2023 12:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Nov 2023 12:37:46 GMT
USER www-data
# Fri, 24 Nov 2023 12:37:46 GMT
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
	-	`sha256:29229bf842a35e0f2fbaaf7d4ac99a03cd25e73c3d1e2b3cf7c9faa421594fe1`  
		Last Modified: Tue, 12 Dec 2023 22:09:01 GMT  
		Size: 12.5 MB (12452312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda911fba6baa41094156504359c3aa5e605ccda6527ca1c026c16b7f6e069fd`  
		Last Modified: Tue, 12 Dec 2023 22:09:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17abdf3d29187a38fda77f581f08b5932654b903d093134b86deedb79c2a97`  
		Last Modified: Sat, 16 Dec 2023 04:54:40 GMT  
		Size: 17.0 MB (16993551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b06a6ba39c7bdec98078b5c40fcd685ab646254fec37058ed4fadbda58e5d4`  
		Last Modified: Sat, 16 Dec 2023 04:54:37 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231f1f14a946d3911c533e73880e54f2a916f096ce4eb8cf9b6150bd4bf0cc4`  
		Last Modified: Sat, 16 Dec 2023 04:54:37 GMT  
		Size: 19.1 KB (19104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040dedf3f386f3371f3e7de7f85a5a75d2e53b3a2f4efc0818fde52f65e88c95`  
		Last Modified: Sat, 16 Dec 2023 12:59:34 GMT  
		Size: 22.4 MB (22407105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16723e0e43da044c1c8d308333f5aecfaabbcf70fc882292154146fd7767c0b4`  
		Last Modified: Sat, 16 Dec 2023 12:59:35 GMT  
		Size: 9.9 MB (9930694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19061dd8c167f6dc0f6af1b0678dd03fe9329980739cf75b1c4403d56ed0a1`  
		Last Modified: Sat, 16 Dec 2023 12:59:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6fed8707c86d1dae4e8520463d225f9b5ed452a3e2a4e79f53bd86e8eaa8f`  
		Last Modified: Sat, 16 Dec 2023 12:59:35 GMT  
		Size: 1.5 MB (1521708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280ff6e39baf5a77019db020177abc7cb1d6ca71b22e47e22a709fcc6aa8e75b`  
		Last Modified: Sat, 16 Dec 2023 12:59:35 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.9.0-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:22d2b5a5f7e8aebdd1a6369fd889ce7fd5a75eb6cfa347408ba6a52385a69011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1214654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384531da7eb866cee40cf0da509e50185ef679c261cf900e4572750bfb1bdb45`

```dockerfile
```

-	Layers:
	-	`sha256:131c3c0706eac54c624b4675ce14b3d5287d97d46c256739177f1443a769bd4a`  
		Last Modified: Sat, 16 Dec 2023 12:59:34 GMT  
		Size: 1.2 MB (1173888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f1a4eac32b7566e3684174ca7f9208e754fe3ebfd0c1d584c9da0c0180948f`  
		Last Modified: Sat, 16 Dec 2023 12:59:34 GMT  
		Size: 40.8 KB (40766 bytes)  
		MIME: application/vnd.in-toto+json
