## `php:fpm-alpine3.23`

```console
$ docker pull php@sha256:014c142087e9cd4cfcc71475d49c652fac9ae4302685597e3558eab77f717af5
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

### `php:fpm-alpine3.23` - linux; amd64

```console
$ docker pull php@sha256:77eed413b53ad667e53935923cd13e4f98c911d315bfe57273de074a15a32b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38462597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62096150463c31508bbdc0f8d79dc297b2cf830673cb02665116fcc736f9c6a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:20:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:20:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:20:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:20:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:20:34 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:20:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:20:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:24:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:24:07 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:24:07 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:24:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7823efeab626d735314f135c1a03858aaba82b6744c83af8dce38e44581a9b8d`  
		Last Modified: Wed, 28 Jan 2026 02:24:15 GMT  
		Size: 3.6 MB (3591768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e1a42e60c2fc912fc787ae16582169d42202c366f06d383156affc52230f04`  
		Last Modified: Wed, 28 Jan 2026 02:24:14 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd474027ebc9e2e9ebc0d19a2eda1cff469405ff96d0bde61dfadd826b5c7545`  
		Last Modified: Wed, 28 Jan 2026 02:24:14 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6353b109fb07f5561d2be0882b6c22482e52ef2bc41e260cc8416ea1520b23f4`  
		Last Modified: Wed, 28 Jan 2026 02:24:15 GMT  
		Size: 14.4 MB (14355566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89fcf48d8f601a71c7c88842718a626c67724e77c7c6b02a0add7fb7aa7283`  
		Last Modified: Wed, 28 Jan 2026 02:24:15 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30784e3108528181c06eec83e1e76a617223a3b5a1cdfa5d7a0630f8af2b7ce`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 16.6 MB (16616569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9f61e57ec84994f37d7c1ed178b2822506c45c0700023a195b94cf35972193`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0660e91918c8851046f53adf3996910c378751421db083293c8a6ac9044e01e7`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 23.5 KB (23497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b537ac732474b0b35466659fceb6bddd904300738dd3d12db6ffa5679dadc2`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:f3ba1bd1088952a105e9db56c290568e0a3684162d6a6741967f87299b1bd55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 KB (331120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba404c479d1412fcae6eb44ac44ba6cb29d461a5ac373d04eca820aa8b64bf1`

```dockerfile
```

-	Layers:
	-	`sha256:1020cc77960ad1edbb3b951e11ed2b70609e7d51c7d001bcf5a4fa4844fbbac1`  
		Last Modified: Wed, 28 Jan 2026 02:24:14 GMT  
		Size: 282.1 KB (282118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002ea16d5e362c4bf2c53c4a61328549d343a0b1e268b1a29cbcfbb7abcf7a08`  
		Last Modified: Wed, 28 Jan 2026 02:24:14 GMT  
		Size: 49.0 KB (49002 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; arm variant v6

```console
$ docker pull php@sha256:378a31f02bfe623d8a09b46be609226bfe594a64bd1bd17a5a6f971e8706bb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36077763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9271ffb66ddbac64fc2f1876be88d70a7ee444cc76c76c0c3e8eb8eba670eeda`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:26:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:26:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:26:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:26:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:26:57 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:27:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:27:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:30:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:30:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:30:06 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:30:06 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:30:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:30:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:30:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082da126eee59fbee4bdac3526fc6e802b1688e4a111a209f42d05bc14805134`  
		Last Modified: Wed, 28 Jan 2026 02:30:12 GMT  
		Size: 3.5 MB (3548649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6071bb81e00ef7cfd3f097fc5164026c03a043fb1f11ae52bd1d99bf22195596`  
		Last Modified: Wed, 28 Jan 2026 02:30:12 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017bb438e2037a8b30354733c83ce1f791232a5dfe7fd3ad823d561811beadd7`  
		Last Modified: Wed, 28 Jan 2026 02:30:12 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5170540ea75e8b8dae8d65a6c59bcccb9a2c2ac94ae8ed67d2446759b0c89bbf`  
		Last Modified: Wed, 28 Jan 2026 02:30:12 GMT  
		Size: 14.4 MB (14355584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a85e6e13f412d3392cd17a6541fd469cc596d2ac779253a06029edec0d7b2fb`  
		Last Modified: Wed, 28 Jan 2026 02:30:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351883efa10c2a6d460f7b29f4a63993f8845b6a576c340dc53729be41d170c`  
		Last Modified: Wed, 28 Jan 2026 02:30:13 GMT  
		Size: 14.6 MB (14567019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79fd82d52443e8bb6de03b1550f5dd5548c08a828e8e74861877cab0e82a78`  
		Last Modified: Wed, 28 Jan 2026 02:30:13 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a4731215f9e160d7f48f3fd6bb3c4810307f80f5bbbde48d7b1756bc081239`  
		Last Modified: Wed, 28 Jan 2026 02:30:13 GMT  
		Size: 23.3 KB (23316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a1af273856cefbf165b0aadb21b6c494f4682697a0f778790fef9874f62df`  
		Last Modified: Wed, 28 Jan 2026 02:30:14 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:f2ef823a646142d8bff4b19d6aa241349de9d2c707bea2f643edbb8daf30e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (48976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b0010521e4fb0487496e634660bbb33f1dcc9838f262b2d9033faaf362704`

```dockerfile
```

-	Layers:
	-	`sha256:dc5e722cb0e874c209e46df41192db6173eba1ccfa5f8704dcd1906e0f5cf967`  
		Last Modified: Wed, 28 Jan 2026 02:30:12 GMT  
		Size: 49.0 KB (48976 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; arm variant v7

```console
$ docker pull php@sha256:f319776cb9ce11b065bb26110d1166ca9dc13dab891beeef38227718b7693270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34786254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73e7f44c80b8944db227b3dd19c955b6f0958f1882c9a008060144ac3a25026`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:24:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:24:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:24:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:24:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:24:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:24:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:24:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:24:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:24:31 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:24:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:24:31 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:24:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:24:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:27:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:27:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:27:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:27:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:27:45 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:27:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:27:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:27:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:27:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83ee2875db5734cafe4b8c1e99a9f3876de0b27fa866b726a2a974b7a64a5fb`  
		Last Modified: Wed, 28 Jan 2026 02:27:52 GMT  
		Size: 3.3 MB (3347448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af81ebb6855cc5ff87bedce7c960191bee72bc0773ee8fe26e6d9da446586dc1`  
		Last Modified: Wed, 28 Jan 2026 02:27:51 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab481d5ad485851b61a45970104213984c96d16ba7ca19a67e9d6cd773a864`  
		Last Modified: Wed, 28 Jan 2026 02:27:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2597a0833c2badf75bf409be70c69580d9634581bfa315203b6018243e88cbb1`  
		Last Modified: Wed, 28 Jan 2026 02:27:52 GMT  
		Size: 14.4 MB (14355577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6251b2057c82e3413140f2064d06f64b189aa7b4588c112c4e5cebdff1695c73`  
		Last Modified: Wed, 28 Jan 2026 02:27:53 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3bcaf98ca37f7e6b7d659df6928c63af338818a542fec013e2381ac202492e`  
		Last Modified: Wed, 28 Jan 2026 02:27:53 GMT  
		Size: 13.8 MB (13764802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acfe930e2603cc2a36efba007bdb098620ceae280ded0a1f65de98c187093`  
		Last Modified: Wed, 28 Jan 2026 02:27:53 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429bf1255f8be35df9f54dfa1543cc3e642a9a832cf86f762ad50eceb4345d10`  
		Last Modified: Wed, 28 Jan 2026 02:27:53 GMT  
		Size: 23.3 KB (23322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdedbc741dd76869d9ad452e3a41238970d16470bd7752c9b1f2f05353970f66`  
		Last Modified: Wed, 28 Jan 2026 02:27:54 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:8664a67ce357eca899e9cc8e1a7a73dc6fe9f854dfe138d4995f959ce915406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 KB (327737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b959bcfe04dddc46f92f4a90742c78e1964420c43cbdf64fb24be819a4c7298e`

```dockerfile
```

-	Layers:
	-	`sha256:d13ad6a9c7323d5a4bc792d2aff9b936ef9e3e5704e14685464c6c7d9cce3370`  
		Last Modified: Wed, 28 Jan 2026 02:27:51 GMT  
		Size: 278.5 KB (278546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64cf5044f45a96c64f40581d22e721f3c974247546b32af86576c1ffe82c36a5`  
		Last Modified: Wed, 28 Jan 2026 02:27:51 GMT  
		Size: 49.2 KB (49191 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull php@sha256:b9a189aa60bd3b752115aa2632e8bc10bfcc415ff403911d87562415c1cd36a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38221653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62149c7fc33cc7dfbdc237a76e75700395340e2096db63caa5f2919d03124670`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:20:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:20:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:20:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:20:13 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:20:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:20:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:23:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:23:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:23:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:23:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:23:39 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:23:39 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:23:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:23:39 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:23:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9861190c74051a2348c9047920a9a76dc4ac8c4f3c579bb0dfe5bea20533d102`  
		Last Modified: Wed, 28 Jan 2026 02:23:46 GMT  
		Size: 3.6 MB (3601813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38722b5fb59e7b6f02e2d963e3fbbaf7eab73aae36fe407b85abc6904021c77f`  
		Last Modified: Wed, 28 Jan 2026 02:23:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edc259f7b6aef9737fa92ec8d0bd5d4f5e9bbd73f2b8c0b0c7a6ffc9276c11b`  
		Last Modified: Wed, 28 Jan 2026 02:23:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc8edc8356be7ffb024c30e22947afda56b7e853333a1ae3d8d753eb97657fd`  
		Last Modified: Wed, 28 Jan 2026 02:23:47 GMT  
		Size: 14.4 MB (14355567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c63fdee2bf184a03c4342d8e17e86ec5e78352b48f4dec6fae95546b298e4d`  
		Last Modified: Wed, 28 Jan 2026 02:23:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f2497c0418ce6b09be68408a8dad2eda39f0d009f80182032af37cc6d95ba`  
		Last Modified: Wed, 28 Jan 2026 02:23:48 GMT  
		Size: 16.0 MB (16030461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a417bf7f57846dc9dd58e8226913985aa19d2bc0e26111e638ae7ea7f5d431`  
		Last Modified: Wed, 28 Jan 2026 02:23:48 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651f437a3798adb14a80f7fe7c88c9349ba2b4b8c11a29694ae4b46a181d4ccd`  
		Last Modified: Wed, 28 Jan 2026 02:23:48 GMT  
		Size: 23.3 KB (23341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e0fca79a8d139e1afaf24d53490ce7384ec1eb0c415e267b99822aa115df5f`  
		Last Modified: Wed, 28 Jan 2026 02:23:48 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:91d2658b501d817985c2eb0c25f18de6ca98c17a28307a4897bd67920502ad2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 KB (327826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ea1c46461652b0811a8046f52f8485110564c1bd6d53c935aadc4e5e0acd34`

```dockerfile
```

-	Layers:
	-	`sha256:d02b3bb9141eaea261116c41aee2109617f4c23b784858e39bb611759f36346a`  
		Last Modified: Wed, 28 Jan 2026 02:23:46 GMT  
		Size: 278.6 KB (278582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a0830bfd8e7195432aa3d1a9969618de2ce93cecbbe14f936d1b4bace9bfcf`  
		Last Modified: Wed, 28 Jan 2026 02:23:46 GMT  
		Size: 49.2 KB (49244 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; 386

```console
$ docker pull php@sha256:56152364243f0badf3722e82a42b3fccfaefb296a89992503fff98e8e8487c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38664350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecc3bca9252bfe9b9c9394c8ca22da19ec549a3721e851f3096db3b6881f28`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:17:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:17:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:17:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:17:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:17:03 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:17:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:17:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:20:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:20:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:20:29 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:20:29 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:20:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:20:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:20:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b04c2e380bda02ab92448fd00e467e5ba6a6167938a0058d9e7f7f1844b8a9`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 3.6 MB (3629354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b29a694be1970887018ee3aeebdd1f346bf251d0689c9df25d67051aad3ac3`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4bc5a2742fd893d7ca490504d72f68126e0b2b4c3786925e99e9f3678b5be1`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02293de56101e4e2c44250b387c0880a6917b9d474b8e83157c21b58ecfa6070`  
		Last Modified: Wed, 28 Jan 2026 02:20:37 GMT  
		Size: 14.4 MB (14355556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714495b3bde47aba99b4cbf555dea5f54609a57ac78908f6ebeac73c991857a`  
		Last Modified: Wed, 28 Jan 2026 02:20:37 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59207eb277dd20fad6342dcf23a2dd59cf59c4254c24f36f2a1282cc834826a3`  
		Last Modified: Wed, 28 Jan 2026 02:20:38 GMT  
		Size: 17.0 MB (16955565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8c97b7e833eaab4be094d96df6daab667fcb322ff726d9e133e85c2c1dedd1`  
		Last Modified: Wed, 28 Jan 2026 02:20:37 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bfa3c4eed294ff99c8159758aef10b981bab60d2ab8995b8bb475693c70870`  
		Last Modified: Wed, 28 Jan 2026 02:20:38 GMT  
		Size: 23.5 KB (23503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5885bfd0bd5d2d09a82d73bd275a5dfcc844d6469f1ff342737718084975ef8`  
		Last Modified: Wed, 28 Jan 2026 02:20:38 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:d3b9a1014b893bd3255fb07d8199b8fe3c7eb17c55f4e2592a0c13c6bde6ae90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 KB (331011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04172ef653920eada6b3bdc57d9c652e14068cb065a16a93d6b227b0b644b78d`

```dockerfile
```

-	Layers:
	-	`sha256:7c7d51b417e33c241e020c74a33d902475b372f665872ecd2af823fe8a1a11fc`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 282.1 KB (282073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:257937e9a22f0b555008c1769e439fb4e2d93626b61d0adbb4f2ca8ed7d0d86b`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 48.9 KB (48938 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; ppc64le

```console
$ docker pull php@sha256:59099007b189904becbbaffc3493ced0e25ecbdc5f1d2826e1f8d6fd2283812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa8db83dfde21af9fa753187095c03ae3f330b6d37fa4b85912e15cb71a1910`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:38:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:39:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:39:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:43:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:43:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:43:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:43:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:43:37 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:43:37 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:43:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:43:37 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:43:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7dd774a9daa9cc5f74d16d61155e614ceedece1fd19c05044ba6ace37dd4c6`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a002cadcf53d322e552c6a02f973915d8017427dfda71de122592386df6743`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b05b21b742c21780f39ad80c5babf4b1d13a4f41a2726c561bfb0fcc954e0`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0240c66f2f649263f65cb23040d6f3e01923bdaa3db18a3b086e8299546b3`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 14.4 MB (14355584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4c1916d8ab04d5c7c614bc2f69c44eab90c83dc656fc76685e7d66c35c7643`  
		Last Modified: Wed, 28 Jan 2026 02:43:15 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0547a7133de0304ca6a07c58b21880785621db75c5b0e1fa934608c373e3c221`  
		Last Modified: Wed, 28 Jan 2026 02:43:53 GMT  
		Size: 16.7 MB (16729418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dea240310066542b4ea8ee2b02ed4966152e2fb6dbb0aaf59e86e4b3982731`  
		Last Modified: Wed, 28 Jan 2026 02:43:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb04dbd3ff07fe59f20057d2b8a9b83020f981b2a42764c844f7fc6d6dbfd857`  
		Last Modified: Wed, 28 Jan 2026 02:43:52 GMT  
		Size: 23.3 KB (23331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c50dee073c9b482bc207f276d5ebfdfb75ac03abb4f843715b8229371f95a7c`  
		Last Modified: Wed, 28 Jan 2026 02:43:52 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:ec7f94f66efac32ac6b2cde4969d6bb58655b837ed795a2308fd355ab4477c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 KB (326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032e60c894a0661e75277e0b4bebed21678259cd90b9568090af6666686d5bc6`

```dockerfile
```

-	Layers:
	-	`sha256:5fda7f7e611128168e0bd097bcd9c46d00d7d284b9bc361d4742113d149f0b4b`  
		Last Modified: Wed, 28 Jan 2026 02:43:52 GMT  
		Size: 278.5 KB (278535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb788dae02e517c49663edfd7cd7f43a9ae25e58b6b7142624d6e1a43d5448d`  
		Last Modified: Wed, 28 Jan 2026 02:43:52 GMT  
		Size: 48.1 KB (48130 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; riscv64

```console
$ docker pull php@sha256:d7f1c046856e4128b5837cee6cf55ea5804536c9c73a8075ebc5f9697b7fa494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37281625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e600dd9a27a643aaf69c2e0eb21acd4fd0757fd257a2a1d7486302fa6cf73`
-	Entrypoint: `["docker-php-entrypoint"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.5.2
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Sat, 17 Jan 2026 20:04:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 Jan 2026 20:04:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 11:23:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 20 Jan 2026 11:23:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 11:23:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 20 Jan 2026 11:23:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 20 Jan 2026 11:23:12 GMT
WORKDIR /var/www/html
# Tue, 20 Jan 2026 11:23:12 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 20 Jan 2026 11:23:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 20 Jan 2026 11:23:12 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 20 Jan 2026 11:23:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:00 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:09:59 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:09:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42e7691a5ac89a26cf121121e54d4615dbd5be673123734769af72847ab8beb`  
		Last Modified: Sat, 17 Jan 2026 21:45:03 GMT  
		Size: 14.4 MB (14355583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8009a96b3fbcbb0a3cb6dda1b075a1caafb2f130fc19967f68fbab4a423ef7`  
		Last Modified: Sat, 17 Jan 2026 21:44:58 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c966e7e3bbe6c537ef54783093e8af041f8b7620da592d72d0c0cd2f3922a4`  
		Last Modified: Tue, 20 Jan 2026 11:24:09 GMT  
		Size: 15.6 MB (15565125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0562e45545ab60bdbbce8858a9fc829b32a50029406afa168b0b00852278e2d`  
		Last Modified: Tue, 20 Jan 2026 11:24:07 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28071bc3bd9a663aa546fab1e1fbeeac17289f225417fa2848c6f8d02b803671`  
		Last Modified: Tue, 20 Jan 2026 11:24:07 GMT  
		Size: 23.4 KB (23374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffea984aaa3a2bbc3aa910ba860a5af3e7dc134fff575562356d38cd2f7b31ed`  
		Last Modified: Tue, 20 Jan 2026 11:24:07 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:fd2f257f89de228a3a2f33c81af39502369b8816124aaf1c3a8762a638188483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 KB (327612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299f0ad5090dd6a1b60c69fd9e881fb1c39cb70a64ed3c0200c7ac30d60d4a88`

```dockerfile
```

-	Layers:
	-	`sha256:f18994303b3811612d4a449eaced3add1b3b9f972a62c6b44a17042c5fb4a399`  
		Last Modified: Tue, 20 Jan 2026 11:24:07 GMT  
		Size: 278.5 KB (278531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c70137cff6e3f3c6ad6ec74c05b8d187d8ff44467a5d13b0dc501f112f1ad8`  
		Last Modified: Tue, 20 Jan 2026 11:24:07 GMT  
		Size: 49.1 KB (49081 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.23` - linux; s390x

```console
$ docker pull php@sha256:0079b8c5108ca0d0ad6f97f207b241eb9b6847a7dc97b3219533fcba52f0c4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37808049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ea305903f89df1a13b25a879aacbb956d9500f2aea3fa51b4011c33c0622d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:22:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:22:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:22:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:22:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:22:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:27:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:27:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:27:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:27:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:27:44 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:27:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:27:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:27:44 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:27:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cf22f299f5bcaf74fad4af8e728f6e6624c9a610c22221efa870a8765d30d4`  
		Last Modified: Wed, 28 Jan 2026 02:27:03 GMT  
		Size: 3.8 MB (3795102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0814653fdf7094e8d4c40445da0f7faef7d6e1c3470e2400b2c3e23b34824e75`  
		Last Modified: Wed, 28 Jan 2026 02:27:03 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88a5ab07486c1edbe76d7f40fb614509f04ca091ab87b96dc64e90aff8b8e2`  
		Last Modified: Wed, 28 Jan 2026 02:27:03 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ba033170c5409f940ba1a68652271697f3d9baef9ec81cb17989bea3b28ddd`  
		Last Modified: Wed, 28 Jan 2026 02:27:04 GMT  
		Size: 14.4 MB (14355562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f44bd2698f8aeb10d3ff119826a2c0f11cbe305ca4a29e16252aa2a4e845f`  
		Last Modified: Wed, 28 Jan 2026 02:27:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158fffe342540a36a70a24559784cf6abb8444757442a148eed99c0627f8c4b4`  
		Last Modified: Wed, 28 Jan 2026 02:27:55 GMT  
		Size: 15.9 MB (15895345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035576996bd74decc64cb25fbff12491c01c85aeb14a7cf6ad9c08b5c4e25de`  
		Last Modified: Wed, 28 Jan 2026 02:27:55 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76033bbfd68da8c3457ca2a9abe4e218ade79297bcf47f28cf6ce441e5b81239`  
		Last Modified: Wed, 28 Jan 2026 02:27:55 GMT  
		Size: 23.3 KB (23327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dca5d9cef37e8ac5eaf432bf6f7b90df7d82016d4f0b6c5fc7f194cb4b87c7`  
		Last Modified: Wed, 28 Jan 2026 02:27:55 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:39e183f096090e1ede4b5c90f5672a245a4d28e9a68ccc597ca2903f1744f7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 KB (326528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5611944b821335b98a548ab446996a75077bba0d4ab9ff80330a62caf9cb0a99`

```dockerfile
```

-	Layers:
	-	`sha256:cef3382a33d7a540f83da5405655cf11ae42c9d03e48e16689016af1a23ffdf0`  
		Last Modified: Wed, 28 Jan 2026 02:27:55 GMT  
		Size: 278.5 KB (278477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168f5b2af0cb9505ceb073869d46fce1d23efe8f75707969f3c83fedaf292fee`  
		Last Modified: Wed, 28 Jan 2026 02:27:55 GMT  
		Size: 48.1 KB (48051 bytes)  
		MIME: application/vnd.in-toto+json
