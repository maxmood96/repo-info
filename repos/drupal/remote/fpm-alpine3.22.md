## `drupal:fpm-alpine3.22`

```console
$ docker pull drupal@sha256:5c1e9f50cb5145c1ee4595a371a42fa21e62c26b3b06512451b6397fa4568462
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

### `drupal:fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:bc648cfce20fa3417e4fc9bc20e80a5e57376d5245733fc8dfaa82ad2c2dfb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59712542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f708c1872bcdf6828a5d50095408e97334f327336dc93b610d7c0744c2a1c91`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:15:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:15:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:15:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:15:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_VERSION=8.4.20
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 17 Apr 2026 00:15:42 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 17 Apr 2026 00:15:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Apr 2026 00:15:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:18:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Apr 2026 00:18:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:18:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 17 Apr 2026 00:18:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Apr 2026 00:18:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2026 00:18:50 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 00:18:50 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Apr 2026 00:18:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2026 00:18:50 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Apr 2026 00:18:50 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 01:14:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 01:14:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:09 GMT
ENV DRUPAL_VERSION=11.3.7
# Fri, 17 Apr 2026 01:14:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 17 Apr 2026 01:14:09 GMT
WORKDIR /opt/drupal
# Fri, 17 Apr 2026 01:14:15 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c59b4ec83e5d135fdad3b49c156e918fda8337055269d1f2313f4dfa1078a`  
		Last Modified: Fri, 17 Apr 2026 00:18:57 GMT  
		Size: 3.5 MB (3463495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e4c5788c6c6f51593840653a776fad8b01ecf9768305e272e6737979aca49b`  
		Last Modified: Fri, 17 Apr 2026 00:18:57 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e55fd1837b554d54300fddeba77d6d1f4f14a84b22a6ff04eb7adfaf4bcddf`  
		Last Modified: Fri, 17 Apr 2026 00:18:57 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66574c3597983a286d938a6e0cab51e18425bf9a795f87856198c1e5f458086`  
		Last Modified: Fri, 17 Apr 2026 00:18:57 GMT  
		Size: 13.7 MB (13707451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14da3cb47a2da72f3d14aa3d7f27bdd7b309f475cd0e8d4e81ea12523be714ab`  
		Last Modified: Fri, 17 Apr 2026 00:18:58 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79fb877cd89c8cb21593cc270b7e05b36707c14aa5eb0100bbcf4445b36967`  
		Last Modified: Fri, 17 Apr 2026 00:18:58 GMT  
		Size: 15.1 MB (15060279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336b3e25b323473c1f6806cf29b5e5fe9517c197260793e2ed2a575ee14c919`  
		Last Modified: Fri, 17 Apr 2026 00:18:58 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5100df7671d1fb69480277dd64e45b7cee752859cc691796c8d695e8fea1e97e`  
		Last Modified: Fri, 17 Apr 2026 00:18:59 GMT  
		Size: 20.0 KB (20036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a047cebcf5f9d9640bb302522b13e5647672a7b393c11978118374ab62ede563`  
		Last Modified: Fri, 17 Apr 2026 00:18:59 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a90d6f6fc88098a6ff4703e6408e61f4ea079d84de7b87316ae4a7b569e2ea`  
		Last Modified: Fri, 17 Apr 2026 00:18:59 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246ccc9b425ee852c3da2b67846e41e7fca3f8b0a9e737e2b84d14c3844be249`  
		Last Modified: Fri, 17 Apr 2026 01:14:27 GMT  
		Size: 1.5 MB (1493954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c90977d582b4748bbbfe3922f67c049800c46bb8d6a0fce82ec4a2289f8e466`  
		Last Modified: Fri, 17 Apr 2026 01:14:27 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261ced15c49e0ad33683cd9083151ba4d1068dbbac2978aebb293dbca41aa71`  
		Last Modified: Fri, 17 Apr 2026 01:14:27 GMT  
		Size: 790.8 KB (790764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccda6a0d6b71bb4022934debc9feaaa24487929e169f8dd0fc71c34b18195d85`  
		Last Modified: Fri, 17 Apr 2026 01:14:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228262855e737e63a333e459242839f9fbe9e0d6ea8e78718203fc98f15ff72b`  
		Last Modified: Fri, 17 Apr 2026 01:14:28 GMT  
		Size: 21.3 MB (21334533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:638f4acc596de981a4cd54279dc7cd4ba622e03c3652956b7f9b9058660a2c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.1 KB (411131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8df200f1f082ac8065ef7ce1bb1c3281a5c8aba77faf8c63f2e2bf6f4ac3280`

```dockerfile
```

-	Layers:
	-	`sha256:76767963b041c1741a95264e08d40e5ec82f9bc236a58ebf861be6e94951b3b7`  
		Last Modified: Fri, 17 Apr 2026 01:14:27 GMT  
		Size: 376.6 KB (376631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b5507779cd39b518b4fb3d8cc5314abc6958495c6836c5632122072adfd038`  
		Last Modified: Fri, 17 Apr 2026 01:14:26 GMT  
		Size: 34.5 KB (34500 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:f97715ad1588cd496fe8b25a10b5ab5828a910dba0f2de243bae64fcdd896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57707685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e4eb492626bfa15d115d9dae06ad10dc0cb5bdefd6e9963bff3e97a3e86699`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:16:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:16:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:16:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:16:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_VERSION=8.4.20
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 17 Apr 2026 00:16:15 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 17 Apr 2026 00:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Apr 2026 00:16:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:19:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Apr 2026 00:19:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:19:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 17 Apr 2026 00:19:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Apr 2026 00:19:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2026 00:19:15 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 00:19:15 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Apr 2026 00:19:15 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2026 00:19:15 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Apr 2026 00:19:15 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 01:13:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:13:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 01:13:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:13:34 GMT
ENV DRUPAL_VERSION=11.3.7
# Fri, 17 Apr 2026 01:13:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 17 Apr 2026 01:13:34 GMT
WORKDIR /opt/drupal
# Fri, 17 Apr 2026 01:13:43 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 17 Apr 2026 01:13:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e671b18b8aaed26044159f819edbf4e1393657d1ff7b753ba29b6659146f3d6d`  
		Last Modified: Fri, 17 Apr 2026 00:19:21 GMT  
		Size: 3.4 MB (3427477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f047bc805e3cee52adcbd04275a339fae5f8cb9ea566c43ced1e84f909c0b21`  
		Last Modified: Fri, 17 Apr 2026 00:19:20 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6dcabd6735077f648bd3e445f4280185aa720abcece25f649b0b3e1a811228`  
		Last Modified: Fri, 17 Apr 2026 00:19:20 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ecd477992d993d136412bcb968304d010379302d96ab50d67790dbcf254c4a`  
		Last Modified: Fri, 17 Apr 2026 00:19:21 GMT  
		Size: 13.7 MB (13707462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e1c89a6559bf47d2765e7819438723ffd480ac48f8b0d46ac5d7ad3723c40`  
		Last Modified: Fri, 17 Apr 2026 00:19:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3834e83562ab58f2adb4309f59c794a62525ff3cfa20b84f4b05d0fd8bd0db`  
		Last Modified: Fri, 17 Apr 2026 00:19:22 GMT  
		Size: 13.5 MB (13548799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdc3ed55d93f500a1ddf0dd477f81d2f111839635492b8598f4d9087c32db63`  
		Last Modified: Fri, 17 Apr 2026 00:19:22 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04929411d7ac0bb87d4e9c1e3d700760b9929a72225db1daea57cc9b96f03f`  
		Last Modified: Fri, 17 Apr 2026 00:19:22 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0451b205b2b14f468703ff257ac2de4514877137f82c32e05096926b2caeebbf`  
		Last Modified: Fri, 17 Apr 2026 00:19:22 GMT  
		Size: 19.8 KB (19836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcefd7dc5436978e485beed2abc3a6b41e68590be17d4be5a5cfe59905b7e72`  
		Last Modified: Fri, 17 Apr 2026 00:19:23 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be538f5fb46616e51bb4a241663d4d8ec8351f8719d9805ad28d155ccdeb48d`  
		Last Modified: Fri, 17 Apr 2026 01:13:51 GMT  
		Size: 1.3 MB (1336521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08314b0111656a53db9acfdaa462442628020e41c3d9947a7932febec460c73d`  
		Last Modified: Fri, 17 Apr 2026 01:13:51 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab987a67158fe2d2a5999b6f54563a73bab2a40d50870be7e64f17cc03938fb`  
		Last Modified: Fri, 17 Apr 2026 01:13:51 GMT  
		Size: 790.8 KB (790767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb11f0efe879d2754253e818342d344a9923348ecaa804e9921078e5d959b51`  
		Last Modified: Fri, 17 Apr 2026 01:13:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d850ddfa019c7764b6305d7f5104c6874c4df05df7a5ee17eb0ddd3c8ca4d`  
		Last Modified: Fri, 17 Apr 2026 01:13:53 GMT  
		Size: 21.3 MB (21335785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:ca02c3962bd65f633a73b885aeca28a5f038eec6b07f633edc12092826dcda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 KB (34445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aca887996e9c333ad17ecf02939be7c9dcf22c04e0f5af19d4198fe05d5c5d`

```dockerfile
```

-	Layers:
	-	`sha256:92bebfff295e4b2a9b11fc23508b385123245f426d87122a022a93d161eac0a2`  
		Last Modified: Fri, 17 Apr 2026 01:13:51 GMT  
		Size: 34.4 KB (34445 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:2628bfabedfd9e5fd85913a4b48f7bba56fb4bd784207ced32987e2e26861991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56394968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff46e60030a835f3b7bcb2610b1601fd8fb401d560a76549d948f6c258cc0c6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:18:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:18:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:18:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:18:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_VERSION=8.4.20
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 17 Apr 2026 00:18:49 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 17 Apr 2026 00:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Apr 2026 00:18:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:21:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Apr 2026 00:21:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:21:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 17 Apr 2026 00:21:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Apr 2026 00:21:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2026 00:21:51 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 00:21:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Apr 2026 00:21:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2026 00:21:51 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Apr 2026 00:21:51 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 01:15:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:15:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 01:15:05 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:15:05 GMT
ENV DRUPAL_VERSION=11.3.7
# Fri, 17 Apr 2026 01:15:05 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 17 Apr 2026 01:15:05 GMT
WORKDIR /opt/drupal
# Fri, 17 Apr 2026 01:15:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 17 Apr 2026 01:15:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ee8898359fa2d5a9e150d40980d5cfd9273a2d286c3fe347e9e7170d0dd70`  
		Last Modified: Fri, 17 Apr 2026 00:21:57 GMT  
		Size: 3.2 MB (3244411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ad3744acecb18b3dbf2c39eaaf3b0065c4feae0edf3d6ac2b51b51cd912c49`  
		Last Modified: Fri, 17 Apr 2026 00:21:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c104e163da7cbff8b2c8636cc2cf220a2f9c93e6408b81a1b0d964d9b2c48e`  
		Last Modified: Fri, 17 Apr 2026 00:21:57 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce0e917f6274fc7e49a49ea7aa9ccb619ef65444aa19763edea02e4c352091a`  
		Last Modified: Fri, 17 Apr 2026 00:21:57 GMT  
		Size: 13.7 MB (13707420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06f0f84a2d8958293125cb9aadf50e088039ddc6d3aacbf057614b4270c05ad`  
		Last Modified: Fri, 17 Apr 2026 00:21:58 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4a0c290295f5a1f9ae733fed3ea7800100f06396b2b49ec18f7fc6681a227b`  
		Last Modified: Fri, 17 Apr 2026 00:21:59 GMT  
		Size: 12.8 MB (12803250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4672aa559139ff3e9ea01553491a51fb702b2aac2586adfde2c726b5f734e1b`  
		Last Modified: Fri, 17 Apr 2026 00:21:59 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92d32795b080ae339518115f8440b925e222436a3ed503bce2f2f5c1e00c8f7`  
		Last Modified: Fri, 17 Apr 2026 00:21:59 GMT  
		Size: 19.8 KB (19821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bda83042a5fc3e8bceb5ca3a6d91d9ab450ff70473c7321ada0610cbb0eb`  
		Last Modified: Fri, 17 Apr 2026 00:22:00 GMT  
		Size: 19.8 KB (19817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7bb0cdfbac8c23ae1b520d190a67dd82fdffc745043133767400ba367e3c56`  
		Last Modified: Fri, 17 Apr 2026 00:22:00 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aaf851168e97f4aa83dbf906a2486a337af665507a1cb499848a23671925ce`  
		Last Modified: Fri, 17 Apr 2026 01:15:24 GMT  
		Size: 1.2 MB (1234293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b4e62a82ea7be5a4baa28a4d5d474242f27a5108ed7c28ce70df181179c9d1`  
		Last Modified: Fri, 17 Apr 2026 01:15:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc15da6e49f2487b78e28f8bae59f4b7e5fa2524079407c32f52edc7e7728d2`  
		Last Modified: Fri, 17 Apr 2026 01:15:24 GMT  
		Size: 790.8 KB (790765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1e49a084b1b8a01d92202ae36e75c71c1cd50cb11fff09978de027ed128272`  
		Last Modified: Fri, 17 Apr 2026 01:15:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89592ab7a3e282138b93168f35af0519fbaa2b56a2fd7737c211f4a09f0b7c3`  
		Last Modified: Fri, 17 Apr 2026 01:15:26 GMT  
		Size: 21.3 MB (21335557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:a2b1b6482bdbffc19ea8762651587adb6c097830091f31705149661922555f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 KB (408369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044ede98c22abd079df925dcce66bdbcdf3b8ff1226b5621a266e61bcbf55258`

```dockerfile
```

-	Layers:
	-	`sha256:4def2206884bf492f215d123b11c89c4f8ed89adbe8588eeadec85bee3696486`  
		Last Modified: Fri, 17 Apr 2026 01:15:24 GMT  
		Size: 373.7 KB (373709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089b98dd8c94133d7b1f6ce8a7474bfc3d6b8fe2e84236ec3906fcda0b185a2c`  
		Last Modified: Fri, 17 Apr 2026 01:15:24 GMT  
		Size: 34.7 KB (34660 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5f87eb0334f06ad523b0155fd982de3bc4f24d18f25ecadaa83505b39d5a93fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59668410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6630725c6afe3f39817479a6f4b069229eb547131c0edd3502ecb404c12ac0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:15:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:15:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:15:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:15:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_VERSION=8.4.20
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 17 Apr 2026 00:15:59 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 17 Apr 2026 00:16:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Apr 2026 00:16:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 17 Apr 2026 00:19:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Apr 2026 00:19:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2026 00:19:43 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 00:19:43 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Apr 2026 00:19:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2026 00:19:43 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Apr 2026 00:19:43 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 01:35:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:35:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 01:35:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:35:38 GMT
ENV DRUPAL_VERSION=11.3.7
# Fri, 17 Apr 2026 01:35:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 17 Apr 2026 01:35:38 GMT
WORKDIR /opt/drupal
# Fri, 17 Apr 2026 01:35:45 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 17 Apr 2026 01:35:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befa02ffb4f258b72841a36824ffb22dcff3f3276152d5e27e88b54b029a83cf`  
		Last Modified: Fri, 17 Apr 2026 00:19:41 GMT  
		Size: 3.5 MB (3466779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3f191ebd3d020eba37412a2224d06f578c439e3900f39b255d8994d0c8570a`  
		Last Modified: Fri, 17 Apr 2026 00:19:50 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0242da4b9277b1a0a92b1a2c3a394978db280d3a10e751c6476f358d00993653`  
		Last Modified: Fri, 17 Apr 2026 00:19:50 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dc6c5ab1239f8c0ee0ded3d6024301f792c93b1d80554235a72bc2f42ce882`  
		Last Modified: Fri, 17 Apr 2026 00:19:51 GMT  
		Size: 13.7 MB (13707457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdf5c7115bb78ba000e6151ecdc84551538e6a39bb5c34d9f855706fce24282`  
		Last Modified: Fri, 17 Apr 2026 00:19:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec754da436b4ac8f3636bd3c062dede7485d71261e333b3eea6d23ed6187bef`  
		Last Modified: Fri, 17 Apr 2026 00:19:52 GMT  
		Size: 14.7 MB (14691127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb995bfbae9fcc0442b91f37d70335ad5cadbe8a14a353fd458e266d8d7d6f6`  
		Last Modified: Fri, 17 Apr 2026 00:19:51 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2c89df8fc1134988da31e66e1ffd6a1d638dde2f6d5c4d39cd5b84e9790637`  
		Last Modified: Fri, 17 Apr 2026 00:19:52 GMT  
		Size: 19.8 KB (19836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1635dacd8dd947968fa95c5fa7ad764ff6ffb24705d7a51090a96f5b0b0b2`  
		Last Modified: Fri, 17 Apr 2026 00:19:52 GMT  
		Size: 19.8 KB (19830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eede29d8ed364120da5cdea63f6a4e9bfa1f8b70ff11db9b021b811aa32c77`  
		Last Modified: Fri, 17 Apr 2026 00:19:53 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24d4722014fe404153f5e445cb4d150bd53bc1823bd4516cf2f082b0c3ec8d0`  
		Last Modified: Fri, 17 Apr 2026 01:35:58 GMT  
		Size: 1.5 MB (1481291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dbc746d2b1e70febcf2abcb2f1bd6f2af5932a25861108ebd2424382942ffa`  
		Last Modified: Fri, 17 Apr 2026 01:35:58 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e4c6ff7965238be485674b297975aa15640dd215d77fc3025e4f4ece659753`  
		Last Modified: Fri, 17 Apr 2026 01:35:58 GMT  
		Size: 790.8 KB (790769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91380704c046f8b47420eb5f836e9a24fc166501d645ea24ff08c97019ea231e`  
		Last Modified: Fri, 17 Apr 2026 01:35:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb372b332a5e50971ce7aa29bfe477648b38e3f5a58da13c00e9a6d0f70f57`  
		Last Modified: Fri, 17 Apr 2026 01:36:00 GMT  
		Size: 21.3 MB (21335618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:6bfab25cdfdb1b221c3726be5fe1d7930a9f4f516f7590e65634edfa4b0e399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.5 KB (408453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c88b9645a2e4c41026c66edfc9273faa82909942b288d19ae26345b2fa1ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:77e934d89367302cdb0be79521a351c8e4acf713d9a5bbfa8ae3be72b6a85540`  
		Last Modified: Fri, 17 Apr 2026 01:35:58 GMT  
		Size: 373.7 KB (373745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d7fd48d42b22624a49e0b33239b836969533aaea4e00a86042842f29bee251`  
		Last Modified: Fri, 17 Apr 2026 01:35:58 GMT  
		Size: 34.7 KB (34708 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:cc5bd4fe995c33bcd38beea054cc83bb45910a85ad1771e30e30fd627eb49a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63245561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018770e85360672acc7891f3c4687b297bf5ee9777c5e1514eb17b8eed90a694`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:20:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:20:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:20:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:20:56 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_VERSION=8.4.20
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 00:21:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:21:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:24:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:24:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:24:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 00:24:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:24:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:24:18 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 00:24:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 00:24:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 00:24:18 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 00:24:18 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2026 23:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 16 Apr 2026 23:38:52 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 23:38:52 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 23:38:52 GMT
ENV DRUPAL_VERSION=11.3.7
# Thu, 16 Apr 2026 23:38:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 16 Apr 2026 23:38:52 GMT
WORKDIR /opt/drupal
# Thu, 16 Apr 2026 23:38:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 16 Apr 2026 23:38:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954b0df7f78d81c0899e129e67a55b792ae63a3ed950331098028b7dd9ef481f`  
		Last Modified: Fri, 10 Apr 2026 00:24:26 GMT  
		Size: 5.8 MB (5807148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f767e40180f52a8e1cca5fcb1d20fd867a24e722a09b4cca10a5b7fe2d2cc86`  
		Last Modified: Fri, 10 Apr 2026 00:24:25 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4703ed0c9c8a3c51706e8b4a28803202daa2e8357851263f8f45bf7567979`  
		Last Modified: Fri, 10 Apr 2026 00:24:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bf6f2c2e26bbf7b348ebdd36c833f4c6145bd7d8eacc0ab27e88bffc8bb0e4`  
		Last Modified: Fri, 10 Apr 2026 00:24:26 GMT  
		Size: 13.7 MB (13707495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14228cf001547dfb68739a1844f414a7bcdb83531aab5d089c5068d1db4f917a`  
		Last Modified: Fri, 10 Apr 2026 00:24:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7276392de2bdb3957871a41094185b88575f4b77a68c2d25ce40e854d6dc0313`  
		Last Modified: Fri, 10 Apr 2026 00:24:27 GMT  
		Size: 15.9 MB (15876397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f7293aab1bf6afe65b2af7f5b85a0ad30f6d3db2d4cd7c4ff038ba72a4749`  
		Last Modified: Fri, 10 Apr 2026 00:24:27 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd735542fe2233c2bbd6698acaf7b45df842418b6e57ae9f365993b4ab288f`  
		Last Modified: Fri, 10 Apr 2026 00:24:27 GMT  
		Size: 20.1 KB (20094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a2476df8038bef366250ce90f6b7b58311b9b3dcdf1d032f4a574ee3fa10a9`  
		Last Modified: Fri, 10 Apr 2026 00:24:28 GMT  
		Size: 20.1 KB (20096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb98ac7534f9de8fd7a9a8f2458f8ffda4a0509930561f15132a351b3a973c1c`  
		Last Modified: Fri, 10 Apr 2026 00:24:28 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80624dc96196ae2a696aab64aea9b1d5f6979b2a1e88e76fdfd9cd3b4f5cf1df`  
		Last Modified: Thu, 16 Apr 2026 23:39:10 GMT  
		Size: 2.1 MB (2053501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ae8c4e146a85c9adce48ae875ac4c8f55036e655bfe83080df709ac9f5334d`  
		Last Modified: Thu, 16 Apr 2026 23:39:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe312ed57e61b053ad9079c491f15abf8102245ca56a9340ab6698511b5f6ba`  
		Last Modified: Thu, 16 Apr 2026 23:39:10 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9a35738996fbc9fa8b58b37d1b09f03e8c60521e5a982376ed7e03120a9995`  
		Last Modified: Thu, 16 Apr 2026 23:39:10 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aef33c23276456658858bb0e6043ab525aea898698167bba518af874af5d5eb`  
		Last Modified: Thu, 16 Apr 2026 23:39:12 GMT  
		Size: 21.3 MB (21335524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:bb581e5f7cf0131d4b8e72dd1e3c2a3553005c66d7819f3d018a2709ec49f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.7 KB (412733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3580dc979dd8a86f7538e652c4e1ea4500f42d5a7d60056354353ba7de2d89f`

```dockerfile
```

-	Layers:
	-	`sha256:424c94d7f0823f1f5643237e0379bad2cbd599dc6a20c6b8f8a7210dad41134a`  
		Last Modified: Thu, 16 Apr 2026 23:39:10 GMT  
		Size: 378.3 KB (378296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81676b7981d18a83b05346406275c0bc4f6c6e57e3219181893e815b13b1f62b`  
		Last Modified: Thu, 16 Apr 2026 23:39:10 GMT  
		Size: 34.4 KB (34437 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:102bf466b08c376ab31a4932acc6869719992458e82e1a39620386d41b913468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60376016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d36e52af08e780a1f9c437910250c2d5153f48fed1bf9e272f4642d1b96b74`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:19:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:19:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_VERSION=8.4.20
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 17 Apr 2026 00:26:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Apr 2026 00:26:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:38:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Apr 2026 00:38:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:38:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 17 Apr 2026 00:38:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Apr 2026 00:38:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2026 00:38:09 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 00:38:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Apr 2026 00:38:11 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2026 00:38:11 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Apr 2026 00:38:11 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 02:10:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 02:10:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 02:10:14 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 02:10:15 GMT
ENV DRUPAL_VERSION=11.3.7
# Fri, 17 Apr 2026 02:10:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 17 Apr 2026 02:10:15 GMT
WORKDIR /opt/drupal
# Fri, 17 Apr 2026 02:10:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 17 Apr 2026 02:10:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b158ada90b6cc8f44737ff5d95bedaf7f63979acc7eb3452859f5d0ace79a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:56 GMT  
		Size: 3.6 MB (3615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99d415a1788bb58d298132317074efb0a3a7801f8a3fed0809ed39f6869175`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb866ab296180559ca8a3add579c6854d381da1068c287f30bf1ddcaa1eaf8`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3c66f54cbbd36ddf3b6880a800d0333865cab3ef7094eca451d02fc0994bf1`  
		Last Modified: Fri, 17 Apr 2026 00:32:25 GMT  
		Size: 13.7 MB (13707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303251c63a4e9b104df608a839efe069bf3585eac6fab83931d45b5554e8476f`  
		Last Modified: Fri, 17 Apr 2026 00:32:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9b8d3473d3e3ba177615a1506a2345ba2e634abdaada7e33ba8a3a8473c5c6`  
		Last Modified: Fri, 17 Apr 2026 00:38:37 GMT  
		Size: 15.5 MB (15520905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0478402f0a89ba9812da3ec3fab9218537d54aeceb7c46014150b681b057a086`  
		Last Modified: Fri, 17 Apr 2026 00:38:36 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a527750ed82931917c626d7d1584ddf527767f80cd39465cedd38c20594dbae5`  
		Last Modified: Fri, 17 Apr 2026 00:38:36 GMT  
		Size: 19.8 KB (19844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac81201dea99871d8955a238901d3d6db6edc7a1bf49441f079ffbecf0db9512`  
		Last Modified: Fri, 17 Apr 2026 00:38:36 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166d3c3ae0225ae0e8a18a4725985b8e8a669529ee9fe0382286d41c1353f334`  
		Last Modified: Fri, 17 Apr 2026 00:38:38 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b82d6765edb9c86fd5fd67274a496a43671ea76ec714466977bbeb6e9e1461`  
		Last Modified: Fri, 17 Apr 2026 02:11:10 GMT  
		Size: 1.6 MB (1615925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfca10edef16c25b6408e96375b115b67acb17381386ce0b36202cb567ca6ed`  
		Last Modified: Fri, 17 Apr 2026 02:11:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a3514ee5e30318a3448500dd550cdea50114cd55dafb9808a9e3535ad2cdab`  
		Last Modified: Fri, 17 Apr 2026 02:11:10 GMT  
		Size: 790.8 KB (790764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a686e909ea1f7b3926fa47ac7b27bb67b03364dee77984d116fe6b66df52f6`  
		Last Modified: Fri, 17 Apr 2026 02:11:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc646f88670d91bcc81c3c15c6a2a05b3499fef3a09f85db937bf7372c99acb`  
		Last Modified: Fri, 17 Apr 2026 02:11:11 GMT  
		Size: 21.3 MB (21335718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:0b7757d16d5e5f7b06217737bd03e478fa01ab00334d0aa57afe6cd8d1b48859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a118ce5f99fa6b29785cee5f044ec8c195e33edf7fbdc244662bed4f61851b3`

```dockerfile
```

-	Layers:
	-	`sha256:fb9f217485bc5ce7661b327393382f9306d19732dcbe9f1b4b968ff9718d6a18`  
		Last Modified: Fri, 17 Apr 2026 02:11:10 GMT  
		Size: 371.7 KB (371748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d56a0c9e7325a76cc9d03936c5bf111ff916d62976878c364008631f0e69cb4`  
		Last Modified: Fri, 17 Apr 2026 02:11:09 GMT  
		Size: 34.6 KB (34582 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:3b2dbf0746a2654262ba3ecca37743bb14ae0b5e8f99d87a7fdb1930e6c19a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58868924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22bded78a8d16acd46cbf7025ab9e4d6a2a30091c77f035a19fe8d2bf5d684f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 02:06:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Mar 2026 02:06:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Mar 2026 02:06:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Mar 2026 02:06:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_VERSION=8.4.20
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 22:00:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 22:00:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 23:56:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 23:56:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 23:56:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 23:56:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 23:56:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 23:56:30 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 23:56:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 23:56:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 23:56:30 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 23:56:30 GMT
CMD ["php-fpm"]
# Mon, 13 Apr 2026 00:29:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 13 Apr 2026 00:29:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 19:35:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:35:54 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 19:35:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 19:35:54 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 19:36:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 19:36:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfcec5e28255dc0e86ab83e16a74b5c1c525134a3732aee9e431f8cc84bce27`  
		Last Modified: Fri, 27 Mar 2026 14:21:20 GMT  
		Size: 3.6 MB (3600619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0570e48bf7a46da44ec0d6ff793a75c8aba195204deaed906886b9c3172e561d`  
		Last Modified: Fri, 27 Mar 2026 14:21:19 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a134d0a16baab5e83185028e3a86fe467859436a2b79af399201c18fdf43c`  
		Last Modified: Fri, 27 Mar 2026 14:21:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b7cf352b97fb84db7ca5b713f985cfd204e4becc1bc8f9c165c6e5ac0e274`  
		Last Modified: Fri, 10 Apr 2026 22:58:42 GMT  
		Size: 13.7 MB (13707498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649a9e468e04f5fcf932aab246f649344b6f1258e1f018a781b7bbe18b3ff15b`  
		Last Modified: Fri, 10 Apr 2026 22:58:23 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f339d707f1b77608ac3121500ceed7a8a3c3f8e4891019a7b2d04b3f0156a`  
		Last Modified: Fri, 10 Apr 2026 23:57:23 GMT  
		Size: 14.4 MB (14448743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ebe7b2f076ba147038c760de026260b28ec58247dfb163a3ffba1d1e0e00cd`  
		Last Modified: Fri, 10 Apr 2026 23:57:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19626d1f771abf697116b3212ef52278a2003ca85f12aa7a24c1a0f2a16daf58`  
		Last Modified: Fri, 10 Apr 2026 23:57:21 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cacf30b1b24da54f22f01f173911a88f11cd9d200a4cd199e71a76b27749d1e`  
		Last Modified: Fri, 10 Apr 2026 23:57:21 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2821816d5ea7af43623eb476a5432ec69ca462670a7a34b4a7baeff50552230b`  
		Last Modified: Fri, 10 Apr 2026 23:57:23 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fbbb12a0a1ce8a31b425cc0283e66c39fa5f24d60cbba716bf18eb03f15e01`  
		Last Modified: Mon, 13 Apr 2026 00:32:58 GMT  
		Size: 1.4 MB (1414894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8423c4a7404d3e386b9896b0d498523eacb1dedbfb64289dca0575b1dbc19a2`  
		Last Modified: Mon, 13 Apr 2026 00:32:57 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a7978375ad816f2e6e1f79b52fa941f67a5645bdca63e6662d2e39f4746fc`  
		Last Modified: Tue, 14 Apr 2026 19:39:15 GMT  
		Size: 790.8 KB (790777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12978d47b000dc9fb5487f1ab7248f5cf0ab0a236bf05d53fc66c06b5c75daf`  
		Last Modified: Tue, 14 Apr 2026 19:39:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafb76adbee32b53d10445c03ead54bdd3c627c5f5e7d616eebd5d5a448681e`  
		Last Modified: Tue, 14 Apr 2026 19:39:19 GMT  
		Size: 21.3 MB (21335411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:5c38fcb1155e45726612994c3b5badd84dec4dbb40e3119a42712c5282805585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e80501544f86849b20a7d12f6222cfd2e19f8666c73ec2ad6a9742d7e78829a`

```dockerfile
```

-	Layers:
	-	`sha256:5b7852991da0f0753551ef83e9cddd06778822561c508480d4a4b4ff0f4e65e4`  
		Last Modified: Tue, 14 Apr 2026 19:39:15 GMT  
		Size: 372.4 KB (372431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31154bbb8047188556fe4b5dc5b0f2e19d21982d88b65c85e57d90901819dc4`  
		Last Modified: Tue, 14 Apr 2026 19:39:14 GMT  
		Size: 34.6 KB (34582 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:3e69db670f58f1879abb748f8d5875a5fc52d583711c58430668ba143a01d342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59691000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835cad936abb273149934f4318bcf744011cb1c7f737866aef2526bc71e5dbb5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:14:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:14:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:14:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:14:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_VERSION=8.4.20
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 17 Apr 2026 00:14:14 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 17 Apr 2026 00:14:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Apr 2026 00:14:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:26:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Apr 2026 00:26:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:26:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 17 Apr 2026 00:26:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Apr 2026 00:26:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2026 00:26:05 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 00:26:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Apr 2026 00:26:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2026 00:26:05 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Apr 2026 00:26:05 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 03:01:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 03:01:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 03:01:11 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 03:01:11 GMT
ENV DRUPAL_VERSION=11.3.7
# Fri, 17 Apr 2026 03:01:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 17 Apr 2026 03:01:11 GMT
WORKDIR /opt/drupal
# Fri, 17 Apr 2026 03:01:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 17 Apr 2026 03:01:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836341fc6723b8e48289f89815cd8d74acbc7e38082c18f9e12e5a7c1ebfb672`  
		Last Modified: Fri, 17 Apr 2026 00:20:23 GMT  
		Size: 3.7 MB (3689218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f493ee025f9b0a494fa2c32fce5d60e17890c75d4e0bba25ad9aeee0c8224fb`  
		Last Modified: Fri, 17 Apr 2026 00:20:23 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25043eea15c95dbd8ae2b7639e5e5501e0d1f41ea61e9fa528589b8b001b0501`  
		Last Modified: Fri, 17 Apr 2026 00:20:22 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e043e51287465d8bca6e37422d0e8c22b826fc5c223df59fa9b7533ff3bfe3`  
		Last Modified: Fri, 17 Apr 2026 00:20:29 GMT  
		Size: 13.7 MB (13707477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbfbfad2bbf5449a6ef347be17d6674ecbc3609edf9e0d3bbecd5c72bb27592`  
		Last Modified: Fri, 17 Apr 2026 00:20:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a75bd9d01201870eb278b1a7313d1e928979c66969ac3adeb82a4399539063`  
		Last Modified: Fri, 17 Apr 2026 00:26:16 GMT  
		Size: 14.9 MB (14920543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874980f4c951058192905fd85c22543196743a8c7e8279b2f6ee392c7644ce47`  
		Last Modified: Fri, 17 Apr 2026 00:26:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d3acfd756e64d73b55b208a23d42fd197f116e06bed39a018c61961e5a75ed`  
		Last Modified: Fri, 17 Apr 2026 00:26:16 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be3329f068ca415d14faa23d1d03b56a159decd3166dab89fb743a2023383f`  
		Last Modified: Fri, 17 Apr 2026 00:26:16 GMT  
		Size: 19.8 KB (19836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd0191e754298da5f6e0e6a49f2c4b2ef667d6f4d0ac2f37601ff81c14da613`  
		Last Modified: Fri, 17 Apr 2026 00:26:17 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8a964c315d16ed5ba11a4a6564256b784475c49a8692fcb2318d86c86da24`  
		Last Modified: Fri, 17 Apr 2026 03:01:43 GMT  
		Size: 1.5 MB (1540089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b0fbd92d387c8a5c77c36aebd48d8db597baf7c615e2f84a6a31cb743f2d14`  
		Last Modified: Fri, 17 Apr 2026 03:01:43 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245a7112f0ba8167fb982bf7357c1e67c854a22738fda29ef51ab64dcda59334`  
		Last Modified: Fri, 17 Apr 2026 03:01:43 GMT  
		Size: 790.8 KB (790763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7806a394c4d97605c3ade2ab6bad01024af61ef48d07cbef4272c01cdfb72a`  
		Last Modified: Fri, 17 Apr 2026 03:01:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caa4d1b85bd9bd5c84c31140922cb8d434d513c24943adc7ddb157ff4bfdba4`  
		Last Modified: Fri, 17 Apr 2026 03:01:44 GMT  
		Size: 21.3 MB (21335554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:02355ab500c1d745ba6a8bdcc02611d4f942e53b762654a3493e1191e51b8b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 KB (406190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594c19b7769af64a72220f149b86e454505084dff9bd88ae9134ee29268a75d4`

```dockerfile
```

-	Layers:
	-	`sha256:be63abe79be95f858f4554bdd45802f80ef8ffa8df30418f112376f1860644e6`  
		Last Modified: Fri, 17 Apr 2026 03:01:43 GMT  
		Size: 371.7 KB (371690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa793684e12799557425c346b1827379b33de75aa4f8ba9c20badf9d5607fc85`  
		Last Modified: Fri, 17 Apr 2026 03:01:43 GMT  
		Size: 34.5 KB (34500 bytes)  
		MIME: application/vnd.in-toto+json
