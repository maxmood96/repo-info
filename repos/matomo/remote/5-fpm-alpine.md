## `matomo:5-fpm-alpine`

```console
$ docker pull matomo@sha256:4be11910a4fc5613a76ff0e99dab7235e8e71740457506223b8368f3e6d3a8fa
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

### `matomo:5-fpm-alpine` - linux; amd64

```console
$ docker pull matomo@sha256:322de1daea37d5bdc8b8fedd1763953b1c35bf447496a29c96bb7d02d49f9102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62908296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae316c3edb20f38423d6768f0f934d247d21d44406f7e1d38d1c31d86f3f7bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:54:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:54:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:54:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_VERSION=8.4.22
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 10 Jun 2026 20:54:15 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 10 Jun 2026 20:54:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:54:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:57:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 20:57:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:57:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:57:34 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:57:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:57:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:57:34 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:57:34 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:17:40 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 10 Jun 2026 21:17:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 21:17:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 21:17:40 GMT
ENV MATOMO_VERSION=5.11.0
# Wed, 10 Jun 2026 21:17:45 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:17:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 10 Jun 2026 21:17:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jun 2026 21:17:45 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:17:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 21:17:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e859233b20eb836e65d7399086395f0fecadc1d37cfe42c4522542e01f8c8c0f`  
		Last Modified: Wed, 10 Jun 2026 20:57:41 GMT  
		Size: 6.0 MB (5975983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddfffd06482a6124edc99efe6dbff44c41cd8dff2cdcb78f80a6187826ae64d`  
		Last Modified: Wed, 10 Jun 2026 20:57:40 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba6137bf95b48d43772820198fbd7a9d3b029c750448493e215c09299648b41`  
		Last Modified: Wed, 10 Jun 2026 20:57:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5341088f4dc94ded12ba9b1ab7361a7457a09112dd07a1fbf6d749625618cc`  
		Last Modified: Wed, 10 Jun 2026 20:57:41 GMT  
		Size: 13.8 MB (13755200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb72ebf877823ef4063d0e418b1cdd19c7a495152c4e65dd97006ba7c4093111`  
		Last Modified: Wed, 10 Jun 2026 20:57:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892260cda2db7438ee97332ba4a518d497547ec1d698c09b1b58f1aab7f7ce70`  
		Last Modified: Wed, 10 Jun 2026 20:57:43 GMT  
		Size: 15.4 MB (15368092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514c12da3bd7335d235895324febbd5b2c51cd34ea61b332a0b3b0332a304d36`  
		Last Modified: Wed, 10 Jun 2026 20:57:43 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b83d8c4b0134bc0d4afc0ef8eeb5d42976b66fb8cc61fc478c4b1ecf412a9a`  
		Last Modified: Wed, 10 Jun 2026 20:57:43 GMT  
		Size: 23.3 KB (23251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52e7c0520015bea6160f59fbdac5c7dc620f8c95f6c80d40ecb5d4cf5364af2`  
		Last Modified: Wed, 10 Jun 2026 20:57:43 GMT  
		Size: 23.3 KB (23256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c0450430622fe08cf03425882600e3d06f8fc530ce83a5b340d8443ca4808`  
		Last Modified: Wed, 10 Jun 2026 20:57:44 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b2ca14b31b1300236ac11fde4488fceae6521a89aab241914f9b74de23322`  
		Last Modified: Wed, 10 Jun 2026 21:17:52 GMT  
		Size: 2.8 MB (2829912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f5cc0d092fd15d7315d5ca6a7dfb1b0c78d31acac34357b950cb850c31f727`  
		Last Modified: Wed, 10 Jun 2026 21:17:52 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39e21516b8bca64749bf03aab14d4173aece62e754a27192964ce544f5409b2`  
		Last Modified: Wed, 10 Jun 2026 21:17:52 GMT  
		Size: 21.1 MB (21050980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6237f6bbb6ecaff24ea43ba0535c8ebfde81a40f82599d72bd1104cb03855c`  
		Last Modified: Wed, 10 Jun 2026 21:17:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65be78b399eb896cdbc924519b7236737d4fe39b76b600563dce000bbe91d85a`  
		Last Modified: Wed, 10 Jun 2026 21:17:53 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:d6f5ab871e2c996aca5903436a1320f36f49df0a8b20c760dab3defe7d4a6b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170bf47be484f93335eb4352cef77de160ed0d604413400b2d579e1a97600940`

```dockerfile
```

-	Layers:
	-	`sha256:5f76803ed6b36f493017706d28d335c0852347502aaa2c7b514b4c1f0d25239a`  
		Last Modified: Wed, 10 Jun 2026 21:17:51 GMT  
		Size: 31.5 KB (31509 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull matomo@sha256:debab189c4dacebedbe4de7f3d592b98287a7a45a101e3700e4ade60c5fafa74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58347956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a366cfa40399e0a8b74a23c29d7d626887f239d6463ce71127b67bb66ee1e3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:38:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:38:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:38:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:38:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:38:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:38:30 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:38:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:38:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:41:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:41:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:41:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:41:36 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:41:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:41:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:41:36 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:41:36 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 20:06:33 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 20:06:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:06:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 20:06:34 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 20:06:39 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 20:06:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 20:06:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 20:06:39 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 20:06:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 20:06:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b434f0ccf7b6e34bfd5e6b3f8158f926f8bf79189ca86ad5d157dda729e1c1b2`  
		Last Modified: Fri, 05 Jun 2026 22:41:42 GMT  
		Size: 3.5 MB (3464908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464a13145b0fac2794511bb652cf5beeb455039813515058074cf4c7b7044bcf`  
		Last Modified: Fri, 05 Jun 2026 22:41:41 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dee06ea2e3f9fbddadcd257274cff1cc3cd72785fd393b56917bd962b1e7cc`  
		Last Modified: Fri, 05 Jun 2026 22:41:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b26b20cf449418a7d50b20695a4806461407be91e8bff3e214a3c49c8ea5c20`  
		Last Modified: Fri, 05 Jun 2026 22:41:42 GMT  
		Size: 13.8 MB (13755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87e57ee65156278ee3ee68fd86412c3c3cd9ef07f525f8fb34f45a18222b37c`  
		Last Modified: Fri, 05 Jun 2026 22:41:42 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883e8bd8cdd927a271ea1dc455d93d5c83f2d4e9fb2bbc0535a6c356005380f0`  
		Last Modified: Fri, 05 Jun 2026 22:41:43 GMT  
		Size: 13.8 MB (13757731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caee9f835a66a33dda1b367635e8a55701121ee1ee10e6e2d67185ea6c49632`  
		Last Modified: Fri, 05 Jun 2026 22:41:43 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c323047e980e8eed162b799e65d4c322f4e05ec915b860aaf368cd76f9a0027b`  
		Last Modified: Fri, 05 Jun 2026 22:41:43 GMT  
		Size: 23.0 KB (22978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb7a9a959da64f90ad762535ec0d4defe263023219a744f37699b1132ab4092`  
		Last Modified: Fri, 05 Jun 2026 22:41:44 GMT  
		Size: 23.0 KB (22991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672c624a5368e63147a0d8bb2de7cdeefc7d4faa5216ed8a7c133a7e598780a2`  
		Last Modified: Fri, 05 Jun 2026 22:41:44 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4043594f633452c3ceb233041cccbd8aa501bcfed5904347d9caad5aebf8c15`  
		Last Modified: Tue, 09 Jun 2026 20:06:46 GMT  
		Size: 2.7 MB (2687013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654cc6d031af7b2864d92deaf887e3006bfc9526c3f53408f3a5e870b19bd4eb`  
		Last Modified: Tue, 09 Jun 2026 20:06:46 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3535ced617129e14cd18ac771d9f134012e9afd3f263a64ff622930b726871`  
		Last Modified: Tue, 09 Jun 2026 20:06:46 GMT  
		Size: 21.1 MB (21050445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1b00dd967d86fd681577f8da07f8b030734b423f94f4c7e0ba978ef090459f`  
		Last Modified: Tue, 09 Jun 2026 20:06:46 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af02ae70c8fb960cc7a16df29f1fd90919ff349725ff8b9b57611b0b862e6c6b`  
		Last Modified: Tue, 09 Jun 2026 20:06:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:995a57ab614f27f78956caab11e4bcfd2000f035c479cfe3ba7c7b46308283dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a1783d1eb88283302ef57c4d081e3a4bdecf087c4c559335c92e2ff2d8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:20f4d6f3050193c2de23aa4ab72ecada3eea8c095814bc77757afb09598b5280`  
		Last Modified: Tue, 09 Jun 2026 20:06:45 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull matomo@sha256:4e12d6832a873f646968979175a3f04f4c938de69331277580fe77854f3315ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56964597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5306e4455c9288fed9fc01378cecb3c5a3233329768cafa52808718dbe9e978`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:46:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:46:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:46:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:46:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:46:28 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:46:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:46:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:49:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:49:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:49:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:49:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:49:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:49:37 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:49:37 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:49:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:49:37 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:49:37 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 20:06:50 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 20:06:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:06:50 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 20:06:50 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 20:06:54 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 20:06:54 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 20:06:54 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 20:06:54 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 20:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 20:06:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312f5c7d2ec7c700d490fcca85937d9dd6727f8873f271b059a3fb2575c62a3d`  
		Last Modified: Fri, 05 Jun 2026 22:49:43 GMT  
		Size: 3.3 MB (3274821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb955971665b87240b15eb32d3c31688d2ea8ccef6707d29fd334eeae499e74`  
		Last Modified: Fri, 05 Jun 2026 22:49:43 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec97530422256a42c9b793bc7ffcd789627f62b1ff6436623eeadb956543a995`  
		Last Modified: Fri, 05 Jun 2026 22:49:43 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84bc5d2bd5d9b5930a8115a223d4bb84d6f95022faab47ea288342b0673aa6e`  
		Last Modified: Fri, 05 Jun 2026 22:49:44 GMT  
		Size: 13.8 MB (13755163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda2a7b23821feff1bf8d69e672cd763901477da35a943d9e78a377b3b46b27c`  
		Last Modified: Fri, 05 Jun 2026 22:49:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55e1d349da5386fe19a0459850fa9816070b8be3f445c882bdceebcaa2e3d2`  
		Last Modified: Fri, 05 Jun 2026 22:49:45 GMT  
		Size: 13.0 MB (12991295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0a168401bfce2d086c92f91e77676be42d9788923490f84ba5cbe37e33b480`  
		Last Modified: Fri, 05 Jun 2026 22:49:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddec0e18c63ccd748e0ba3be8d4e6849f06aaac1e47e910c39ed566db87a1c0`  
		Last Modified: Fri, 05 Jun 2026 22:49:45 GMT  
		Size: 23.0 KB (22975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75480693d3c31062ca36181a3eee68873d8abb64e44ef39b6be7ebc00e26c95b`  
		Last Modified: Fri, 05 Jun 2026 22:49:45 GMT  
		Size: 23.0 KB (22994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e7bfe599c03d75c5ef7b270fdcd1986cd6a84d20b4a248b230cb677e7e71c`  
		Last Modified: Fri, 05 Jun 2026 22:49:46 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568ee33d75ab4f37eab6b1b86180707856381d3e21c28dd90b393cc65f2212d`  
		Last Modified: Tue, 09 Jun 2026 20:07:01 GMT  
		Size: 2.5 MB (2548896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a670dbebe3f3429d42cec3c24f2fa7b2b204d0a0d2348447e206ddd50f6c9be`  
		Last Modified: Tue, 09 Jun 2026 20:07:01 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd49ccd5ee3a6f17b67c9952aa88a86aeeae061fc43b05fd79f1b69137655fa`  
		Last Modified: Tue, 09 Jun 2026 20:07:01 GMT  
		Size: 21.1 MB (21050456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e2e9df9ae0244f68dcfb565eb0ef521108b6b84956348f179fd4aad57d0cb`  
		Last Modified: Tue, 09 Jun 2026 20:07:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b936d552595e074490ebd09da37feb1e55aa76e7b2ada0cbaa642748712c46`  
		Last Modified: Tue, 09 Jun 2026 20:07:02 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:ddf71f30b43df5069601f3929676f185caa487e5207243160e85bdc29aaf9813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98948fe48b48f381f459d23ec53e1d272ae636fd071527afc022dfeb9139a468`

```dockerfile
```

-	Layers:
	-	`sha256:b71502bed0b5e4cfab7bcb5b0fdce055a6c709a3431e22145e7cbe35f18743d5`  
		Last Modified: Tue, 09 Jun 2026 20:07:00 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:cf75390c1e1130f3f4c39a14cba2d24b6685f721832572dc40299a1ccf9187b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60243150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee733594eadbca4ce21a76dda618cd3b3c75e70334bffd12344fecff2066e0a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:39:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:39:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:38 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:39:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:54 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:42:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:42:54 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:42:54 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 20:06:07 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 20:06:07 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:06:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 20:06:07 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 20:06:12 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 20:06:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 20:06:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 20:06:12 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 20:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 20:06:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0790422a84699d306dfa38710d010d82e947bbf07a3ae07d47a853006cd2d6e2`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 3.5 MB (3518848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e40dfdbab1bc0d8edb0eb22eb40e6b42ea6c0015693ad3725c15e16ee91de`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54873b1869aac974259a78866c355ab7aa6a3d21290c29f59243d761fe1dcde8`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293d840b2a3bc39d3771b3d57dacd2f2baede0fe8aafb924bc103ed34a1d1745`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 13.8 MB (13755157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53fa9b7f09b268ea494f52f44c44f97c38d1f70bce7a5a231cecd091c6788e`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0160e9c787422b7cb3cb779acb7fdee3c255f70de105dbb128145bb7c86635a2`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 14.8 MB (14821483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b0e957bb818f93212b9728f3caecbf45ff8b63382216f1a46ab2fe39cbe679`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e9ab3ba01d31ad3b5c1f71e41f1046044518b7819c722c9c6a058d6a163aee`  
		Last Modified: Fri, 05 Jun 2026 22:43:03 GMT  
		Size: 23.0 KB (22978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8103d46de60e4fe3badc598dd1f2308df44b0c4e2d62f6f7678f2eb6d37716a9`  
		Last Modified: Fri, 05 Jun 2026 22:43:03 GMT  
		Size: 23.0 KB (22999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a384a71ca6c3d591d224ae80d724d942ad051130278603dd78ac0a633e5b8fe7`  
		Last Modified: Fri, 05 Jun 2026 22:43:04 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c5a86bb0be55bcaf57f8afc177aac0200d67f897e5974c8239001fea7403a2`  
		Last Modified: Tue, 09 Jun 2026 20:06:19 GMT  
		Size: 2.8 MB (2836460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c419a9d7d8339e1e38897ab84a02d267d0f6e5a7071c08a9f7478284f81f70`  
		Last Modified: Tue, 09 Jun 2026 20:06:19 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b9abc9f21e6bb22122034ed7a0036d2acbb739d32268e3dbe21b5931c44e8f`  
		Last Modified: Tue, 09 Jun 2026 20:06:20 GMT  
		Size: 21.1 MB (21050486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565933652d4389076b1388947a78a1237018a6cdb978da6879c9099a3bfb65e`  
		Last Modified: Tue, 09 Jun 2026 20:06:19 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2313ebd6d9f776004442047dbb629d36148edd69c6dae356f2ebd6867451767`  
		Last Modified: Tue, 09 Jun 2026 20:06:20 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:f4ecaf4d375a76fc8818ffd270d19ea484b095b32839b70b189fb8e87d689231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b44b0d078b42454872c1d3c66ad640d8d7a8ec4a6be94e12346b84067e0ad3`

```dockerfile
```

-	Layers:
	-	`sha256:eb3f61c1c4cf26f20d890e7d6454fd2fbef40fb9a2945b8dfe7f7c81a008e5d4`  
		Last Modified: Tue, 09 Jun 2026 20:06:19 GMT  
		Size: 31.6 KB (31643 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; 386

```console
$ docker pull matomo@sha256:8397958796a6b97ba5a5d8485d1f4acab14d50fefa5b3c802bbf065b9a384f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60556914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb941ca4e84696d15f748d7a4aadee2c91894d62eddfe4608e942627ab0ba0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:40:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:40:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:40:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:40:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:40:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:40:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:40:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:40:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:40:15 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:40:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:40:15 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:40:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:40:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:43:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:43:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:43:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:43:44 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:43:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:43:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:43:44 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:43:44 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 20:07:00 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 20:07:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:07:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 20:07:00 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 20:07:04 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 20:07:04 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 20:07:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 20:07:04 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 20:07:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 20:07:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bdc0e9a22f68db4429c0a70fc219b455e333810fc980c79649b7f968be8478`  
		Last Modified: Fri, 05 Jun 2026 22:43:51 GMT  
		Size: 3.5 MB (3536311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6796d8a6b4e9d0022a720867aba351b1af9b053acacbaa74ad5910db508d41cf`  
		Last Modified: Fri, 05 Jun 2026 22:43:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb176ba2497cacfaf75e7e9c102fdfe91a7bed1cae3cd562035a602b98f3540`  
		Last Modified: Fri, 05 Jun 2026 22:43:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce27d955496cdb63ae0494cc97e7679bc649535213b030c09946ec04497a750e`  
		Last Modified: Fri, 05 Jun 2026 22:43:51 GMT  
		Size: 13.8 MB (13755140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913f34f8b5d44eac1487bbc9add90e7e15851a19b4d732c0498a085412e847c`  
		Last Modified: Fri, 05 Jun 2026 22:43:52 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a40419dc7603d1eba13eb9801318e45bf2a2a307dc429ed682be640b8d17138`  
		Last Modified: Fri, 05 Jun 2026 22:43:53 GMT  
		Size: 15.6 MB (15627997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023df6118b292679fac456ea5aca15e41010b0c42d5233c92c6ee9301ab8375c`  
		Last Modified: Fri, 05 Jun 2026 22:43:52 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2d91cf77c36aaf4c52a54e72c9fded7dcba20c3c421a70b68d535cf8827d20`  
		Last Modified: Fri, 05 Jun 2026 22:43:53 GMT  
		Size: 23.2 KB (23171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95784913619bd906705de3ffa214d6d9e3e8945e58179def81292175f87c0809`  
		Last Modified: Fri, 05 Jun 2026 22:43:53 GMT  
		Size: 23.2 KB (23195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b44165c4b3627feb3980e28bfafa170e5fcbad2c96caddaeaecc833498798b`  
		Last Modified: Fri, 05 Jun 2026 22:43:54 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b05aed5e6f938e424df4e9a53d65e10094ee2e9a618aeb8a31bdc5b4cc3fd0`  
		Last Modified: Tue, 09 Jun 2026 20:07:11 GMT  
		Size: 2.8 MB (2834928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6d2232f5084003298885b8dbed21f1dd4fdd629cf915e92c7eee8a5a93dac`  
		Last Modified: Tue, 09 Jun 2026 20:07:11 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e01080d2012e8b4d9c1a9a09d420142eaf53df13b1a59497f864e02bf0feae`  
		Last Modified: Tue, 09 Jun 2026 20:07:12 GMT  
		Size: 21.1 MB (21050854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f4253c095298367dc368542726ab250e9c32ffe43c9277034798ff0ff6c2cd`  
		Last Modified: Tue, 09 Jun 2026 20:07:11 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d982de92e62f63aef13545080aedc2e87f20aa287f1a539ab5055db7ed5cca14`  
		Last Modified: Tue, 09 Jun 2026 20:07:12 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:f98e942504c2aefc31e50d616459921feb17c90a3eb62fab713687d5977ca792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7865fbbb1c54d20c2adf1223ba5e583a16ec8f727ff7ba2b2618fb104034b80`

```dockerfile
```

-	Layers:
	-	`sha256:1980a491b0e428acc06a881a8856f3a46f0e0aa16049f9160d35d1819dd851e4`  
		Last Modified: Tue, 09 Jun 2026 20:07:11 GMT  
		Size: 31.5 KB (31472 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull matomo@sha256:0b1d79449f92666e312fa90315275230eccd37d030124fa211ff2f5b24feb5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62225286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fffd4065b2949d6392928b440b23b5ce127176c20f1bad60f8146c73d3bc569`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.4.22
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 23:01:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 23:01:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 23:06:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 23:06:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 23:06:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 23:06:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 23:06:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 23:06:54 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 23:06:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 23:06:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 23:06:54 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 23:06:54 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 20:10:56 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 20:10:56 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:10:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 20:10:56 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 20:11:04 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 20:11:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 20:11:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 20:11:05 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 20:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 20:11:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c16b15cd3a83d718102a7ef015d6130c04d91aaa162c62e8e14f0e0ac8fc48`  
		Last Modified: Fri, 05 Jun 2026 23:06:43 GMT  
		Size: 13.8 MB (13755350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147ca298290d15e24c8e0710242b96a983cac5d1e5de85fce2963b267bd95e3`  
		Last Modified: Fri, 05 Jun 2026 23:06:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a80dbee2b9666d891de76bc9c42c3550dd7daf2e6cdbf8586f15f6fb1e5571e`  
		Last Modified: Fri, 05 Jun 2026 23:07:07 GMT  
		Size: 16.7 MB (16704492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b5884ee99d445f1f9a52d6b6ae9c81a5942fba5f7b6903f769c683df635c67`  
		Last Modified: Fri, 05 Jun 2026 23:07:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b1dc6a53ddda273828c9e7d82dcff07f6dcc62685015216da628f666b571e`  
		Last Modified: Fri, 05 Jun 2026 23:07:06 GMT  
		Size: 23.1 KB (23077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc4102811bdc73f2035fd1c1e054c1c1784d89e8a28fb3710d24f685b88bcc`  
		Last Modified: Fri, 05 Jun 2026 23:07:06 GMT  
		Size: 23.1 KB (23082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a31e0c7061cc3b0d21fe56e18d15cc6123f09e50a4f5d5f2d419b315411f973`  
		Last Modified: Fri, 05 Jun 2026 23:07:07 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444a266daacdf014fb5774f0e7ecc2d4eafb000b65da0d598bb93ad0cd27a07`  
		Last Modified: Tue, 09 Jun 2026 20:11:17 GMT  
		Size: 3.1 MB (3055816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaba7c1dee1552531f29354f40f2e971069b35bec1baed36831068fc700be78`  
		Last Modified: Tue, 09 Jun 2026 20:11:16 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298aee59c70bec62d282208b8baef7af237e10eb934a63d6c14cbd70bcfeecdc`  
		Last Modified: Tue, 09 Jun 2026 20:11:17 GMT  
		Size: 21.1 MB (21050566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd335b3275288424ca15bfea7cb069e5ece776fb20ca7eb4e6d7f9e9460cbd3d`  
		Last Modified: Tue, 09 Jun 2026 20:11:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32527ff267ccb25a9436feafc5aeb1c0c02b570be8fbdc3cfc1410839374dbcb`  
		Last Modified: Tue, 09 Jun 2026 20:11:18 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:e0b858f188b64dcca19d9fd727e0adf7793163c9627209e592361d95b87fe0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e062968c6e724ca7cc518f200aa3e997ed35183ccba2454d1cf01399ea068b46`

```dockerfile
```

-	Layers:
	-	`sha256:67aa23ce0c71e273a86863055e11d8738651351ddfaee4409b58ac0af6ab6359`  
		Last Modified: Tue, 09 Jun 2026 20:11:16 GMT  
		Size: 31.6 KB (31557 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; riscv64

```console
$ docker pull matomo@sha256:0d14cc6ef412e613a8a62f9e1c89e72a1bb5068c362ed940c0dc247faa286122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60434837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d7547e3497812dd5bf1c81b02512702c41e6d665f30a5d956386b2994aaf2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.4.22
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Sat, 06 Jun 2026 02:36:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 06 Jun 2026 02:36:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 04:34:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 06 Jun 2026 04:34:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 04:34:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 06 Jun 2026 04:34:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 06 Jun 2026 04:34:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jun 2026 04:34:50 GMT
WORKDIR /var/www/html
# Sat, 06 Jun 2026 04:34:50 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 06 Jun 2026 04:34:50 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jun 2026 04:34:50 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 06 Jun 2026 04:34:50 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 21:04:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 21:04:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 21:04:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 21:04:49 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 21:05:08 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 21:05:09 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 21:05:09 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 21:05:09 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 21:05:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 21:05:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0e81bea972865d3688cd1afd9f7e498985c11c6e69b7e3a85fbb0d11dcc35`  
		Last Modified: Sat, 06 Jun 2026 03:35:45 GMT  
		Size: 13.8 MB (13755371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3746412d588e87a976aeb686c330a0bdbd549a7f17f0a6eddb1d6a58e7bfda`  
		Last Modified: Sat, 06 Jun 2026 03:35:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760f9363ed4723df6b0529ff257f7a7b4fdbe25574e06507bfdc8c9fee070567`  
		Last Modified: Sat, 06 Jun 2026 04:35:44 GMT  
		Size: 15.4 MB (15360947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6370fa8d1961f461529e037b20f4d0317febef3bc749b9f3b57095c74ff6a81`  
		Last Modified: Sat, 06 Jun 2026 04:35:42 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b91f7caa176ba152a910f6adb715fde68169e13633c8cd464471543f172c7e`  
		Last Modified: Sat, 06 Jun 2026 04:35:42 GMT  
		Size: 23.1 KB (23073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7168e536156d48fb514e3e563a4724bd3eb04ce95a04ed617dccfe3011d33adf`  
		Last Modified: Sat, 06 Jun 2026 04:35:42 GMT  
		Size: 23.1 KB (23090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408200f2d4c687053b355c40879360799354dfe317f9a1d1c92718327e9c1798`  
		Last Modified: Sat, 06 Jun 2026 04:35:43 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e818994a3601356010a64109d3a9201a0dd8be385438e3c5e99db7898bf06`  
		Last Modified: Tue, 09 Jun 2026 21:05:59 GMT  
		Size: 2.9 MB (2884980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4bbb7154243fa61a3e78cbd2849fa598f6b093ae3e16c285d18cde409353a`  
		Last Modified: Tue, 09 Jun 2026 21:05:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4211e5903c55ecb9e6a2b1c7828d66b35c860914f1cc8341282e3267eeb9c9c0`  
		Last Modified: Tue, 09 Jun 2026 21:06:02 GMT  
		Size: 21.1 MB (21050576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becbca1f5a898233ef7daf2e39e951af685176f717b27d80078e236c38e9001d`  
		Last Modified: Tue, 09 Jun 2026 21:05:59 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55342a6cb9bb48cde88d2bd7461955a74d5195dbf9f75998070c920dd49177f`  
		Last Modified: Tue, 09 Jun 2026 21:06:01 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:87f0ea05d27a508b4de1d24a0f71a568b9309a98adaad4fe258e12ce08d3ddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6460a466f50aaed3949951b44c1e273320ce1e52f2f8c833d33ab866de008fde`

```dockerfile
```

-	Layers:
	-	`sha256:14d8352fe5f284697a96de67ccc60f219d290445165cac21dcabb053f9b491a8`  
		Last Modified: Tue, 09 Jun 2026 21:05:58 GMT  
		Size: 31.6 KB (31557 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; s390x

```console
$ docker pull matomo@sha256:50cdd5b0c79720a8783249ce8bb14a3386d33729954332d7bf79791d3025a893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60919677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d5e5fbea644f960c91dcadd3460485de0352d0ebc5bcd668f12a733f79e9e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_VERSION=8.4.22
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:53:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:53:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:53:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:53:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:53:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:53:57 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:53:57 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:53:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:53:57 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:53:57 GMT
CMD ["php-fpm"]
# Tue, 09 Jun 2026 20:06:00 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 09 Jun 2026 20:06:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
ENV MATOMO_VERSION=5.11.0
# Tue, 09 Jun 2026 20:06:05 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Tue, 09 Jun 2026 20:06:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Tue, 09 Jun 2026 20:06:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Jun 2026 20:06:05 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2026 20:06:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 20:06:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5b23cd7e08583775ca52654782b3eb898be0895811ff074d0b60e2bdabdca`  
		Last Modified: Tue, 05 May 2026 23:50:39 GMT  
		Size: 3.8 MB (3787468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f70f6e1cd967f35b17107285a2dc3920f6cf2d49ba0521083fa3949317113`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc64825ed6643492e29ef55789e3eb5ed14b413945792b7bc86db5b7c4e70c`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a96cf25fba74c91d013b5bed76070e778fd82d18f1e23abbfaa747d842e86`  
		Last Modified: Fri, 05 Jun 2026 22:54:10 GMT  
		Size: 13.8 MB (13755356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13e4d25fd7313fb8fb05c8309957081b53740dfa142a0d64d5f602be319340`  
		Last Modified: Fri, 05 Jun 2026 22:54:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cf5b6f543dcfd04f056dbf72b83980f6f9eaef2aae1d83e45fa4be991cc59b`  
		Last Modified: Fri, 05 Jun 2026 22:54:10 GMT  
		Size: 15.6 MB (15628140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569686aefa3db07a5cfda358acc345a62db9749ce9c0e2748a2ac6b833fa9561`  
		Last Modified: Fri, 05 Jun 2026 22:54:09 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44c43cd582e3bd156cdfc3f07eb75fe1677e03280b79cf9a232924e40205878`  
		Last Modified: Fri, 05 Jun 2026 22:54:10 GMT  
		Size: 23.0 KB (23036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f35403100d76c3020d8326bc672e7570d4d1e9a4729ddbf55b43afd77b814`  
		Last Modified: Fri, 05 Jun 2026 22:54:10 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e5742ab01cad5086b9b54b0173e4628325e86d2a5967f59a73fc2d968bf98`  
		Last Modified: Fri, 05 Jun 2026 22:54:11 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0342f480d1b0a5d90affc42207e3f800753302a72f5a90a2995f63484c5420a1`  
		Last Modified: Tue, 09 Jun 2026 20:06:16 GMT  
		Size: 2.9 MB (2910711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c9dc714d96d95fcf736caf98eb82e42914cf9621cd340bec72619e66ca991a`  
		Last Modified: Tue, 09 Jun 2026 20:06:16 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0173d2e8303a01c0aeac7fbd4d4e7254e5ecc6e3a6d8caea2e537d4ffe9e6669`  
		Last Modified: Tue, 09 Jun 2026 20:06:17 GMT  
		Size: 21.1 MB (21050498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc96613b5f5144cbac0e6d329c799dc4c582491beafb334d21e4b26498c05b5a`  
		Last Modified: Tue, 09 Jun 2026 20:06:16 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7186e685e071ed0938c024e7fede53506091e4d477c0e66752936e28809c889b`  
		Last Modified: Tue, 09 Jun 2026 20:06:17 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:3b79a48fe3872f8c99696ca9e1f270a4fefa6417304fab72a3e8e50f79773883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32295a1ce2d7ab89e460785d89bfad25d5dc9d4a3ce0d81b16656f2622ce8366`

```dockerfile
```

-	Layers:
	-	`sha256:a599c2d8f2ceee4a3548b00a523bd401178b9a3823f1663c44e480069eacc1bc`  
		Last Modified: Tue, 09 Jun 2026 20:06:16 GMT  
		Size: 31.5 KB (31509 bytes)  
		MIME: application/vnd.in-toto+json
