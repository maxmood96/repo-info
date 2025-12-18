## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:88dc7cfbc1b5681eaf3068d2a8e008f76fb418d9a3fccb8a1330afa45834d6f6
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

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:325bd47f333c650a9984ba9b702a730d9fc70b828fad03711dd5858165c4a120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41377441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9537d1a450e0d37895d575df4b5dcbbf4b113e479311f5f600cd6a04af7963`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:29:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:29:40 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:33:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:33:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:36:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:36:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:36:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:36:02 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 00:36:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 00:36:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:36:02 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 00:36:02 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 01:16:34 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:16:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:16:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:16:58 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:16:59 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:16:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:16:59 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:16:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:16:59 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:16:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:16:59 GMT
USER adminer
# Thu, 18 Dec 2025 01:16:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5582280d056ee93ee1ec4f352db074d36da5be30792cb9eec41c9ade518ee0b`  
		Last Modified: Thu, 18 Dec 2025 00:32:58 GMT  
		Size: 3.6 MB (3591476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9195846a7445311b102301da4c4c9b33e64e3e57f847427a7cfcf296c238d55b`  
		Last Modified: Thu, 18 Dec 2025 00:32:58 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f614dc8c61c8d80f8a00f17949c83871d4dd23358d0fd63586942c2e0b4c51`  
		Last Modified: Thu, 18 Dec 2025 00:32:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28203d87c73b4abac16bd6c9735f869560b368b1895a3d2cbaaae154a0c23355`  
		Last Modified: Thu, 18 Dec 2025 00:36:17 GMT  
		Size: 13.7 MB (13676364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e6af437f22ec49b87dddb2c4ff102fa80e9edb0abf2ec9c05ae59446604644`  
		Last Modified: Thu, 18 Dec 2025 00:36:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8589186cbd606cee7f3b2e3a2a2214c31873171b52a8889651f03a0c2e01f6ee`  
		Last Modified: Thu, 18 Dec 2025 00:36:17 GMT  
		Size: 15.2 MB (15174552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3461070629adaf3c9c927d497da744df06a95ce464e84e814dd1ba34d38062`  
		Last Modified: Thu, 18 Dec 2025 00:36:16 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3818df4d16747ad976cf06e35552778246948453b0bf558b2ea99dd80cecba98`  
		Last Modified: Thu, 18 Dec 2025 00:36:15 GMT  
		Size: 23.5 KB (23493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69472ac524be9a901da9fa03037ddebe3826eb73a35daadc2e29078779e8fa`  
		Last Modified: Thu, 18 Dec 2025 00:36:16 GMT  
		Size: 23.5 KB (23504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d12391b59f08f11d33f9f454bfcb87528ea570d6c12828cc0c3c4809630719`  
		Last Modified: Thu, 18 Dec 2025 00:36:16 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b107b51a88b4f81b82d90fd3e40ebc1323e083b5512a01bdac40d4d00528af9e`  
		Last Modified: Thu, 18 Dec 2025 01:17:10 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0fe2c1cef193e5359fdd0683bc819d4cd85cb85c3ea732bd3469e41e64a05`  
		Last Modified: Thu, 18 Dec 2025 01:17:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6169d931ef9f143ef908b3671af0898bc87dfc85df00f5d523e99491a36eec25`  
		Last Modified: Thu, 18 Dec 2025 01:17:10 GMT  
		Size: 4.4 MB (4370221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d8107a356a1e0decf1c1c26b7df5f4bfd23340aa387e41eaffc2eb425be156`  
		Last Modified: Thu, 18 Dec 2025 01:17:10 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066a97b59931c3ceeb0c322d149b89b89f75f7e00019fda354cf9ece640e56a`  
		Last Modified: Thu, 18 Dec 2025 01:17:10 GMT  
		Size: 640.9 KB (640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c776e4f9cd21c3cab04e9e9452b50f81eb1de0ac455b5a6c77cfb9ec28cb6218`  
		Last Modified: Thu, 18 Dec 2025 01:17:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:1ae6acb02a6a723046e4c7c5a4544ba8169f830820041f2067f9d2adcbe3cbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (33982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45565fb6db2825bc6a4447fc3d66983ce513ccfd1bf63fe7f63fef4f39e70fab`

```dockerfile
```

-	Layers:
	-	`sha256:66305b77226d9809f35e0db836fc1cf13f7b927688cb02bccf5c0a7734b26f72`  
		Last Modified: Thu, 18 Dec 2025 04:50:40 GMT  
		Size: 34.0 KB (33982 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:900aaa82e951fb6ab8621167128ccbbd0a331328878d104d3fee7f27795b4a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39134342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa3e8aa21fa88fd15dec625b4f036ab45f4e41dbfae8b9f1ba975a5e79fafa5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:34:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:34:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:34:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:34:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:34:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:34:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:34:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:34:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:34:29 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:34:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:34:29 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:38:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:38:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:41:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:41:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:41:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:41:07 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 00:41:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 00:41:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:41:08 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 00:41:08 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 01:34:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:34:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ecc8841a5ef867ff72e8a5015b2378fe3007b3fad53ed75fc76f953e52acd`  
		Last Modified: Thu, 18 Dec 2025 00:37:53 GMT  
		Size: 3.5 MB (3548042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0078fbe24ab98cc1bb103570e40ef173dea37bc0028861d209d2df6c309e44d5`  
		Last Modified: Thu, 18 Dec 2025 00:37:52 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77269d22aad414845a1939d48f1c928e5489a7b8ee55f09b631f879d8c15fa21`  
		Last Modified: Thu, 18 Dec 2025 00:37:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d12444239ba021fcd2ebbd2b7fe8caf23d970b490eafbc39de87bec1cc783c`  
		Last Modified: Thu, 18 Dec 2025 00:41:23 GMT  
		Size: 13.7 MB (13676367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78cfd4a009edf3fea5a2b31c888e8edf2053b59b08fb11849c038ea1f09c306`  
		Last Modified: Thu, 18 Dec 2025 00:41:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b9dbdd2bcedcb1c95bde213f271eacd6e4f105e4b0abc3927c08809ab24015`  
		Last Modified: Thu, 18 Dec 2025 00:41:22 GMT  
		Size: 13.7 MB (13667782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4867adbe41fe6e5d6b8b7e6a4621107db23965714617faac5b7e1c2cd51e8d8`  
		Last Modified: Thu, 18 Dec 2025 00:41:20 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91272db02df5e07a9353541c667f4ee4f3d43e6240f496b9864a75902e544d`  
		Last Modified: Thu, 18 Dec 2025 00:41:20 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcf6e6411ca29b054ec342507118ef77948b5b422b447c61c59e0e1389fa257`  
		Last Modified: Thu, 18 Dec 2025 00:41:20 GMT  
		Size: 23.3 KB (23343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d7dbeb02d7e28ae91141c34822f05da00d3161f8bb9711cf69cd2ce8f01072`  
		Last Modified: Thu, 18 Dec 2025 00:41:20 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12701a4c94e5308c5c95b2d088597aa6a79e5e4a685057d7f7bb0fd89b08747d`  
		Last Modified: Thu, 18 Dec 2025 01:35:27 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d87dcb683ae9efa02e140e43539515e84a22de964a4786d5e00a491f8d2b97e`  
		Last Modified: Thu, 18 Dec 2025 01:35:27 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c40082751a99e1de79d812c5a04f4adb5c36da50f56826e856f5c82d89b348e`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 4.0 MB (3969324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efa48b408b0bcc603737b9c9dc8feb2b70b1d31fd5c0076395ae4894ef9577b`  
		Last Modified: Thu, 18 Dec 2025 01:35:27 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43da7c2ab9f4dc010cdaddcf414359d06ec8c0e6e054e0578dd1dac4ecf69eeb`  
		Last Modified: Thu, 18 Dec 2025 01:35:27 GMT  
		Size: 640.9 KB (640866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2141f123e7d053bd23aa6a39ef2feb15e0d07e7379ff5fe77d3793ac99e0a2c1`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:7103a825bd0760ee594775f8040a8fa9b7d7cb3f34fe14f9e875512bad16d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2316fc82edd83d9c1cfe4ce48fe4cecb6d002070d12e7f5b646c23480d83ce4a`

```dockerfile
```

-	Layers:
	-	`sha256:933825b2a2ed85e37dc1695ff4be8df71326d7ca23a6da99c5a5408d5df53edd`  
		Last Modified: Thu, 18 Dec 2025 04:50:43 GMT  
		Size: 34.1 KB (34094 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:60cb32a42f22c02219a5a0a5a6e664f0ba0969ed6a5a8f494c82aac131815d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37952655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cc594958fb21b3ba29e1e6ab19c8bc3be7151260591d0cda522e78df59fd3a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
# Thu, 18 Dec 2025 00:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:38:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:41:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:41:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:41:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:41:17 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 00:41:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 00:41:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:41:17 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 00:41:17 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 01:34:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:34:50 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:35:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:35:23 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:35:24 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:35:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:35:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:35:24 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:35:24 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:35:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:35:24 GMT
USER adminer
# Thu, 18 Dec 2025 01:35:24 GMT
CMD ["php-fpm"]
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
	-	`sha256:1a594438dfb0570e0a677cc1a7f5dc3a6758746b9f448933df44c02e3f720f2a`  
		Last Modified: Thu, 18 Dec 2025 00:41:32 GMT  
		Size: 13.7 MB (13676370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e364f0ed91f995b900059a7be771f3a8a6aef28613b05e1ad2392cb1162a9`  
		Last Modified: Thu, 18 Dec 2025 00:41:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ffbcf8a27b5e9d6d4ffd1c325618f8fc532cf0cd2260e33e670cc21f8b69d5`  
		Last Modified: Thu, 18 Dec 2025 00:41:33 GMT  
		Size: 12.9 MB (12905756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aa9d49c3573c19b75b4089f35eeacefc1c10d87c843a9088475c09f4867f5`  
		Last Modified: Thu, 18 Dec 2025 00:41:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cb8ee7798fbfb33d04f3101fa3627c8cb80fdbda3a911be603dc038521060`  
		Last Modified: Thu, 18 Dec 2025 00:41:31 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c217316f561fb1a557d84322ceac68508e6e9e8294666fa45c6f28b6443c25b5`  
		Last Modified: Thu, 18 Dec 2025 00:41:31 GMT  
		Size: 23.3 KB (23348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aceeecc9292eb3f261de612ec54d2a590a641fe4ef836302827c6057620ba1`  
		Last Modified: Thu, 18 Dec 2025 00:41:31 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec41b3a80986082e14c7b034c4494d757252374226ad16d0978ca6b70e1f4f81`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a670812dfd7c0b3833d3900392bcf970cfa5123c2840693cef356a1cebc882e`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4502ccb6f9a9639c748d56bc4e95784a8a4e80528726c2c03b81052a6573c`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 4.0 MB (4039955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027b3c4f0fb742819aa3416fe8d2b4e574d7ed57f208a90873a92948f53fcd99`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6538db41a7de9cfab09bc52970e313de694ed7580aba8bf83be179d20a9fe6c`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 640.9 KB (640872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f04cc06326eb64ad1057da37ce151e42cea766ea6da9868cef5c84ffe98ac8f`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:13c852ce9cd68d0dade2dc384e96578dfe0b148ac45ba5b23ce6696ee0ab4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42d8d32de837694a442ab70d05ea9883d56b9d042a4c80f10880e6f828ce89b`

```dockerfile
```

-	Layers:
	-	`sha256:dded15568c6f106da52097f43a56a2b018487632433fecf1bddfc1d03702fb35`  
		Last Modified: Thu, 18 Dec 2025 04:50:46 GMT  
		Size: 34.1 KB (34095 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:21cc0cf3da24b0fc4c680d63c5dad83f5d1a0c360d2190e6863ffdf0a5970a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41224860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab3de7c3507aceaed3ba9ea149de2e9049e5aaa127d9bc0765f9e6a44ef061a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:27:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:27:49 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:31:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:35:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:35:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:35:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:35:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:35:01 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 00:35:01 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 00:35:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:35:01 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 00:35:01 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 01:23:57 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:23:57 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 01:24:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:24:31 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 01:24:31 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 01:24:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 01:24:31 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 01:24:31 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:24:31 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:24:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:24:31 GMT
USER adminer
# Thu, 18 Dec 2025 01:24:31 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca7f18269dee9bf9fb760a5325bae8448ce2ecea648a880ff960e786f732070`  
		Last Modified: Thu, 18 Dec 2025 00:31:35 GMT  
		Size: 3.6 MB (3600950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2791cbda59da4f7bb1afb93901c41a8c16618dc698ed42d9fadc9a2046fac`  
		Last Modified: Thu, 18 Dec 2025 00:31:35 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a2550c5e4c02e304302c4835e5f6a0d566235da35382c9172d102ebc7735f2`  
		Last Modified: Thu, 18 Dec 2025 00:31:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4df4ad1f8075830b5b522294333152bd6940bdf9fdb9991079f606977f89a9`  
		Last Modified: Thu, 18 Dec 2025 00:35:17 GMT  
		Size: 13.7 MB (13676356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e01779360ced48958afab153a9bc16270320f1888f518b3567903a9868043`  
		Last Modified: Thu, 18 Dec 2025 00:35:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d5832d6f29bc9f631616d6ff65b1794c7d8040beb888fab903382e90bc4ada`  
		Last Modified: Thu, 18 Dec 2025 00:35:17 GMT  
		Size: 14.7 MB (14683910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a21039b53ce120c15471d73ea1a6155376256a35f482db143423a4373435ce`  
		Last Modified: Thu, 18 Dec 2025 00:35:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2596aabed34c4e923d00809c9a614e6ea4b97fc17120ae2f0fc5c275d26ff8`  
		Last Modified: Thu, 18 Dec 2025 00:35:16 GMT  
		Size: 23.3 KB (23342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f702ca46ee2f6e367ef6ac86746a1402b2304ee917c99d3b58fc8f78c4881d3`  
		Last Modified: Thu, 18 Dec 2025 00:35:16 GMT  
		Size: 23.4 KB (23359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88030eda7dcb326b36dc0bfec86e70a5c59f854513eb83d6043c21c83415c225`  
		Last Modified: Thu, 18 Dec 2025 00:35:16 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed9a35712c673bd4f7ef375f2a559f3193c917e6e5ffb4cb56daf48b701517`  
		Last Modified: Thu, 18 Dec 2025 01:24:44 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9434ddce0a9d4ad5d9d6a83a3dd7ebb042a43377648a6a433ff3940c91ebe392`  
		Last Modified: Thu, 18 Dec 2025 01:24:44 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5278316f8085524209d4cd9111882f555701055ecec39aa9917b5a545caddfe6`  
		Last Modified: Thu, 18 Dec 2025 01:24:45 GMT  
		Size: 4.4 MB (4363490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbc88a5f72c37f6e7272f52ed07c15874b4b96d28f1c47957627141110c8ce4`  
		Last Modified: Thu, 18 Dec 2025 01:24:44 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ee9b872ffc7d841d90abf240dec626c355f451915630b1d35494473a76747`  
		Last Modified: Thu, 18 Dec 2025 01:24:44 GMT  
		Size: 640.9 KB (640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fed5f4841c376fdf87ee4cdf015430462d902875a24ee1f973c6d226df4454`  
		Last Modified: Thu, 18 Dec 2025 01:24:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:b92efded0ce158ca01d4256e59b563e0be5f48b1150e9720822795aa002e80d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589da0be23e16bd9d6cb1dafeb4213e5a0547645f1727167e0e2e66237f64525`

```dockerfile
```

-	Layers:
	-	`sha256:7efdef391d2d71f2ec8e1b9c00812e65fec104365377b53f2319e9d40061aae7`  
		Last Modified: Thu, 18 Dec 2025 04:50:49 GMT  
		Size: 34.1 KB (34120 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:90fec02c7f73264e2b42fc1d0cc591fd76bb7e1915106b6e0f9f4aa3c9ab7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41381108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c5032cbf662aa824d0b7d1e3cab932fee7b3c0375564c2b5d56be17ab7015b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:30:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:30:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:30:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:30:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_VERSION=8.4.15
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 18 Dec 2025 00:30:17 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 18 Dec 2025 00:34:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 00:34:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:37:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:37:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:37:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:37:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:37:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:37:32 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 00:37:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 00:37:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:37:32 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 00:37:32 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 01:16:26 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 01:16:26 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
# Thu, 18 Dec 2025 01:16:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 01:16:52 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:16:52 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:16:52 GMT
USER adminer
# Thu, 18 Dec 2025 01:16:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c688a2a8129a5ccbe2065c49f91e3c7a52c26cfcf637b3a8f6d786c51689b3a0`  
		Last Modified: Thu, 18 Dec 2025 00:33:59 GMT  
		Size: 3.6 MB (3628728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f12e891d65501876e8bf3c7fc38f88ffae5a86904f4aa1942bd960f70b25d8`  
		Last Modified: Thu, 18 Dec 2025 00:33:59 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd61b524c85c4604bcefbe19a0246826117689a4e74c325c755a5d9306db950`  
		Last Modified: Thu, 18 Dec 2025 00:33:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d051ef3a565b577ae77e61f2b591acd36049b4565bff8f6038dbaaab4da93d`  
		Last Modified: Thu, 18 Dec 2025 00:37:48 GMT  
		Size: 13.7 MB (13676350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9eb8bcfa7e4168ea5d44da38cc4047acef09b37d6dc5baca8a054779596944`  
		Last Modified: Thu, 18 Dec 2025 00:37:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f6383e2019c71f009189874352b6fb9c2660061e1d210f7534c2f0ef7fa27`  
		Last Modified: Thu, 18 Dec 2025 00:37:48 GMT  
		Size: 15.5 MB (15485430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e863246594ed903e47a4a730ac3ee471d6b73826ea61e59ddf1c25c1d2a7b727`  
		Last Modified: Thu, 18 Dec 2025 00:37:47 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829846004d6ef3a39126b67e1a23f45b28ef58515cb04a92a3dde5454e0968b8`  
		Last Modified: Thu, 18 Dec 2025 00:37:48 GMT  
		Size: 23.5 KB (23500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c86a93520ad25abe4868d481c1fdf754452ba724e0150ce17c6abb79f7a099`  
		Last Modified: Thu, 18 Dec 2025 00:37:48 GMT  
		Size: 23.5 KB (23521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff704ca5eea079c426e915aeef815d72a0f8f171ebe962cc2dbba69efd7efbb5`  
		Last Modified: Thu, 18 Dec 2025 00:37:48 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d119a6665d67c5ef91b2d0578fa0c1a7824f3cc47c9b6545c775a00722726fdd`  
		Last Modified: Thu, 18 Dec 2025 01:17:03 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7820f76663771036ecda4474689d3080b90fc07a7328a99d6c49ba8f3bf1e310`  
		Last Modified: Thu, 18 Dec 2025 01:17:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16891ae82376e633f0b48b6351bc00e1046b4bea3b60e6d8247e259f2883a410`  
		Last Modified: Thu, 18 Dec 2025 01:17:03 GMT  
		Size: 4.2 MB (4199766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03bd9c2c51da6ea4ca505165e1f8ae93560115155cfc8690acd8775863fbc48`  
		Last Modified: Thu, 18 Dec 2025 01:17:06 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccbc1ccae4faefaf6f87eacaa4c8a1919d7043d66acc484dfd84170a1c78c3`  
		Last Modified: Thu, 18 Dec 2025 01:17:03 GMT  
		Size: 640.9 KB (640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32e8c9f5652e75aa1ae883ba8e5a58a91ccdb84ade7b4ad918924167060bb`  
		Last Modified: Thu, 18 Dec 2025 01:17:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:a2a200a2dcfe3b16e3e9dc47789a7dc4194e2688334167e3cf33429596df03d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (33951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab13c481a5fc734aadd06a1f1fc0cc4e8fb58962c1bb5f5ff0230d73548fe73`

```dockerfile
```

-	Layers:
	-	`sha256:7de0d48d08d99270f0691d007747b15d0f93dc1f06da5079b4f88ea10ff537d0`  
		Last Modified: Thu, 18 Dec 2025 04:50:52 GMT  
		Size: 34.0 KB (33951 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:daa43bf7f593907eabb6b6a9a403e72b348beafecb4837cbc83a1df253edbf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41970355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062ffc92f9b181c18e603304fc034878addb31bea5d9fb10089893e1c5a36418`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
# Thu, 18 Dec 2025 01:05:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 01:05:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:05:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 01:05:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 01:05:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 01:05:23 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 01:05:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 01:05:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 01:05:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 01:05:24 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 02:39:07 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 02:39:07 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 02:39:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 02:40:02 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 02:40:04 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 02:40:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 02:40:04 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 02:40:04 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 02:40:04 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 02:40:04 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 02:40:04 GMT
USER adminer
# Thu, 18 Dec 2025 02:40:04 GMT
CMD ["php-fpm"]
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
	-	`sha256:7e588f3d8367518708ac284b4fc06c58b46d8399c8790ac3df872b273e48f9f0`  
		Last Modified: Thu, 18 Dec 2025 01:05:54 GMT  
		Size: 15.7 MB (15716529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dc2c8868a465d27a4ca659534443c620aa11e133edfe5103392c2cf9bc672d`  
		Last Modified: Thu, 18 Dec 2025 01:05:51 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912e7ce5142bd82464539244aefb3f26da199d0003360c2bb5ddea2c2f1a979`  
		Last Modified: Thu, 18 Dec 2025 01:05:52 GMT  
		Size: 23.4 KB (23351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21a032b470d29019038505ce7a7f6798ae9c8d5ac9297ef9939d9907863ff09`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 23.4 KB (23371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb002b1b0f03696dc29f7789416562612ee326d22feb9747461cae3ecb39d4d`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2859b81d12ca6428cc0af232a8813e2ef70bb92a78a6aa0df5e18d57a0966872`  
		Last Modified: Thu, 18 Dec 2025 02:40:20 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e77697bad4e28e94a7c95c05b4cd81018af7d8d0e61667f67fdad71a2a104b9`  
		Last Modified: Thu, 18 Dec 2025 02:40:20 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb8e5fa1500dd79be78b5bc07f58de97fdeda1af1dd37ce95129fce57053d6f`  
		Last Modified: Thu, 18 Dec 2025 02:40:21 GMT  
		Size: 4.3 MB (4276384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4674ebba091f45124fb13306363b308ea844d0a0ddbfa1992dfbb2b344fc805`  
		Last Modified: Thu, 18 Dec 2025 02:40:21 GMT  
		Size: 1.7 KB (1699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993d7c58aac0d5b681e65245fabb12503dd1d794a9ab610e211e10c0e1287c7b`  
		Last Modified: Thu, 18 Dec 2025 02:40:21 GMT  
		Size: 640.9 KB (640865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231ec569df920d17f0d45cb17ccdb57c63d08b049f2cc4fe33c45c79c806409`  
		Last Modified: Thu, 18 Dec 2025 02:40:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:452496f8019e8011184198c37f0ca88ceb52f052a9e6fbf4d3837106c050b516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386c338c2143733eaab1471c4971f133b6cb67d3585e63d8655508d807df7a89`

```dockerfile
```

-	Layers:
	-	`sha256:d0786295eee69641ae08480a966478181bf5dbac65b30ba50145c6169428bd2e`  
		Last Modified: Thu, 18 Dec 2025 04:50:55 GMT  
		Size: 34.0 KB (34028 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; riscv64

```console
$ docker pull adminer@sha256:6b7d1d9307ddb61fc3e473b9ce19451406e8b013b45340b419635c9cfd9e6079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40094712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b8325145482151c00d828a2712390c5109ff501380c40cb2ccc212633f464`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
# Thu, 04 Dec 2025 09:25:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 09:25:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 09:25:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 09:25:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 09:25:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 09:25:23 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 09:25:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 09:25:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 09:25:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 09:25:23 GMT
CMD ["php-fpm"]
# Thu, 04 Dec 2025 17:59:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 04 Dec 2025 17:59:50 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 04 Dec 2025 18:05:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 04 Dec 2025 18:05:25 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 04 Dec 2025 18:05:28 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 04 Dec 2025 18:05:28 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 04 Dec 2025 18:05:28 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 04 Dec 2025 18:05:28 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 04 Dec 2025 18:05:28 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 18:05:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 04 Dec 2025 18:05:28 GMT
USER adminer
# Thu, 04 Dec 2025 18:05:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:9ddc5f3cd1bc938589d3af8bee2a0a760eac5593351c8cfbf7daa966d79bd79a`  
		Last Modified: Thu, 04 Dec 2025 09:26:30 GMT  
		Size: 14.5 MB (14451333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dea69d8712081a20f50702211ef8728c137aef12d913a49d7b3b2210aa82298`  
		Last Modified: Thu, 04 Dec 2025 09:26:29 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce5c9a07f0e52fb87d03303a9f5405bb267fc835bc6e3c87635f0f0732cebf`  
		Last Modified: Thu, 04 Dec 2025 09:26:30 GMT  
		Size: 23.3 KB (23308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f45b2944ae118a8ba724c516eb2a8946f88256c5d31706a46d89fb1ad4b979e`  
		Last Modified: Thu, 04 Dec 2025 09:26:30 GMT  
		Size: 23.3 KB (23336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deefbbba63184595d7d47d0b71530760ce003b267843b476a5c4b464abb797ab`  
		Last Modified: Thu, 04 Dec 2025 09:26:31 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc2b9ec1f85b4ce7feddc6396a58f88819ca4ce244eb83be542e4399398ca3`  
		Last Modified: Thu, 04 Dec 2025 18:05:52 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b20c75312d1c741f6dbfc990183a1b34c6fa176e43c10b04647d0066e55fa`  
		Last Modified: Thu, 04 Dec 2025 18:05:52 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042d00aa1494b16251ec91aa661591f01d15578b4df27dd91850d6fe260550a`  
		Last Modified: Thu, 04 Dec 2025 18:05:53 GMT  
		Size: 3.9 MB (3939142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fa0f6bb0e28b31c311ab1efc24ef701399243ae4a0d5da86a29f2a347f9264`  
		Last Modified: Thu, 04 Dec 2025 18:05:52 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d6e7901788fc75d8360d95ad8c23ed57a5c204a31c796f5564bd8ede0ebbb3`  
		Last Modified: Thu, 04 Dec 2025 18:05:52 GMT  
		Size: 640.9 KB (640876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d567ceafd5da0d899e07ad7d035f6fa6a309fec6187b3a3d9003d9e34ca52663`  
		Last Modified: Thu, 04 Dec 2025 18:05:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:4ba2610e167719afeb9ab77889f016efe1e9c2aa32bcba8c05cfc5a5e381bc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3fc162e2a50cbcff043e12cbff8fbfa78bf1fc7f4fd316eb8119760568527`

```dockerfile
```

-	Layers:
	-	`sha256:25d6fc0347e3fd8c47272bd3d7d9a348aaa47a487c3c9ff18630dc22bb9b3a84`  
		Last Modified: Thu, 04 Dec 2025 19:49:36 GMT  
		Size: 34.0 KB (34028 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:d6154e4c940fa72e3b3824077c558763bd79b802a255dfddb27e4a76aac1fe8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40981356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2464457317ddc5be1d0c3fd6eb8a882ccc60c87d4094e937aa43563bd54fd70`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
# Thu, 18 Dec 2025 00:55:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 00:55:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:55:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 00:55:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 00:55:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 00:55:32 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 00:55:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 00:55:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:55:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 00:55:33 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 03:47:42 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 18 Dec 2025 03:47:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 18 Dec 2025 03:48:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 03:48:16 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 18 Dec 2025 03:48:17 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 18 Dec 2025 03:48:17 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 18 Dec 2025 03:48:17 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 18 Dec 2025 03:48:17 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 18 Dec 2025 03:48:17 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:48:17 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 18 Dec 2025 03:48:17 GMT
USER adminer
# Thu, 18 Dec 2025 03:48:17 GMT
CMD ["php-fpm"]
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
	-	`sha256:65421836992505b4c6015242dd6e9fa4b682c4b23b3b2af556040df7764094e7`  
		Last Modified: Thu, 18 Dec 2025 00:55:57 GMT  
		Size: 14.9 MB (14930025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ca59dddc57cad08f41d3139e6783beb8f7bb2c365ff56feab8f232fb5daf0`  
		Last Modified: Thu, 18 Dec 2025 00:55:56 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a59d55592d68d4505ac89559a7b56fcc83f94fe68b78d43af625b6d3e7345`  
		Last Modified: Thu, 18 Dec 2025 00:55:56 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d2be7c59e6e76a61bebb90d671bd76000431ab62745a63c192631f1a6f7669`  
		Last Modified: Thu, 18 Dec 2025 00:55:56 GMT  
		Size: 23.3 KB (23348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42d899c02d049f29e3144fd8f42fbfa3ed4397859347d826ec35fea7e3651cc`  
		Last Modified: Thu, 18 Dec 2025 00:55:56 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf62e3196f121710e68003549d90139e79b58ae0398c3f2bf1d2b6dec4b6274`  
		Last Modified: Thu, 18 Dec 2025 03:48:29 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd1ba527fc6c265d7cbf4bb6d95d5995dcc07ff7ca10d44d2687850b15fcf17`  
		Last Modified: Thu, 18 Dec 2025 03:48:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eb032953aaf6f77cbe2eb996ded1cdfa7e2cccc55a4e71ac3ff6aefee38871`  
		Last Modified: Thu, 18 Dec 2025 03:48:30 GMT  
		Size: 4.2 MB (4151757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d409cfb13dd5804d390caf877f46a0dbcc16885fa95913d322a1aeda08b2`  
		Last Modified: Thu, 18 Dec 2025 03:48:29 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be825564ccc42a3b0d4a2ed5380a143c8bc6189cbf25252ae172a5b903c7e312`  
		Last Modified: Thu, 18 Dec 2025 03:48:29 GMT  
		Size: 640.9 KB (640865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8ac8bc6dd08d7d097039047978a825beb8f415e3631d2dd6178d706a482b9c`  
		Last Modified: Thu, 18 Dec 2025 03:48:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:4ec46d187d68486208c14de86bb436e79289d2a0776f22382261471045755c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (33984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e91b5cbe43394ad0c72de6f216371ba38cf377bee7b84cd01634f37d7222e18`

```dockerfile
```

-	Layers:
	-	`sha256:fcf654d31184081fe77bde7c394ce2079fa1b49b18d3461571ff872e6ad93ba6`  
		Last Modified: Thu, 18 Dec 2025 04:51:01 GMT  
		Size: 34.0 KB (33984 bytes)  
		MIME: application/vnd.in-toto+json
