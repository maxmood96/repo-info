## `postfixadmin:4-fpm-alpine`

```console
$ docker pull postfixadmin@sha256:c037ca3c74cc315aa38b7d0b2119f67c18764aa9034d19420b47da02693d092e
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

### `postfixadmin:4-fpm-alpine` - linux; amd64

```console
$ docker pull postfixadmin@sha256:6770ef115f88401b437cc7fc159fe15fa317e21e8e9e84a0cdb56e727ee2cf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60982778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7535a11bdbacf2a7178025066841b1a6904185682119f8d40353895e8d3485`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:57:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:57:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:57:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:57:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:57:46 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:57:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 22:57:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:01:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:01:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:01:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:01:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:01:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:01:13 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:01:13 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:01:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:01:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:01:13 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 00:27:03 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 00:27:03 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 00:27:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 00:27:21 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 00:27:21 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 00:27:21 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 00:27:21 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 00:27:22 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 00:27:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 00:27:27 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 00:27:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 00:27:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaecf1e5498bb01dd1ae2b44061041bed40b2d9d7da210595201f49aa323681`  
		Last Modified: Fri, 09 Jan 2026 23:01:31 GMT  
		Size: 3.6 MB (3591454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e21eeaedb28aff9479673d129859cc9e8c6cb1348ee466631aed801f52c5cb`  
		Last Modified: Fri, 09 Jan 2026 23:01:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c3856a471a1b6385943c82cdecba63db32020cefc5ef3ad7b15de38167343`  
		Last Modified: Fri, 09 Jan 2026 23:01:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b1827620c48f0857d496655bb9cb5dc074c8ce30cb38bc78b45b5397c2c530`  
		Last Modified: Fri, 09 Jan 2026 23:01:31 GMT  
		Size: 12.6 MB (12625785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45bdb4339e06b9d7e63c03e53845b97259ff185bb1ca3613d1ef7641174b6d8`  
		Last Modified: Fri, 09 Jan 2026 23:01:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed476e94fc01c97908c7732728a130c55ade8f5a416dc8add47634bd7f4ca078`  
		Last Modified: Fri, 09 Jan 2026 23:01:32 GMT  
		Size: 13.4 MB (13370826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3781b849d7a291084969754f4225c84073e273f5febafc6f9070fce1d77447`  
		Last Modified: Fri, 09 Jan 2026 23:01:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dde4db1941f91ef2c02ebf8149cb98f05a55811775071663d2a74c266bcc5`  
		Last Modified: Fri, 09 Jan 2026 23:01:31 GMT  
		Size: 23.5 KB (23500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606645425d56e7a70529982285edc399f769cb19b8f11138fbc72d2543b827a2`  
		Last Modified: Fri, 09 Jan 2026 23:01:31 GMT  
		Size: 23.5 KB (23519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63ab254ffc67a8ddc8b4e107c1e4b68f38a824dd18aa0a63fa121ae854d8115`  
		Last Modified: Fri, 09 Jan 2026 23:01:31 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f97ef2e730824ce5bc7e38452d7f165872f818f1a5092ddfbff62218a9930e`  
		Last Modified: Sat, 10 Jan 2026 00:27:40 GMT  
		Size: 523.1 KB (523074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b5f465e8b214d34ea631d1a493005e39c088ce6c204c97f60f0a410d71c6f`  
		Last Modified: Sat, 10 Jan 2026 00:27:41 GMT  
		Size: 298.7 KB (298654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4977066c14da2680b94b0d4b80bbed7dbab1edb0beb2850d63d438592f6de6ec`  
		Last Modified: Sat, 10 Jan 2026 00:27:41 GMT  
		Size: 2.6 MB (2602216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e03fcbc9631b95f5f7e53759248c9983b61d4d02f57ec6a9b44060bde6874e`  
		Last Modified: Sat, 10 Jan 2026 00:27:45 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f4311c779471db3adee1629b53f502ce3620e4493931f870a248601252fc02`  
		Last Modified: Sat, 10 Jan 2026 00:27:41 GMT  
		Size: 776.4 KB (776355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1baac87093cfa9720f10b82bf06cfeba6e390e7bb261b76127295036b38fd`  
		Last Modified: Sat, 10 Jan 2026 00:27:42 GMT  
		Size: 23.3 MB (23272349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a7fcba69424290ce5a869b4fec1d31552d2495756c94bbbf48ff6c5125bd45ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8409483b0ad5d65aa7c958af32154d9aa6cedb28115a357b0323611d22a5c80`

```dockerfile
```

-	Layers:
	-	`sha256:eafe377783270ab31996611d472792ae8d5981bef73981659bdbfaaf23cb1eea`  
		Last Modified: Sat, 10 Jan 2026 03:11:49 GMT  
		Size: 37.2 KB (37180 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull postfixadmin@sha256:385f54f3e68c66b1acb5a54c68fc9424ce1315748ced6db4e68f61e55fa23ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59351261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad75cc616b1a8890f69a96ce9310eb2b5b97b9b7b64f1330c6ac8f5babfe4650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 10 Jan 2026 01:04:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 10 Jan 2026 01:04:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 10 Jan 2026 01:04:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 10 Jan 2026 01:04:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_VERSION=8.3.29
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Sat, 10 Jan 2026 01:04:00 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Sat, 10 Jan 2026 01:15:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 10 Jan 2026 01:15:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:18:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 01:18:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:18:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 01:18:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 01:18:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 01:18:08 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:18:08 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 01:18:08 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 01:18:08 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 01:18:08 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 07:07:47 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 07:07:47 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 07:08:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 07:08:12 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 07:08:12 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 07:08:12 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 07:08:12 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 07:08:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 07:08:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 07:08:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 07:08:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 07:08:23 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 07:08:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 07:08:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d0b03342694844c9ed5491960c2d28898bc29caeabf01215152eae37d65afb`  
		Last Modified: Sat, 10 Jan 2026 01:07:28 GMT  
		Size: 3.5 MB (3548037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad7c356cc3524e2dc45cae918c8af6e1700dae06f31e4fcccddc9eca26ca64`  
		Last Modified: Sat, 10 Jan 2026 01:07:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea716186ae644654c5c435b97433e71721c10ea1d9d7b60fa3ef0e45584f407`  
		Last Modified: Sat, 10 Jan 2026 01:07:28 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bfd903ebd3ffe76d5e07eeeb27fe588548526cf9baeacf4c3cd1762a430e66`  
		Last Modified: Sat, 10 Jan 2026 01:18:21 GMT  
		Size: 12.6 MB (12625803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90574c0b9f2b56e1e3e5bdae79d1c6d751c1fbd85e14f7664c78cc525c471bc2`  
		Last Modified: Sat, 10 Jan 2026 01:18:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3ddec36a4982faf122bc879e520afbb2c25256329c1a790b2501e3fef4adfc`  
		Last Modified: Sat, 10 Jan 2026 01:18:23 GMT  
		Size: 12.1 MB (12098723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a6503f072492590cd18563a43413968c3298c7acd93329ae467e9c1bae9cd7`  
		Last Modified: Sat, 10 Jan 2026 01:18:21 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd0f40735d34a88b8d02082659fa246b63fb65c591ed3d2ddc488d94d7ef02`  
		Last Modified: Sat, 10 Jan 2026 01:18:21 GMT  
		Size: 23.3 KB (23331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37136601c684f4853ada0bb7c927ebbc587955d3c122b5565056ee773702048`  
		Last Modified: Sat, 10 Jan 2026 01:18:20 GMT  
		Size: 23.4 KB (23350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c395e7ee37f8edff7236e2914920030d70d2ef6f1678a2b5a1fe8175de838d7`  
		Last Modified: Sat, 10 Jan 2026 01:18:20 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66248b231e2a7bb0bb82f5db717e5c76279e2c8ade0725524b627d19d449b7d3`  
		Last Modified: Sat, 10 Jan 2026 07:08:36 GMT  
		Size: 525.2 KB (525160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e07beee6f9204b3ae2671f2dd576d687cd91fb3ad74ba107236f9eed0f0b8d`  
		Last Modified: Sat, 10 Jan 2026 07:08:36 GMT  
		Size: 272.6 KB (272648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1545d3242a98ed84a740f6fdb175f2551a8443cfe4b7557c77eb2c8df6496370`  
		Last Modified: Sat, 10 Jan 2026 07:08:36 GMT  
		Size: 2.6 MB (2602224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8a66762ca311e07aa84fd13558314d0ca10fcb45749e7b164fd46d0a338baa`  
		Last Modified: Sat, 10 Jan 2026 07:08:39 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2d4789b717d8049a7a21750f0ab9eb468759b4416563c896ec61d909446169`  
		Last Modified: Sat, 10 Jan 2026 07:08:36 GMT  
		Size: 776.4 KB (776356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3862a528931845d5df471b78b63d03ec99e3c6cfd82da525d836522cbd8b6530`  
		Last Modified: Sat, 10 Jan 2026 07:08:39 GMT  
		Size: 23.3 MB (23272257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a329459f3c54bcea498aa96d30252eb5b086cf73c55d383753c9ab21df81b822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2fd6fe5ec4fd0feba2fc2558087342826608e8694765489b8a5ce5dc6859d`

```dockerfile
```

-	Layers:
	-	`sha256:36131328890ac547e10817f9ba8955fd6f6aea2eb01c7e85c80fff2c550f3b5d`  
		Last Modified: Sat, 10 Jan 2026 09:10:43 GMT  
		Size: 37.3 KB (37322 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:c5a6a94b5443ad026837792a7b07a898df78fe300ea4a66650d8c5cef69101a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58099297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ad97b1effdb0180fbb982f7268866a6ed648f5fc67daac1c633b9658a6c8d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:35:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:35:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:35:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:35:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:35:06 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 23:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:35:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:38:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:38:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:38:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:38:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:38:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:38:48 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:38:48 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:38:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:38:48 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:38:48 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 01:01:53 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 01:01:53 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 01:02:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 01:02:15 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 01:02:15 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 01:02:15 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 01:02:15 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 01:02:16 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 01:02:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:02:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:02:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 01:02:20 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 01:02:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 01:02:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97037d584d37b8ab9ffaa0391958a7eacb54059e3449ebd4d8596a61beae6055`  
		Last Modified: Fri, 09 Jan 2026 22:38:45 GMT  
		Size: 3.3 MB (3346832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc8f71f3253a2a179eec1d65eb6b3d3345be6e7aa62ff268de699521f57d2b8`  
		Last Modified: Fri, 09 Jan 2026 22:38:44 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876777cc989301c3bffa365aa7388dd6e59fc1610b136e2029160f66704ed3a7`  
		Last Modified: Fri, 09 Jan 2026 22:38:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8f4fff38eb4f3436a5465a1b95577450f09914018a3d0451b89069f9826be0`  
		Last Modified: Fri, 09 Jan 2026 23:39:03 GMT  
		Size: 12.6 MB (12625805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728a1e415ea08895620fe82098a333ae3f2a413726ea6fcf70c40e4bb6416330`  
		Last Modified: Fri, 09 Jan 2026 23:39:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cee46bf98eaf6c365920640a1cf38ac2f09bb6ef8a676451ec3f8bd6c9bbe1`  
		Last Modified: Fri, 09 Jan 2026 23:39:03 GMT  
		Size: 11.4 MB (11397673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c134fd607d6913a843f89ba154bd4858a94ad10a5a2e4a52add877ae72f8ed`  
		Last Modified: Fri, 09 Jan 2026 23:39:04 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26417e65419cc16551df753d06907ff4be0085e5f798b5c75c4cfa7c5747fee`  
		Last Modified: Fri, 09 Jan 2026 23:39:02 GMT  
		Size: 23.3 KB (23340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8d621ee6fb90c189bcadeb465b4a16d92e877cba967447abdf580ddfcc8440`  
		Last Modified: Fri, 09 Jan 2026 23:39:02 GMT  
		Size: 23.4 KB (23358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5554e55ab7501b40307d848e910aab1536de66b1160092698b31bd4a3f77b779`  
		Last Modified: Fri, 09 Jan 2026 23:39:04 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16d33f7607e9ce5972dc7e403522dc0b0c521e854846f1d27cc60ec7a8ed95`  
		Last Modified: Sat, 10 Jan 2026 01:02:32 GMT  
		Size: 482.5 KB (482503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b461d0c7433b7f8bdfa25e84b696c634f08c0f1a2cb53b9675ec08051dbda`  
		Last Modified: Sat, 10 Jan 2026 01:02:32 GMT  
		Size: 254.6 KB (254641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c65c20bb906ff07afd84141f864908b2255f38b93dc2b5fb22a69ef210ad8`  
		Last Modified: Sat, 10 Jan 2026 01:02:33 GMT  
		Size: 2.6 MB (2602215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd0570c07d65c2f9f44e0f3fedd60c73c080482b34b94ec430308bd95e9d16c`  
		Last Modified: Sat, 10 Jan 2026 01:02:32 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde617365823fa0b38f4eae9cb2f318bb405b27044fa8334a285ad6f920488de`  
		Last Modified: Sat, 10 Jan 2026 01:02:33 GMT  
		Size: 776.4 KB (776356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af834aea565a077dcc853ed80cb794780478b0b6b66c9e7f12386ada861e0444`  
		Last Modified: Sat, 10 Jan 2026 01:02:51 GMT  
		Size: 23.3 MB (23272237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:1f16800c83921bebce628e3eb61229eae6dfbced8791bf878a8f5e2a03533506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b8e298b0b90155934a8bb7cd2c6cf8eaf829e791bc7bb1548a3fcf45aa48b9`

```dockerfile
```

-	Layers:
	-	`sha256:9b0f9464fc0fd78ef5b68e27d4c525391bd305aaf4898713f8d30a11a21d37ab`  
		Last Modified: Sat, 10 Jan 2026 03:11:54 GMT  
		Size: 37.3 KB (37321 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:9332e9439e79fc73993a89d26409ff106755537fa639fa9ff4820cc315e1e09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61272737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ca3124448b3355bcace092ff6aabf09032295357a89e2a59cc0c9dcc3ef298`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:47:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:47:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:47:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:47:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:47:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 23:01:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:01:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:06:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:06:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:06:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:06:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:06:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:06:20 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:06:21 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:06:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:06:21 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:06:21 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 00:29:48 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 00:29:48 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 00:30:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 00:30:09 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 00:30:09 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 00:30:09 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 00:30:09 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 00:30:10 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:30:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:30:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 00:30:14 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 00:30:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 00:30:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081121271225baa92f1d3bee236b13f2fa023fb6a911fd7165e9e9d966d92442`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 3.6 MB (3600957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9623b68389765eee841dc588c562b05e8b8da3660eb6fb0af89ffeba4e0e8eef`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e21a42b344c900deae9f11fefc7142435bf3add3e0cc2af1225971a99f7097`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a434b4866b6c870f87b35dbba5027d3f6e4ed9e4c4c01dd514ff20da4905088d`  
		Last Modified: Fri, 09 Jan 2026 23:06:36 GMT  
		Size: 12.6 MB (12625789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ff92864e3d0ea7f8844600e040b0dabfb2a7b66372007c4aee285212cd6ac`  
		Last Modified: Fri, 09 Jan 2026 23:06:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dce8f0395bfadc179b52d9305fc19ee1d77168cc5c5588a7a73947f8bd6e238`  
		Last Modified: Fri, 09 Jan 2026 23:06:35 GMT  
		Size: 13.3 MB (13261370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a575708b3729c5507524facceecb3df01e1688c7447bf18eb3756f69913d5d1`  
		Last Modified: Fri, 09 Jan 2026 23:06:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aadcbb1629f0e263796f672ca2e0bdd1ec0f00a01c8cd0f08f514c2923067b`  
		Last Modified: Fri, 09 Jan 2026 23:06:34 GMT  
		Size: 23.4 KB (23352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de3973fd06755c804818ea4b952c9ea2a38e63b3c3015692ca2dd7172bdbd24`  
		Last Modified: Fri, 09 Jan 2026 23:06:34 GMT  
		Size: 23.4 KB (23360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1521c7d798b7d29050e4a82b51b25b532511f9524bfb0785270cd2307750a612`  
		Last Modified: Fri, 09 Jan 2026 23:06:34 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7888792884ecea8e443fd20704a4f6f2239d5a3ee2b66386bf90b88653f8c062`  
		Last Modified: Sat, 10 Jan 2026 00:30:29 GMT  
		Size: 585.9 KB (585879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9849c5615fe5eaad7778c35a63566cea93502e90fdc8be24e0206feadf43cf29`  
		Last Modified: Sat, 10 Jan 2026 00:30:29 GMT  
		Size: 290.5 KB (290531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6028e76c637024c7da1449d452294f5ad5e57cccd9e9dd6bd1491a08975dc2`  
		Last Modified: Sat, 10 Jan 2026 00:30:29 GMT  
		Size: 2.6 MB (2602218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246473cf32ec3a04f8895f9892d789802e868cdafd6bebc7af6b7a5ae9a389c3`  
		Last Modified: Sat, 10 Jan 2026 00:30:29 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc051a874a49dc0dcfd1fc2820222a56920d8298cfbf8eada484f43ee7996f8b`  
		Last Modified: Sat, 10 Jan 2026 00:30:29 GMT  
		Size: 776.4 KB (776356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6023495e2832331a6968314ad1d760e141de6613073bddff3b503e19a962c0`  
		Last Modified: Sat, 10 Jan 2026 00:30:31 GMT  
		Size: 23.3 MB (23272235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:8ec65a0ceb1f47776d3b0286d2e94979d656c9f06cebac7ac5ef20d8d11e42ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d5119efc89b1df10d7fccc749fd92be106c08515b8dc8abb5fda90ebb34b1a`

```dockerfile
```

-	Layers:
	-	`sha256:bd3c20a8b9eec4c2a5e5011fe817c87bf9efefb3b2d311d93ec9f900890b9127`  
		Last Modified: Sat, 10 Jan 2026 03:11:57 GMT  
		Size: 37.4 KB (37356 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; 386

```console
$ docker pull postfixadmin@sha256:c1e791e3ddfdc948e61179f7c52dd8289e53803cf1a9f31c9aa24c0eac653ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61132739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634d6cdc65eb2301317383fa92d8821608c058656ce8e96c48d18ff079bc492a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:25:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:25:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:25:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:57:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 22:57:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:01:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:01:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:01:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:01:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:01:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:01:55 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:01:55 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:01:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:01:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:01:55 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 00:36:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 00:36:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 00:36:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 00:36:45 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 00:36:45 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 00:36:45 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 00:36:45 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 00:36:46 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 00:36:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:36:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:36:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 00:36:49 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 00:36:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 00:36:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcad021abd1c6e059190f900185611cc66171ff3ddf8cd4af5ae2e92ac2d250f`  
		Last Modified: Fri, 09 Jan 2026 22:29:44 GMT  
		Size: 3.6 MB (3628731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8320b1354e2c2492cba92bdbf83d66fd9875ff7653fbf38338cd4a387da70b`  
		Last Modified: Fri, 09 Jan 2026 22:29:44 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be9a13a571954942ecf29b0ff6f45db49b69d7d6341f9cec0530b2afc31a24`  
		Last Modified: Fri, 09 Jan 2026 22:29:44 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c075655a9dbe7531e72801361162921b17b3d6fe0def4abb22a7335298d0795`  
		Last Modified: Fri, 09 Jan 2026 23:02:10 GMT  
		Size: 12.6 MB (12625783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbb5db20a53be7ee1f69d632f08f9b75164b926fea9302e11aa628a92f68be6`  
		Last Modified: Fri, 09 Jan 2026 23:02:09 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0b6bde17dfe127f9ccb9cd1f12f4a386d12ff8cdd5e384e79bf28049e7117b`  
		Last Modified: Fri, 09 Jan 2026 23:02:10 GMT  
		Size: 13.6 MB (13625238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2a8ea38968c8087bb299e52edb8e12d94f3f513165be7502804da996c7961d`  
		Last Modified: Fri, 09 Jan 2026 23:02:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd17213303b3ef4abdbf367fa594574392a3ffb709b36993035dd6d653b44a4`  
		Last Modified: Fri, 09 Jan 2026 23:02:09 GMT  
		Size: 23.5 KB (23520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d583b6371f4e1b7b4d265b1af36e96bbcc9a5a84ea249d72b0b02469f549973a`  
		Last Modified: Fri, 09 Jan 2026 23:02:09 GMT  
		Size: 23.5 KB (23545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fafa78e28398fd12e8b9ecdd8714137475ae5b08f972b0a5b317f6eed5b280e`  
		Last Modified: Fri, 09 Jan 2026 23:02:09 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6c02626bf37af2a47361eebc2f1e06a8a0f456e2c47941e18586ae591e7bbd`  
		Last Modified: Sat, 10 Jan 2026 00:37:02 GMT  
		Size: 533.1 KB (533082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816d0c1449532db3b6468e2eddf99ecd9e3715a0613ac59118f6c4cfd1ba3af7`  
		Last Modified: Sat, 10 Jan 2026 00:37:02 GMT  
		Size: 321.1 KB (321110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726ab27544b2b371306ba67c3e1e1f65031a109ba3f08633ade0d77c76d2d98c`  
		Last Modified: Sat, 10 Jan 2026 00:37:02 GMT  
		Size: 2.6 MB (2602217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aced24080f4ce6ac0d74ba9ce4d0eb862cb67cf51f8ad2c1ae0fe68513029c`  
		Last Modified: Sat, 10 Jan 2026 00:37:02 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e65a54b95ec1c4398121e9b62714911fd969274bba9a91e189825ef4d5bcbd`  
		Last Modified: Sat, 10 Jan 2026 00:37:02 GMT  
		Size: 776.4 KB (776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a94b4c3c87f4aae3b0e09a0c714d48c197669719be6b42e3c58e3bba13ec00`  
		Last Modified: Sat, 10 Jan 2026 00:37:04 GMT  
		Size: 23.3 MB (23272106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:867f3e857f052453b5cd71b5ffb563dc3b438fb9499963daa303c843aabf70f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 KB (37136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448aaca38f5db0ee76aa76d07942718d286923dd86a741269207f4db94ccf16d`

```dockerfile
```

-	Layers:
	-	`sha256:f43875cbdd61f6884a6d1bddb6c21099cd9f8c037e2a34ce2a06910d8500f0be`  
		Last Modified: Sat, 10 Jan 2026 03:11:59 GMT  
		Size: 37.1 KB (37136 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:bc1c64727bc54bd1311de561c8dda0df8732501251c0c90562a8dcb0dfc8c724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61800361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cd7f93461aa3425c09258710da560fa4e23dff4e1af2cf6c86ee1b42dcb95b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Sat, 03 Jan 2026 02:13:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 03 Jan 2026 02:13:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 03 Jan 2026 02:13:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 03 Jan 2026 02:13:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_VERSION=8.3.29
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Sat, 10 Jan 2026 01:39:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 10 Jan 2026 01:39:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:46:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 01:46:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:46:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 01:46:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 01:46:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 01:46:50 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:46:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 01:46:51 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 01:46:51 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 01:46:51 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 04:59:34 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 04:59:34 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 05:00:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 05:00:13 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 05:00:13 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 05:00:13 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 05:00:13 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 05:00:15 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 05:00:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 05:00:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 05:00:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 05:16:16 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 05:16:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 05:16:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772e0a90d4aa4f209aab27b75a49043c6df83f144ec29ba8e6c8e964a8a165a`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 3.8 MB (3768859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb9c8b89ecca8688bdf852690f34dbf7da2dc90d2e06d7221c85ff1070c08b`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce8460d16487c23dd44b0afef57a49c4aeca53309e968b330dc8c9044d5e51`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a736463d7dd2ee2bfaad957d808f9e3be9a28ec3c989c499b775216c7815e9`  
		Last Modified: Sat, 10 Jan 2026 01:44:44 GMT  
		Size: 12.6 MB (12625816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc6445d74ed4aa2bd4ccc8f77dd75b73d199d732812858a476585b7967c7346`  
		Last Modified: Sat, 10 Jan 2026 01:44:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80989d93ce24a235ff638a6fb70647f2c7ecfb3a2931b6b35b062e122e2f209f`  
		Last Modified: Sat, 10 Jan 2026 01:47:12 GMT  
		Size: 13.9 MB (13931998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221adef8859b945cf1b47f1709367a16a1dccfb83e2a13fe048fe5605a990316`  
		Last Modified: Sat, 10 Jan 2026 01:47:11 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d4fb9ae22a70f453694500753d858f7069e711bc1bf0ebc223a75007a3bea4`  
		Last Modified: Sat, 10 Jan 2026 01:47:11 GMT  
		Size: 23.4 KB (23360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2f0b5a1fa62cfbf853f1d71893b032a1130c50b56ae7f9984e7dd9f8e9f436`  
		Last Modified: Sat, 10 Jan 2026 01:47:11 GMT  
		Size: 23.4 KB (23375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f9f63bb06904649c0f9245ddbc54d71f6ac47bacc869e500af284e7b80d53`  
		Last Modified: Sat, 10 Jan 2026 01:47:11 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e973c63ac340dc50f32646b9645e3ba9b15ec5b6d7585d322e66923ebd92be`  
		Last Modified: Sat, 10 Jan 2026 05:16:36 GMT  
		Size: 601.4 KB (601392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa075f5ff0aa8f7185cbcf39d751f7605819caac504a0afbbccb9383f26a2c1`  
		Last Modified: Sat, 10 Jan 2026 05:16:36 GMT  
		Size: 332.1 KB (332067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0de5e6d660898a1436982bfe5d01cc70af73065a2a39d697593de4535178de8`  
		Last Modified: Sat, 10 Jan 2026 05:16:36 GMT  
		Size: 2.6 MB (2602232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6188b847deb79b2aceb94679d80723a62cb061285fb0f5621a3e5c68e1c920da`  
		Last Modified: Sat, 10 Jan 2026 05:16:36 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039a8c587a74f166aee9bc17bcc93dc723ce1d9e1d6f2cb9905e73acadef37a7`  
		Last Modified: Sat, 10 Jan 2026 05:16:36 GMT  
		Size: 776.4 KB (776358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba71e50330d81f388efd5575616dcb3a797e71e09460e78fc3e13eb75b565e4d`  
		Last Modified: Sat, 10 Jan 2026 05:16:38 GMT  
		Size: 23.3 MB (23272191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:ae86132ecb056fc4b14d964753a903423464e730274a9d3b1bc85f060e3c5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0babe446cb99f2f0543702c5a93526f0580a372bbffe39b27cec302b4fe28ce4`

```dockerfile
```

-	Layers:
	-	`sha256:0b755f2c7e658e4262e574450a9d193a94b2b7c4da6a270bf5b304b029a206d8`  
		Last Modified: Sat, 10 Jan 2026 06:10:55 GMT  
		Size: 37.2 KB (37241 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:2b769462dec29b547dbcc59489cd829452067c515bf7e92482bf243d6a9f51ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61116818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195f22fba1c20ad5589e827e6e73de471a75a602534e3f70c4d09c7d87ee39d7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 07:08:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 07:08:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 07:08:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.3.29
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Sat, 20 Dec 2025 23:43:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 20 Dec 2025 23:43:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 17:45:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 17:45:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 17:45:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 17:46:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 17:46:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 17:46:01 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 17:46:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 17:46:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 17:46:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 17:46:01 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 20:19:01 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 16 Jan 2026 20:19:01 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 16 Jan 2026 20:23:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 16 Jan 2026 20:23:02 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 16 Jan 2026 20:23:02 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 16 Jan 2026 20:23:02 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 16 Jan 2026 20:23:02 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 16 Jan 2026 20:23:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 16 Jan 2026 20:23:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 20:23:04 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 20:23:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 16 Jan 2026 20:23:31 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 16 Jan 2026 20:23:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 20:23:31 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf2b817224238fa1d23d8e72c086765084b9c3459438ce980f9cee6a77a585`  
		Last Modified: Sun, 21 Dec 2025 00:46:34 GMT  
		Size: 12.6 MB (12625801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09217ba7d99997576931c510c7514fa80ddd8a9f38b01975d594b4330cf41850`  
		Last Modified: Sun, 21 Dec 2025 00:46:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ce9c17b22b4dca632a8726220a052103aff98799083528a34215300b12b185`  
		Last Modified: Tue, 13 Jan 2026 17:47:02 GMT  
		Size: 12.8 MB (12776430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9e448d31f3568c3fcbd85b71e5b33870fc46b37614cb42164de4b8dca1fe34`  
		Last Modified: Tue, 13 Jan 2026 17:47:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24d3e4af62dc7d1bbf7206feb93cb85407859b8b8d16c8d2913135a8fd7b97`  
		Last Modified: Tue, 13 Jan 2026 17:46:59 GMT  
		Size: 23.3 KB (23340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab009a391515648fd7d64da450a597c84a774d36bfb71e6305d3c9bdbb8de618`  
		Last Modified: Tue, 13 Jan 2026 17:46:59 GMT  
		Size: 23.4 KB (23355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7410e0e4ba837840adb7aa721ff007b7b004e0f1ba85134a1e126f9a424f2ca`  
		Last Modified: Tue, 13 Jan 2026 17:46:59 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e10d5566ea293d8707a81fb728894de6c825624122018f380b6468c1174e30`  
		Last Modified: Fri, 16 Jan 2026 20:24:28 GMT  
		Size: 539.1 KB (539127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af7a11084228bf2fabb7b50de45109649d4f9a73c2bd15ea80e0ca2c447513`  
		Last Modified: Fri, 16 Jan 2026 20:24:28 GMT  
		Size: 1.1 MB (1138718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85ab20adf287b5a66f6b802dd0b5562fa65c97bc05a714474ec29b36ec6454`  
		Last Modified: Fri, 16 Jan 2026 20:24:28 GMT  
		Size: 2.6 MB (2602226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b799a83bd8aec22eaf52494080ace6357b60eacf848c7a190b0c0090dd59ac0d`  
		Last Modified: Fri, 16 Jan 2026 20:24:12 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653118a25144545e7d5331022614af0197fd6eba0b42fe38d76fd4c19e46db66`  
		Last Modified: Fri, 16 Jan 2026 20:24:28 GMT  
		Size: 776.4 KB (776363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfceab5824106b296cf9c176e3bfd7a38b53884d679baf4a98b9695f379452f6`  
		Last Modified: Fri, 16 Jan 2026 20:24:30 GMT  
		Size: 23.3 MB (23272349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c74deec572b498e34bb71c96ffee5b30baaa35270ad6e5de15fec58803ad382e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11720ccd43e36bbb7deaea1227adb381d7deca539ee414a1b62987916ec72288`

```dockerfile
```

-	Layers:
	-	`sha256:276b7d6b4d1da73590f1e4447ea2c2280f56c234b01f08f6d27e1d2fc3386570`  
		Last Modified: Fri, 16 Jan 2026 21:10:44 GMT  
		Size: 37.2 KB (37246 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-fpm-alpine` - linux; s390x

```console
$ docker pull postfixadmin@sha256:aea506d659e5f2e5ada51a3aa70464ae4661febeb6786788608a5ce21eff7583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60962865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0946e75b4feb9b6004b277acb3cf770e01ea3dc653404153205986b1e1ef70e1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:30:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:30:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:30:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_VERSION=8.3.29
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 21:35:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:35:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:04:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:04:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:04:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 00:04:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:04:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:04:08 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:04:08 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 00:04:08 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 00:04:08 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 00:04:08 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 01:36:38 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 10 Jan 2026 01:36:38 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Sat, 10 Jan 2026 01:37:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 01:37:01 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 01:37:01 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 01:37:01 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Sat, 10 Jan 2026 01:37:01 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Sat, 10 Jan 2026 01:37:02 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 10 Jan 2026 01:37:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:37:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:37:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 01:37:07 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 01:37:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 01:37:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af672712b2dab3c8a68ddbd40990098668c349a31bf4fe54360519012d2e9`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 3.8 MB (3794529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e82f0b184abfa92d79d92b03514acd8b9f92c2ca083f9fa2e62587fde8871a2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b827f069b40835efda3a88ba34853291bec4baedd59564b9d33abc39667950f2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa74a07aa38feb89db7b4b2d4c17d64414b5170d824d1a0c1b04d634d4cbbd`  
		Last Modified: Thu, 18 Dec 2025 21:39:42 GMT  
		Size: 12.6 MB (12625786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bafafc99ad75690fc8e3a233809c902c7eea97daaacbc613444bbba01d277db`  
		Last Modified: Thu, 18 Dec 2025 21:39:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6eb89c26bd653be10ae36fa59bb36fe5a8d468a4934a092599ade80840ddea`  
		Last Modified: Sat, 10 Jan 2026 00:04:26 GMT  
		Size: 13.2 MB (13235386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79df6552f6128f49475a5045135d0a974c6af52c0048df3836bd0aa0cda729`  
		Last Modified: Sat, 10 Jan 2026 00:04:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a10d6c40094844f726c3877b73adeb57509d3aa00a364e51e5502a4451fa2d`  
		Last Modified: Sat, 10 Jan 2026 00:04:25 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8d04a005da9d7c1deff61092e4442c89cf04ec751fd70d4b37c037bec25ce0`  
		Last Modified: Sat, 10 Jan 2026 00:04:25 GMT  
		Size: 23.4 KB (23367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f1781812ea5eba4d7f4fd1ed5006d26f2093e3d7a24480eca315c6ff4b8068`  
		Last Modified: Sat, 10 Jan 2026 00:04:25 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67fb1bc76d90f90e3d113aa6060c3b53bd1988c37fd65639d3f03d245bfdb3c`  
		Last Modified: Sat, 10 Jan 2026 01:37:22 GMT  
		Size: 560.0 KB (559957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5126729867a9ef58a6a252685fd95b7f705868a7539f9d69130c41e7a94eb`  
		Last Modified: Sat, 10 Jan 2026 01:37:23 GMT  
		Size: 310.4 KB (310442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b900d80d6278b3ec1d3d25d0bc519eb8efac65528ec34b896f3e3e5c6eb8f3c`  
		Last Modified: Sat, 10 Jan 2026 01:37:23 GMT  
		Size: 2.6 MB (2602223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3c9b6e066deba6d722be2c565e474bbb104a6c040e222481b0a44f21f489ca`  
		Last Modified: Sat, 10 Jan 2026 01:37:22 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46930ec4f0d4aff7a7678c1c58f0cbed94944036344adb9040a0e534e1987727`  
		Last Modified: Sat, 10 Jan 2026 01:37:22 GMT  
		Size: 776.4 KB (776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a043d176c3c5854198d63e791d534a02ecea760562f64cd4e57a7f27c0ff255`  
		Last Modified: Sat, 10 Jan 2026 01:37:24 GMT  
		Size: 23.3 MB (23272200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:197c96ab17f0f9d3b553e95664581ed682e7fd3560405502d9d7556c22183648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a92911f38cef5aa7100360e97eaff74ea5acd8b3854639e4f7dac14a37983fd`

```dockerfile
```

-	Layers:
	-	`sha256:8d711c209f23261ef3274fe8115e4d8d613d1fc8f18f8fda3300dcea3267a64b`  
		Last Modified: Sat, 10 Jan 2026 03:12:07 GMT  
		Size: 37.2 KB (37180 bytes)  
		MIME: application/vnd.in-toto+json
