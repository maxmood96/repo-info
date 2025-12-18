## `adminer:standalone`

```console
$ docker pull adminer@sha256:8f816804193e7e30f5725f4148a217dd5549579706b7d82204a26c18a32d95dc
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

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d83d52af8d2b8fb5106eab9709c452c863d6b5be2e8f26ded36a695bfb95ec4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46348378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7e9df3c2149d7649857f4145b075e41b3bf3974a6215d589cc26b908fd9cd0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:32:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:32:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:32:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:32:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:32:32 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:32:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:32:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:35:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:35:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:35:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:35:30 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 01:16:29 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:16:29 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:16:29 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:16:29 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 01:16:52 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:16:52 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:16:52 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:16:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:16:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:16:53 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:16:53 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:16:53 GMT
USER adminer
# Thu, 18 Dec 2025 01:16:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 01:16:53 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbe6da4182506efdc65616771e0c502245d613e6afb9995fa73ae065f701a04`  
		Last Modified: Thu, 18 Dec 2025 00:35:45 GMT  
		Size: 3.6 MB (3591430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3ffe6bee64250410d4cb5112f7d292156545c894a04e15bde054cacc4918fc`  
		Last Modified: Thu, 18 Dec 2025 00:35:45 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87e538da3e3cdca688357d89315634bfa02e28228e8743526d6bdea45599890`  
		Last Modified: Thu, 18 Dec 2025 00:35:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe31dad8ce61786a62c96b642352fffd4e50986abef15e672fdd0df4d30d1be`  
		Last Modified: Thu, 18 Dec 2025 00:35:48 GMT  
		Size: 13.7 MB (13676359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741253c470ee4fabef978c5f6aa7b63c925b1f84bc71ab7b19967fba25b69d4`  
		Last Modified: Thu, 18 Dec 2025 00:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dcef75feb31a502bad4c4bc257b2972b7625bcdd73a4fc8c36d9ca964fe076`  
		Last Modified: Thu, 18 Dec 2025 00:35:46 GMT  
		Size: 20.2 MB (20154722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259d03b7fc92a5bc5387fddc10d6cd7e365167b2ba67f80b1d76606762183017`  
		Last Modified: Thu, 18 Dec 2025 00:35:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215ae7e77b85a34c57ee282c0860adf0d185465519f20ce9dcd3b48f839a0d26`  
		Last Modified: Thu, 18 Dec 2025 00:35:48 GMT  
		Size: 23.5 KB (23488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cddc6bd0798fc73e83de933ecfd1fe7cb0d8ffe0ea0d769dfa06001b1dda40`  
		Last Modified: Thu, 18 Dec 2025 00:35:44 GMT  
		Size: 23.5 KB (23509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24afbac349d14f0ceab967fc6f146bc03fc4e31cf6db84c6b2695f09f0d10970`  
		Last Modified: Thu, 18 Dec 2025 01:17:04 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b307537566d885a9eb85db0566c6b469a4985f629eb2545aab87bf3f0a01085`  
		Last Modified: Thu, 18 Dec 2025 01:17:04 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fdc65e2a85f458085a0cd238290387ef991b01b3fd247690ef9a7f991b47d9`  
		Last Modified: Thu, 18 Dec 2025 01:17:05 GMT  
		Size: 4.4 MB (4370236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19763c8d4fa2d83072031a02f64b21f444d2ae6aac26dcde7f58d52d9a19f634`  
		Last Modified: Thu, 18 Dec 2025 01:17:04 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cf9bb3330ec6355db27ea412c8e5c6a4adf37b7a0de9fc24d255a4286fea99`  
		Last Modified: Thu, 18 Dec 2025 01:17:04 GMT  
		Size: 640.9 KB (640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fef2f388e3cb4fb2ed5bfc5450d300f0e36587158416efe85eee0f821e37c`  
		Last Modified: Thu, 18 Dec 2025 01:17:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:0520e6974a594a2fb1e1588b0f601f3fd8725581f7a599d31531e959a926cd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba641c43086de47b82b0d468d3eea8f70c53ded975d816b0492e19161c8142c`

```dockerfile
```

-	Layers:
	-	`sha256:5a14c1d9e7590783c49c055f896446b5d9e1afb033243796dc70c38a4f3009b5`  
		Last Modified: Thu, 18 Dec 2025 04:50:09 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:fa730f571fd40e826d9540cd7d35321795971de6ba7f54f10b273fc7197a25e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43700248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20fb18326e9fac1f8cfdc3f3f6519b018b3f43bcd851818455bb2164d78e512`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:32:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:32:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:32:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:32:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:32:13 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:35:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:35:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:38:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:38:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:38:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:38:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:38:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:38:49 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 01:34:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:34:04 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:34:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:34:04 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 01:34:41 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:34:41 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:34:41 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:34:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:34:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:34:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:34:42 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:34:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:34:42 GMT
USER adminer
# Thu, 18 Dec 2025 01:34:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 01:34:42 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349359a0c202451bc8408ba1466cb8d6f1a4ebfaadab5d14186d0e0244a84b3b`  
		Last Modified: Thu, 18 Dec 2025 00:35:41 GMT  
		Size: 3.5 MB (3548054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812ad0f436973e62ab559b0e22e53a6f5aea9c9f19c0f440a1ab08bbedd17b9`  
		Last Modified: Thu, 18 Dec 2025 00:35:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e61d82a35f33cfd82c0317f7f7427938012f89967675182a15d86ce31913310`  
		Last Modified: Thu, 18 Dec 2025 00:35:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb566208c8072a475b524ee143adf5125d5bccc45a8d66753e063bbddbc56b49`  
		Last Modified: Thu, 18 Dec 2025 00:39:04 GMT  
		Size: 13.7 MB (13676370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a77043d993d7bf8c1d8c23675b0eb3930ef69f7e10c7bd1b2700fc47f0ba45f`  
		Last Modified: Thu, 18 Dec 2025 00:39:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe339f96ce12a35f49c19edb6b39be196ed6f9a4cadbe8e222a18799c52518`  
		Last Modified: Thu, 18 Dec 2025 00:39:03 GMT  
		Size: 18.2 MB (18242888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e86e5d2226816bd6939108147f4a1273a299c9b607f2a90de69f96aa15435b`  
		Last Modified: Thu, 18 Dec 2025 00:39:02 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f3e6b4aea9968d8839615740432e8b770dd86a95460aa22b0f42286c0be9d4`  
		Last Modified: Thu, 18 Dec 2025 00:39:02 GMT  
		Size: 23.3 KB (23327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e14078245b1d668c548ba193f17a844cbcf9408310a2bfb1306092a01b122`  
		Last Modified: Thu, 18 Dec 2025 00:39:02 GMT  
		Size: 23.3 KB (23343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b53e1a2651f58689abc1ca93bc425fe33b5026ab2c1528e12ab882423cf368`  
		Last Modified: Thu, 18 Dec 2025 01:34:53 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b44c2293566b5b5864b54b86ffb29b2020b98b6edc8a6f4d75246e69864352`  
		Last Modified: Thu, 18 Dec 2025 01:34:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b7af6eac4c194a6197bb205824190b520d0b7ee7cf71aebbac1189f65b3b46`  
		Last Modified: Thu, 18 Dec 2025 01:34:53 GMT  
		Size: 4.0 MB (3969320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6da847faa5c7912ee01aa20e21a808c3361ca18239eb286bca39132a3ea486`  
		Last Modified: Thu, 18 Dec 2025 01:34:53 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdebf4a5353dec38b4d91872e7d512b71aa7b4c57e958ddada33d2e67bfa7562`  
		Last Modified: Thu, 18 Dec 2025 01:34:53 GMT  
		Size: 640.9 KB (640865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb164a8d7c18916fa0b132df6fea385d9be1b1cbcc043f3680ea6837cd7f6cb8`  
		Last Modified: Thu, 18 Dec 2025 01:34:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:0212fcd597023ccb06e068ddbc4bd4163a5ac223822264fd936ef376de0c4508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d928961f305616a32104b8df03af4a700f59a9b5328b1e40730c833ab2e53f`

```dockerfile
```

-	Layers:
	-	`sha256:f3300b6555ed51d2aa3a50bf51fc688dc4159399af46e334ea73b8a9b64635a5`  
		Last Modified: Thu, 18 Dec 2025 04:50:12 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a774fbbf3aaabae7c8de2e4478736d85c5333c1cba46a6c1e1f3ed94152f145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42236405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02800cf063676e6ba058568958582c8db840ed84657bfa37614244bdd5f0dcdb`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:34:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:34:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:34:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:34:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:38:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:38:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:41:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:41:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:41:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:41:07 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 01:34:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:34:41 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:34:41 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:34:41 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 01:35:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:35:16 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:35:16 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:35:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:35:16 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:35:16 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:35:16 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:35:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:35:16 GMT
USER adminer
# Thu, 18 Dec 2025 01:35:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 01:35:16 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109c0dd3e5916dfd68c75b95b6d62136b7d9196bf2d439dafd366ade67bbf616`  
		Last Modified: Thu, 18 Dec 2025 00:37:53 GMT  
		Size: 3.3 MB (3346795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa81832028203ac2e4ade90d0b46c9d38f83c8f7eeed25028aef96873a79dac9`  
		Last Modified: Thu, 18 Dec 2025 00:37:53 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dff945df258a5cd0c98c5e16ab6a8aceb2fa7503ff4758b19f52c12fe33e8`  
		Last Modified: Thu, 18 Dec 2025 00:37:53 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0978ca3ba2f08183a40fec6ecc0077f0ea1a6e28bbff31e45683cb7bbfa7727`  
		Last Modified: Thu, 18 Dec 2025 00:41:22 GMT  
		Size: 13.7 MB (13676367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd5a05a906d7ec231e1ba83944681ab64f96a7c8a5435df9489d837df55bab`  
		Last Modified: Thu, 18 Dec 2025 00:41:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c534c2ff3bdd793ca0c24ee57b2631175c037e6242190327b05e6727d3ee1a`  
		Last Modified: Thu, 18 Dec 2025 00:41:22 GMT  
		Size: 17.2 MB (17198680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f3f11e7026c6cb27303e62b54e01dda8af571886c9bb3d1e7862c40db6984c`  
		Last Modified: Thu, 18 Dec 2025 00:41:21 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a8e25f21b9e929e72866b5a68400410ffea38d031fb265ec16b7c37953491f`  
		Last Modified: Thu, 18 Dec 2025 00:41:21 GMT  
		Size: 23.3 KB (23330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701f8ac15f204d8513695fc44a3678e41ddc126edbdc85ed4f9ed2bdcc721031`  
		Last Modified: Thu, 18 Dec 2025 00:41:21 GMT  
		Size: 23.4 KB (23350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589dea47c09076aab556edeea72d1f46b3d9141d87fe1f036ba0b61e7527bc3f`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43968b8ab09a140bdf388b9a2c0be8ecec23035c3fda5a5bf060802a3ad6984`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed855a3abf89138edd70c64c516b7981ddf9f062c0fae03c2c5a23b88f0f3ca5`  
		Last Modified: Thu, 18 Dec 2025 01:35:30 GMT  
		Size: 4.0 MB (4039977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51624f7de87d17bda3e56037ce84d996403de25aac51af6be63043de89d3ce3`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14f2233acfaef6623f62357c7b2b555228560d1a1470990d9cd99cfb1b62440`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 640.9 KB (640867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2141f123e7d053bd23aa6a39ef2feb15e0d07e7379ff5fe77d3793ac99e0a2c1`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:460d55ebdca5177a98f0da43ec9c8553e30b7ff2143fceab39135ccbafe0ad91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589552b8c00c2738e528e1a762f7a62ae400e77f3b95ff6373eed5daf43e5574`

```dockerfile
```

-	Layers:
	-	`sha256:23b78211146797a4417542dda85c7c593eb3b321ff3a32d2f7925569f2fb5a33`  
		Last Modified: Thu, 18 Dec 2025 04:50:15 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:a423b1255da4429e2e65113a3262f7eb39ad5568af009f38eb44e874aa603a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46054446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38aeb2844266244c1258c280d100167ddababaa6736f62eccb09504e1698a4b4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:27:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:27:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:27:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:27:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:27:21 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:31:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:31:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:34:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:34:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:34:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:34:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:34:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:34:45 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 01:24:02 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:24:02 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:24:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:24:02 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 01:24:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:24:35 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:24:35 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:24:35 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:24:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:24:36 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:24:36 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:24:36 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:24:36 GMT
USER adminer
# Thu, 18 Dec 2025 01:24:36 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 01:24:36 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ff19a36e03e63ff511d57643f0319c3e038d62c2ba63b5e50105b709cc6a5`  
		Last Modified: Thu, 18 Dec 2025 00:31:09 GMT  
		Size: 3.6 MB (3600940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68180acfd36c5ff4c65ba05175ec5f23189f814831917d2f950767555784f46d`  
		Last Modified: Thu, 18 Dec 2025 00:31:09 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016cf8102e0454031839ca5cf1b7a8ab4e9209ace3d2fbd66096e827fef0bc6`  
		Last Modified: Thu, 18 Dec 2025 00:31:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1032a7c6223ef32c24ae2f86cf2d01e8b4571c21633769c02d80597183cec82e`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 13.7 MB (13676352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64f9f8110d64a3379abec5e1eb4ed4d6427f14181b93e777aee2e49458a6189`  
		Last Modified: Thu, 18 Dec 2025 00:35:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b5956d972c74ca8bb907c835baa178c670bef8f3462c1139ef32c273b19efe`  
		Last Modified: Thu, 18 Dec 2025 00:35:08 GMT  
		Size: 19.5 MB (19522697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1023e712a57176b8d9f0be5b1cb9d2c4fc2e5a833a9d7c8527f2c3b20a0b89ef`  
		Last Modified: Thu, 18 Dec 2025 00:35:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e1b30e3b2e77b0794dc13a9457f19a152d2d743f91afbef12c4214e7ca9db`  
		Last Modified: Thu, 18 Dec 2025 00:35:01 GMT  
		Size: 23.3 KB (23337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05a75f6cd2a9ac46b97d52321f3da36283b3bc185ae419b5f9fd2b7ab945a43`  
		Last Modified: Thu, 18 Dec 2025 00:35:01 GMT  
		Size: 23.4 KB (23362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb9aaba5f45f9af469d0f0c27091afb25a676dbf9b184df7ec536d185fc22a5`  
		Last Modified: Thu, 18 Dec 2025 01:24:46 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2898fa29e4f54691732f292a0187987eb7c2cbc73093b1266d83c7b36b39a46e`  
		Last Modified: Thu, 18 Dec 2025 01:24:46 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d4aa7c3b5e5fefe4420ffc8fb9af57d69da57aa2297c063c78dbafe48eeaf6`  
		Last Modified: Thu, 18 Dec 2025 01:24:47 GMT  
		Size: 4.4 MB (4363497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96cf1e37184782d7e26b9512f526041d6d8ac36b3a1501d4641551fa638d23`  
		Last Modified: Thu, 18 Dec 2025 01:24:47 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc18efec351d1eb5829fc2f8c453b07cb9306d6a689ca2d956cc8ac651987db`  
		Last Modified: Thu, 18 Dec 2025 01:24:47 GMT  
		Size: 640.9 KB (640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c684912b783ff1827a6edf6cad341a0b0ae9bc8ec35fced1065300015c7af85`  
		Last Modified: Thu, 18 Dec 2025 01:24:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:d3bd59ee61c0014b6dbac14920efabdf9526ce6b88e0bcf59f3e9053afaad0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5464cd5e901bc9d78ce68f5f9a837ba2482db4a67feaedee3ae47376cb0477a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce15c85c487dfa3b18c84e266215b2316bc1dd1dad9cf9819075cae13c5b763c`  
		Last Modified: Thu, 18 Dec 2025 04:50:18 GMT  
		Size: 36.0 KB (36007 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:8db411b2fd6a503b8fd8e9449f1489e695a7ced0d3cebbb64182c89b86d9af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46444529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947b1103064216ac1cea80818a178df25a8a5cc454f821fdb92d135d09bb76c4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:32:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:32:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:32:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:32:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:32:51 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:32:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:32:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:36:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:36:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:36:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:36:24 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 01:14:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:14:27 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:14:27 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:14:27 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 01:14:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:14:53 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:14:53 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:14:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:14:53 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:14:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:14:54 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:14:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:14:54 GMT
USER adminer
# Thu, 18 Dec 2025 01:14:54 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 01:14:54 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e33f3aedc53a4c8d7312c426436297a40c1590fd1e0edcf25666027bfbf3657`  
		Last Modified: Thu, 18 Dec 2025 00:36:42 GMT  
		Size: 3.6 MB (3628729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344e7ffbfe33ae65d30595d71eb6af40385ef73029b413b0dd8940aacf572ebc`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbebd651e3cb014e9b1c9d79927df72ac5bcfd669c0839dfcbae280789937cc`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da6d96c639097567a01ff9001b02004aee8dd86717167655dcde47f5745d923`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 13.7 MB (13676346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2565f93ece9085c5e343a67b99695336b1ad300f9f4e14090a5619661a206212`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99fd20b23546601933f4f780d752466854d2da7ec2d933ce607c5d386a172d7`  
		Last Modified: Thu, 18 Dec 2025 00:36:45 GMT  
		Size: 20.6 MB (20558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046aa4dea32e343cedc07c903b1127e21790c2768b10259b8782e094155da8ec`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe0b764ea1436869fde8824af4c1bdc198b3fa6f5d532479f464b2f31d4b9e`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 23.5 KB (23511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6a8cada627bc395559bd656b46b971268bd617c48819665398d5110e05add`  
		Last Modified: Thu, 18 Dec 2025 00:36:40 GMT  
		Size: 23.5 KB (23516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5283a96e07e06d2b67cb4961c8ec4f131f9fd30542cca3a181efb9e30c7a143`  
		Last Modified: Thu, 18 Dec 2025 01:15:07 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225cedcb57f57a2c9d9f2ac234993554cbc70a4e8a6435181e8c791b08cf7446`  
		Last Modified: Thu, 18 Dec 2025 01:15:07 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f0494a24718499453148684b5a79c990e09b66b17cdc952da3e32e0fbeafe9`  
		Last Modified: Thu, 18 Dec 2025 01:15:08 GMT  
		Size: 4.2 MB (4199768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e9940783f6e74cefcc3f60b4af1c2829a40358136b41481dcc79ae4226db24`  
		Last Modified: Thu, 18 Dec 2025 01:15:08 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693387ee978aae05ce095ebb33fc9b8aa7267748a733a94152bcc89e005ffedb`  
		Last Modified: Thu, 18 Dec 2025 01:15:07 GMT  
		Size: 640.9 KB (640870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ad2e825c55e3b0a7e179f73eb06fe2655b8b1331f0298209db0c0f65b08498`  
		Last Modified: Thu, 18 Dec 2025 01:15:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:53d9f88132dc8e63c6fe528198113c39245a77749c4a8b05a52554c29b044779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e6f79d9f6024901f3b311b291ed7b676e1a5fdde50e3ab6b8c6c5cb3c529a`

```dockerfile
```

-	Layers:
	-	`sha256:42fdea01033371573ef291a4eae947672afec52a329143c5115e187f4f82525f`  
		Last Modified: Thu, 18 Dec 2025 04:50:23 GMT  
		Size: 35.8 KB (35786 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:e4421ebe0ec8edeef24bbe81d14f547f14ac330124d8ae01e5e86e824b5922d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47395167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69d341f3fa5446cdc4ceae9cae36bbe62b59476d35775643cd7499abef5b415`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:36:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:36:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:36:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:36:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:36:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:36:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:36:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:36:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:36:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:36:25 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:36:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:36:25 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:57:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:57:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:01:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 01:01:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:01:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 01:01:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 01:01:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:01:12 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 02:38:02 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 02:38:03 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 02:38:03 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 02:38:03 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 02:38:52 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 02:38:53 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 02:38:53 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 02:38:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 02:38:53 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 02:38:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 02:38:54 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 02:38:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 02:38:54 GMT
USER adminer
# Thu, 18 Dec 2025 02:38:54 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 02:38:54 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520fe501f40cb3dc7ae4e6c3e7c2c443dfa657885af4903b375c4c3bc3ecbe57`  
		Last Modified: Thu, 18 Dec 2025 00:41:24 GMT  
		Size: 3.8 MB (3768861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e468808c5f31df4c4d0864313e369cc90905861047a4daf096a72a85f71211`  
		Last Modified: Thu, 18 Dec 2025 00:41:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f11e31e2b9194dc727d1aa5b066819eaf54cf27435b5ff575aae91d18cbe67`  
		Last Modified: Thu, 18 Dec 2025 00:41:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f273e70d17af64cd95d7d1d4a0223e4c9b1c40f10dbba4c757d29a55d2cd3ef`  
		Last Modified: Thu, 18 Dec 2025 01:01:37 GMT  
		Size: 13.7 MB (13676377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7935ea86ee281335cf6e6ef80174545b723a73f1e94e70e8beab3a52535da4f6`  
		Last Modified: Thu, 18 Dec 2025 01:01:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca6b8aa0f0ccfb35e9de9e0797df2749c6ddca9461ba112e6751c0e7e4b2c84`  
		Last Modified: Thu, 18 Dec 2025 01:01:38 GMT  
		Size: 21.2 MB (21150560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657d8e17d9d337dc684421c3a10ed17c5bd9268330f6e7caac2bc3f2d29edc83`  
		Last Modified: Thu, 18 Dec 2025 01:01:36 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b7c42074de4565675d594992a1c408140fb21875fc107b39c6cbfd91d4d0c`  
		Last Modified: Thu, 18 Dec 2025 01:01:36 GMT  
		Size: 23.3 KB (23348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef3be1d4dd483062036e95ba6ae40d7c47ade61d820a78534644171ca1b1d26`  
		Last Modified: Thu, 18 Dec 2025 01:01:36 GMT  
		Size: 23.4 KB (23367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22251e15f6c6829fcf6617f1dbc6234708f37b3b37685c6e2364a1278e8b0b6`  
		Last Modified: Thu, 18 Dec 2025 02:39:17 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9657b4934466f175a5d9afd9af9c235beb0cb3f78dd84ff83f78e8611aaaa7a`  
		Last Modified: Thu, 18 Dec 2025 02:39:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe0f1a72d109d0e1514ced3f7ab40bba4c6a6e30121de1a6956c92ed38df1e5`  
		Last Modified: Thu, 18 Dec 2025 02:39:17 GMT  
		Size: 4.3 MB (4276370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd0acf7e9b76d98476d16abe2c9e755638a734943c28dc259e6af800912fe7`  
		Last Modified: Thu, 18 Dec 2025 02:39:17 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55995684afa40f4e66397330250fff5744b9b86f6f119dd1b07ca4b7655bb299`  
		Last Modified: Thu, 18 Dec 2025 02:39:17 GMT  
		Size: 640.9 KB (640872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe188afec21f5a22719521624583440002172b6cbe2e2bd56cf3c1c4f3001ea6`  
		Last Modified: Thu, 18 Dec 2025 02:39:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:2809b9f28535cf082f7fc600f7a9246257ba87caba9f3830fd0978ea6f3f9b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29003732b3cc4b92098b5384d148918e1d00c76641478b10db96c100f14d47a9`

```dockerfile
```

-	Layers:
	-	`sha256:d226db9d1bf75bb3cd547e0d8fb1f1d9d87257b34490c50af56209bd3fb1a4dd`  
		Last Modified: Thu, 18 Dec 2025 04:50:30 GMT  
		Size: 35.9 KB (35895 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; riscv64

```console
$ docker pull adminer@sha256:55a1bd31a835f5c1c4d89c93a0b5fe2992e771298e72455f5e74f4b29945c655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45022684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbea8204b8d857776862df85fb1ee1c3956a7c406f54de8fe513abfdbe3cd11`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 04:20:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 04:20:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 04:20:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 04:20:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 04:20:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 04:20:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 07:28:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 07:28:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 08:25:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 08:25:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 08:25:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 08:26:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 08:26:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 08:26:02 GMT
CMD ["php" "-a"]
# Thu, 04 Dec 2025 17:53:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 04 Dec 2025 17:53:27 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 17:53:27 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 04 Dec 2025 17:53:28 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 17:59:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 04 Dec 2025 17:59:02 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 04 Dec 2025 17:59:02 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 04 Dec 2025 17:59:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 04 Dec 2025 17:59:02 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 04 Dec 2025 17:59:04 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 04 Dec 2025 17:59:05 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 17:59:05 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 04 Dec 2025 17:59:05 GMT
USER adminer
# Thu, 04 Dec 2025 17:59:05 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 04 Dec 2025 17:59:05 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2559d37315299ac2974df718491e68e75407bd4024398180bf2e31452dba7291`  
		Last Modified: Thu, 04 Dec 2025 05:22:56 GMT  
		Size: 3.7 MB (3739982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3bd8574cb0921dcd93805f3fca6feedf60a33fb9c08e52f2eb9827989b0a`  
		Last Modified: Thu, 04 Dec 2025 05:22:55 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8090aa9a6be2d187aa1322d22eee1829c9afdeb8a4c68df173418fa6face7`  
		Last Modified: Thu, 04 Dec 2025 05:22:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b6f1d80a56f12660d5596d9ccb80af5ab2555709531ec9536283065ba2b7c`  
		Last Modified: Thu, 04 Dec 2025 08:27:14 GMT  
		Size: 13.7 MB (13676356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4cd5b409854fe4a455aee413aea8743702d3c39940d594e8a1d5df3b733c7`  
		Last Modified: Thu, 04 Dec 2025 08:27:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65325f08d0fe2fd4c2d1ea1265d99c9503f58f1f69a1cf3c8908fc117cd9f49`  
		Last Modified: Thu, 04 Dec 2025 08:27:14 GMT  
		Size: 19.4 MB (19388532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c876c7ba4980223e9461585efedeba7648d89a58ab94e82dd4dbe39a5f5016`  
		Last Modified: Thu, 04 Dec 2025 08:27:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f3ff69b3743d5055de4da79f815375d2579b5d61e85fc551e97808d8d3227`  
		Last Modified: Thu, 04 Dec 2025 08:27:12 GMT  
		Size: 23.3 KB (23296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d498a59440f11542370bf96000fe07e992fe812caeb07e47175b0c9f6fc7a07`  
		Last Modified: Thu, 04 Dec 2025 08:27:12 GMT  
		Size: 23.3 KB (23322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9defd5649cfbb1486487717319cca66b9c248e5539b2e6195a60717acb43012`  
		Last Modified: Thu, 04 Dec 2025 17:59:31 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d229e97c267126af3686e99c48fa9ea02ab920be39eb8716ce5aeaafb057d9`  
		Last Modified: Thu, 04 Dec 2025 17:59:31 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a441e6dbb66f1731b5bb1e4e763f222bd7419110a1a2590bfe36d2ead98221ca`  
		Last Modified: Thu, 04 Dec 2025 17:59:31 GMT  
		Size: 3.9 MB (3939129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495a2a9cd7f157df0c62bb4e6c55910545d50fad030a50f44e61244259a46fb`  
		Last Modified: Thu, 04 Dec 2025 17:59:31 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8aa34c8d11947054928d03f375e80c9392447146821eb4f11a4136cee3afbc`  
		Last Modified: Thu, 04 Dec 2025 17:59:31 GMT  
		Size: 640.9 KB (640872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8408e0308246ba2c3a6a27e6d61a2e3872111cdeecfcef1bf4d9702cc3d24a4`  
		Last Modified: Thu, 04 Dec 2025 17:59:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:5f179fc99e85143e18a9eebf3823eaa713bc2f7facbe7346bd589b352619fbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8275704b865e38e6bc7cf4dbc4724c00833d3ae440b6c6048382c7d053c3f7f`

```dockerfile
```

-	Layers:
	-	`sha256:359e1f1c060156914352d1889d8fc91e86bf8a33ab62a64a777d37bc4a4a03ab`  
		Last Modified: Thu, 04 Dec 2025 19:49:28 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:4a49316d8f0ba80c65b168281b736d7d0f7fa81b2f301bad950f0520f35cda71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46041497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aad2511a70ec8c1a86473475ac878ca5cbaca71f4fbda0504e6bc954e66e2ad`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:31:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:31:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:31:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:47:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:47:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:54:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:54:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:54:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:54:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:54:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:54:54 GMT
CMD ["php" "-a"]
# Thu, 18 Dec 2025 03:47:09 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 03:47:09 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 03:47:09 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 03:47:09 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 03:47:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 03:47:44 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 03:47:44 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 03:47:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 03:47:44 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 03:47:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 03:47:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:47:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 03:47:45 GMT
USER adminer
# Thu, 18 Dec 2025 03:47:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 18 Dec 2025 03:47:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344fa339e55ae2ef62eaee8d37110609d0d656213b8274a8e7a7ab18327247ac`  
		Last Modified: Thu, 18 Dec 2025 00:38:18 GMT  
		Size: 3.8 MB (3794501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327290246b6eefafee2ed67e84a73a399acad16f47f0ad2d3f400fcf15ef1b3f`  
		Last Modified: Thu, 18 Dec 2025 00:38:18 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083737e4ce9faf5aa6c038cf664c25a769c6a5aac182a45e34a89d948c87732`  
		Last Modified: Thu, 18 Dec 2025 00:38:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b269232a830f61596f35ac9a5f8d61f8640f26ffa35a7abbb8473c6f03c64b8`  
		Last Modified: Thu, 18 Dec 2025 00:55:29 GMT  
		Size: 13.7 MB (13676355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9d30d34f87a72689f37ebef40348abbd2bf2e42f30861d92b8b31c658860`  
		Last Modified: Thu, 18 Dec 2025 00:55:28 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85a0f50601903bac2821b5302caadd7a8858fec7a81f26dcb8c8c091726c31e`  
		Last Modified: Thu, 18 Dec 2025 00:55:30 GMT  
		Size: 20.0 MB (19999359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fe46f93d6c555e9e1fec7d3daf14555d38a616428ec45ab134ea7e5e367a68`  
		Last Modified: Thu, 18 Dec 2025 00:55:28 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9e28638819cc8cc9c87c32bb0c92d8ed73e5aecf90f1a20a61072b2fa558a7`  
		Last Modified: Thu, 18 Dec 2025 00:55:28 GMT  
		Size: 23.3 KB (23334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f39c9af70317dde70aded625673c059170e70c8e703881ea4c60b644e513b94`  
		Last Modified: Thu, 18 Dec 2025 00:55:28 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d30e94f3ece1047df3c705f19a9ecde44c163f08a88d37af54ffe88ab2cc9`  
		Last Modified: Thu, 18 Dec 2025 03:47:58 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7efac43209e91afd02c53b18be2ce47f19220b5eda7a95e21e78ec2c73f985`  
		Last Modified: Thu, 18 Dec 2025 03:47:58 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18e840bf587c3d37ce96398dd0ee861f24bb028f58325215c912ff82e70b68`  
		Last Modified: Thu, 18 Dec 2025 03:47:58 GMT  
		Size: 4.2 MB (4151749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9271dac0e2b137f5c33759a8358b08da274df03cfd094c34fa17810a0cc1d13`  
		Last Modified: Thu, 18 Dec 2025 03:47:58 GMT  
		Size: 1.7 KB (1699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6cefb5a97a7a5505ee28468ef92843eddb3463a0699337120bc2f69418a46b`  
		Last Modified: Thu, 18 Dec 2025 03:48:04 GMT  
		Size: 640.9 KB (640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848802b33ceb6a5bb3f9c853aada59b90aae9a837060be19c8d2fb833e497929`  
		Last Modified: Thu, 18 Dec 2025 03:47:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:11c64958d24eb643697fad5db78d63a225c7d4bdf097222690b4260d2037bf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0c2b9297495bf4f23c6fb2a73e1d2c6201db7d53ce5c8583e40dff66bcb92`

```dockerfile
```

-	Layers:
	-	`sha256:ae479624bf416bdfefc2a3b09c0fc85d8ae8acc5cc2397ab52d7784692acc0b1`  
		Last Modified: Thu, 18 Dec 2025 04:50:35 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json
