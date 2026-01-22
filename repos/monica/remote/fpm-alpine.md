## `monica:fpm-alpine`

```console
$ docker pull monica@sha256:69543739810a231ef5e49aa19fe37ed1951b41e14baf1fb2717f0cad3a45080a
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

### `monica:fpm-alpine` - linux; amd64

```console
$ docker pull monica@sha256:b751d68c4534f134b02a21a6f39d486b970361b5a54d5e99b1539c898b7b1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71315996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72842caa7a99f19a49e121afb90fc9831e06d95e7750bebdd8c3cd04ea26ea8f`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:38:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:38:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:38:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:38:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_VERSION=8.2.30
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Fri, 09 Jan 2026 22:38:54 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Fri, 09 Jan 2026 23:05:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:05:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:08:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:08:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:08:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:08:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:08:13 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:08:13 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:08:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:08:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:08:13 GMT
CMD ["php-fpm"]
# Fri, 09 Jan 2026 23:42:41 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 09 Jan 2026 23:42:41 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Fri, 09 Jan 2026 23:44:19 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 09 Jan 2026 23:44:19 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 09 Jan 2026 23:44:19 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 09 Jan 2026 23:44:19 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 09 Jan 2026 23:44:20 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Fri, 09 Jan 2026 23:44:20 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:44:20 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 09 Jan 2026 23:44:20 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 09 Jan 2026 23:44:26 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:44:26 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:44:26 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 09 Jan 2026 23:44:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785d373b978b2bfc266463c855de9f849431296724003dce76e818041e8d3aea`  
		Last Modified: Fri, 09 Jan 2026 22:42:46 GMT  
		Size: 3.6 MB (3591448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573149c9d6eff025e5435f00f18f77a18bc755cfa80aee684b9ab7baf1a5a04a`  
		Last Modified: Fri, 09 Jan 2026 22:42:39 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607d7832cb22cfe925169dbe588adfd7d945386a1ed986830599b7a0eb7f2b15`  
		Last Modified: Fri, 09 Jan 2026 22:42:46 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4d11037e2db2fca3633b784bd1a6fe6b8ef3cea70f82d0d9bc8c05b7475881`  
		Last Modified: Fri, 09 Jan 2026 23:08:28 GMT  
		Size: 12.2 MB (12177924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0bd3b3a158fb6dab04050283cc488c40ad96c57d374b9d387f161acd0fabd9`  
		Last Modified: Fri, 09 Jan 2026 23:08:20 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8396bae9b6cc342a6d9b1280597f3d4cb69f3e6a49b70d5686551049e155432f`  
		Last Modified: Fri, 09 Jan 2026 23:08:21 GMT  
		Size: 13.1 MB (13120538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff973eb0151552d77d42729b3d91f08105226ce1c07b271bd6a46a08867ba38`  
		Last Modified: Fri, 09 Jan 2026 23:08:27 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b192136b48dab53b2ce9ca87acd329180d07dc4be020ac6a81daf1ab898782a`  
		Last Modified: Fri, 09 Jan 2026 23:08:27 GMT  
		Size: 23.5 KB (23503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000e2b14071bd95a29bc4bd7b9e454e533f3178e603f3f2075eb5376a2b78cf4`  
		Last Modified: Fri, 09 Jan 2026 23:08:27 GMT  
		Size: 23.5 KB (23514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1497ddb9e1c481ed3ef72c2e88c57ddeeae25844a9037173ddce80d6548b77`  
		Last Modified: Fri, 09 Jan 2026 23:08:27 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58be325ecd706f0d27893d7b2131a9faa31ec466928d1d5e71ef30cd0c07f6`  
		Last Modified: Fri, 09 Jan 2026 23:44:42 GMT  
		Size: 1.2 MB (1202056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f29cd237110380d8ef8a7e052edca407dcb91e2664b49cb4c7c0f58c08150a`  
		Last Modified: Fri, 09 Jan 2026 23:44:35 GMT  
		Size: 8.9 MB (8885994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551850363fd89076855dc0db6ac98d77dea49d6a2a1b18e93cf458172d3d4646`  
		Last Modified: Fri, 09 Jan 2026 23:44:42 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d903b04f055be40dfeb47be1a001f09ab5cea8dc1b89009ced1eda7d953952b0`  
		Last Modified: Fri, 09 Jan 2026 23:44:42 GMT  
		Size: 33.2 KB (33155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e059f353b7532c916b5724a0130823ea626df84ab888de2e2e82a57fec234d5`  
		Last Modified: Fri, 09 Jan 2026 23:44:46 GMT  
		Size: 28.4 MB (28382136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75ac80925c056d9a9b8b523c9f0b5f17f4ccf31294d965819753194c764e6af`  
		Last Modified: Fri, 09 Jan 2026 23:44:36 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:b5ae81bf64205de6dc14649ad0744b1de2a3ce05a1142f06d00c12d54475b998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 KB (47049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65b247464445d8180b327bcd76fb8320a3fa47abce3199ee38b9bdfb22375e8`

```dockerfile
```

-	Layers:
	-	`sha256:8046ae96d4c4205dae56a7950ebb323cc21e03c69826c8045d903da5ca2d9fc4`  
		Last Modified: Sat, 10 Jan 2026 02:06:24 GMT  
		Size: 47.0 KB (47049 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; arm variant v6

```console
$ docker pull monica@sha256:6f20e5bd98cd28a80e5c8e1e0fe902f739593c5aaf5608c81a4356f75e088be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69319193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bddfe421ce9c2350787f6d647fc843fe877910f0ca2f7b77e11d65ebc7c3166`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 10 Jan 2026 01:09:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 10 Jan 2026 01:09:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 10 Jan 2026 01:09:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 10 Jan 2026 01:09:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_VERSION=8.2.30
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Sat, 10 Jan 2026 01:09:59 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Sat, 10 Jan 2026 01:17:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 10 Jan 2026 01:17:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:20:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 01:20:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:20:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 01:20:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 01:20:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 01:20:14 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:20:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 01:20:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 01:20:14 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 01:20:14 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 05:14:43 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Sat, 10 Jan 2026 05:14:43 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Sat, 10 Jan 2026 05:16:50 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 05:16:51 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 10 Jan 2026 05:16:51 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Sat, 10 Jan 2026 05:16:51 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 05:16:51 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Sat, 10 Jan 2026 05:16:51 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 05:16:51 GMT
ENV MONICA_VERSION=v4.1.2
# Sat, 10 Jan 2026 05:16:51 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Sat, 10 Jan 2026 05:16:59 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Sat, 10 Jan 2026 05:16:59 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 05:16:59 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Sat, 10 Jan 2026 05:16:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01796309e0e05e5057880c9589c5fbe8f06f10e0e7d4aa37c1f356b9b44c9db`  
		Last Modified: Sat, 10 Jan 2026 01:13:26 GMT  
		Size: 3.5 MB (3548054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13f74a8874045498885571dcf4c5fa992d342dbf80ee139a18c506282578c82`  
		Last Modified: Sat, 10 Jan 2026 01:13:26 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5e7a7225010f8283d9f1744d771d11b6127b0a8259436bc59c9b827e0de65`  
		Last Modified: Sat, 10 Jan 2026 01:13:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc43ca4d5662103a865edce20c21611127b1323f5ae27b5950f0c40e0db9043a`  
		Last Modified: Sat, 10 Jan 2026 01:20:26 GMT  
		Size: 12.2 MB (12177927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1a2fdd1e5ae1bfeca86a88d7b07b234a2516ee2c8e63764169cc22963a871a`  
		Last Modified: Sat, 10 Jan 2026 01:20:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba10e34d4f072cdb7ffd398a5b368333599f029e869f3416dc2b699c76020c`  
		Last Modified: Sat, 10 Jan 2026 01:20:20 GMT  
		Size: 11.9 MB (11871377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f829077a5ee080adeab687f74420089ebdb78cd9823d1687d527dfeebac8063`  
		Last Modified: Sat, 10 Jan 2026 01:20:19 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef80cbc19fe82ecf00dee359fb80c72a5d10f5185b086e4323bc119eb7b5106d`  
		Last Modified: Sat, 10 Jan 2026 01:20:25 GMT  
		Size: 23.3 KB (23332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6180556f8931dedb3f0db95bbca21432417caa98869e3789fc56e1980b92d4`  
		Last Modified: Sat, 10 Jan 2026 01:20:21 GMT  
		Size: 23.3 KB (23348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a963e292a474874211c1dc32e6cc38e0ecabb41ec08378474b26c1dd60022`  
		Last Modified: Sat, 10 Jan 2026 01:20:21 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd100f7fa0332c565df6a12fe43b98412f196c2d3d2c5b6a13ff26fc2fbdee81`  
		Last Modified: Sat, 10 Jan 2026 05:17:08 GMT  
		Size: 1.2 MB (1245703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32d101455446ac9ce429e945284f67ebd4a5f7b63f0ef36cd71dc30c03ac4b2`  
		Last Modified: Sat, 10 Jan 2026 05:17:16 GMT  
		Size: 8.4 MB (8429952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf810d4c46ca617186aab72c708d9ddf3259f5cda6dfd450b4f37cad6ce356`  
		Last Modified: Sat, 10 Jan 2026 05:17:08 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83cef5c98829abc7ef0add8e5b0ce536c906c51d0e384d90512096e6160ab7`  
		Last Modified: Sat, 10 Jan 2026 05:17:16 GMT  
		Size: 33.2 KB (33182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb86f2523539fcab203235e1d92918d424f0d78c9a920923e0edc5e3f6ad235`  
		Last Modified: Sat, 10 Jan 2026 05:17:19 GMT  
		Size: 28.4 MB (28382259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8babac4f9104f1e51c9e5871d56e5e2c67977a8ca145555f2a11804155217bda`  
		Last Modified: Sat, 10 Jan 2026 05:17:09 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:c4029ca9d902f024d80f4b13122a495a3611d5b35ebaf1fcfb78e3383f72c3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 KB (47181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b334988138c1ea31605f1a10561b252c8d9a78328b8c304a8675d74f9ba309c`

```dockerfile
```

-	Layers:
	-	`sha256:8c6d65c970242204096c0b62c62daf3bb702e1c0813e4af9deefafda8860dfa1`  
		Last Modified: Sat, 10 Jan 2026 08:05:34 GMT  
		Size: 47.2 KB (47181 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; arm variant v7

```console
$ docker pull monica@sha256:2ba46b1ed4039a29baf6d2863de21e7842c23f9b92845da94ba20aca4c7dd0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67893269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9e68e5c2a0811cfc91928bdc63ad5fa454fbba59176d833a22e43a0f6f1720`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:51:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:51:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:51:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:51:00 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_VERSION=8.2.30
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Fri, 09 Jan 2026 22:51:00 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Fri, 09 Jan 2026 23:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:42:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:45:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:45:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:45:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:45:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:45:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:45:24 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:45:25 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:45:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:45:25 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:45:25 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 00:58:03 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Sat, 10 Jan 2026 00:58:03 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Sat, 10 Jan 2026 01:00:10 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 01:00:10 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 10 Jan 2026 01:00:10 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Sat, 10 Jan 2026 01:00:10 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 01:00:10 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Sat, 10 Jan 2026 01:00:10 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:00:10 GMT
ENV MONICA_VERSION=v4.1.2
# Sat, 10 Jan 2026 01:00:10 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Sat, 10 Jan 2026 01:00:17 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Sat, 10 Jan 2026 01:00:18 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:00:18 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Sat, 10 Jan 2026 01:00:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2deecbd9424de58cf965e9b8ae732ce31ad325fff67038bf1ef7b83cc8e06dc`  
		Last Modified: Fri, 09 Jan 2026 22:55:42 GMT  
		Size: 3.3 MB (3346804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda575c2dec066714428613b9baefea23466c735d7ce1b8ce2efd7cd10912a46`  
		Last Modified: Fri, 09 Jan 2026 22:55:34 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e4e0e5a295b3e78bc8c9b2fdb0f3171d31bdd6dcb309ca10e785f3cbcae0a5`  
		Last Modified: Fri, 09 Jan 2026 22:55:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf3b8d3083a62df6c1bc52947c283042f8c30b29993e1d5bd66f3788342e499`  
		Last Modified: Fri, 09 Jan 2026 23:45:39 GMT  
		Size: 12.2 MB (12177938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad14de5f809c822558905827877679f993c8c54bcef841aec854041b19c746ff`  
		Last Modified: Fri, 09 Jan 2026 23:45:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc42cc99c0dc945c88c4336c10a70bed480ba5def2d70e0c97ca9efe6758359`  
		Last Modified: Fri, 09 Jan 2026 23:45:31 GMT  
		Size: 11.2 MB (11175463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e060fcf66fa0ff49fd5bf9d61fc75bce4ff346adeb0038009d5ff3eb66246e0a`  
		Last Modified: Fri, 09 Jan 2026 23:45:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1d2e4597d2821f61bd4ec8eb80fbf4094e88c5146a0d59444de57b3d222323`  
		Last Modified: Fri, 09 Jan 2026 23:45:32 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae71bff9cb31391a98915df8b13c1e3c0974ae28c49fc11ad8c3046385bcae1`  
		Last Modified: Fri, 09 Jan 2026 23:45:32 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfd06575bfe2cf24fd4c0b1a6254ee2f721f6862aced85d262fb179fafcf449`  
		Last Modified: Fri, 09 Jan 2026 23:45:33 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb1f85951f27c09167aa54dd335d814fb6811d1498118cc7c445f2eeba3d197`  
		Last Modified: Sat, 10 Jan 2026 01:00:28 GMT  
		Size: 1.1 MB (1128375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5439b1bd1dcde7da9c5e7e21555778f68be24f47cb164d3cd47a0e7be40e6f00`  
		Last Modified: Sat, 10 Jan 2026 05:06:47 GMT  
		Size: 8.3 MB (8307580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc21c2eee4c252595e2b39e800decd957a847bef105492abe046d4610dd737`  
		Last Modified: Sat, 10 Jan 2026 01:00:27 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba50cbf75e678f42de37f8f535ef66de69e0f78181afef23918c65b97ed23dd`  
		Last Modified: Sat, 10 Jan 2026 01:00:29 GMT  
		Size: 33.2 KB (33175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484db6b3993c620839de32c5f3285c2049e6fddbe0448ff0e8956474901b16c`  
		Last Modified: Sat, 10 Jan 2026 01:00:30 GMT  
		Size: 28.4 MB (28382226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fc810667f42f738ecf55c329f85a37cc2eb22f8cf8344b707cea6cb9fe80a8`  
		Last Modified: Sat, 10 Jan 2026 01:00:40 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:d12136b9e23c6e87076814dcde3a924bbf8f7fefbd6ad2c53213a32b97725e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 KB (47181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ef2d82dbfc99f8c6631cdd1dc3cc5934db5a4db66678005815fc14af604206`

```dockerfile
```

-	Layers:
	-	`sha256:00ce94b0b70789c4f191e120e011c27b56dcecdda2cf9f50b8fe885da5621f9e`  
		Last Modified: Sat, 10 Jan 2026 05:06:13 GMT  
		Size: 47.2 KB (47181 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull monica@sha256:21efd996b4e19c36d593233ee4caf61a9650a0e5fa2752a3cc7ef7bffa35f277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71585150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d33a517321baa2509f8eb6b1646972ac5b39168403ada13a7ecdebe5c47e8a1`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:30:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:30:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:30:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_VERSION=8.2.30
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Fri, 09 Jan 2026 23:09:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:09:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:13:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:13:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:13:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:13:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:13:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:13:23 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:13:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:13:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:13:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:13:23 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 00:28:54 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Sat, 10 Jan 2026 00:28:54 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Sat, 10 Jan 2026 00:30:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 00:30:39 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 10 Jan 2026 00:30:39 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Sat, 10 Jan 2026 00:30:39 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:30:40 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Sat, 10 Jan 2026 00:30:40 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:30:40 GMT
ENV MONICA_VERSION=v4.1.2
# Sat, 10 Jan 2026 00:30:40 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Sat, 10 Jan 2026 00:30:46 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Sat, 10 Jan 2026 00:30:46 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:30:46 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Sat, 10 Jan 2026 00:30:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777d5c3b20a0769c518333c82792a673bd3f284fb8384dfaa40374fca9fc7a5e`  
		Last Modified: Fri, 09 Jan 2026 22:34:10 GMT  
		Size: 3.6 MB (3601005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c963135034fa57462efb8d4d9232302203971aecbd3f011473657aae0aad5`  
		Last Modified: Fri, 09 Jan 2026 22:34:09 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec838d139fcc806345b1d7ed067126d85b48b94190fbec736aacd82e1786de58`  
		Last Modified: Fri, 09 Jan 2026 22:34:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fd89c50ef4372d1052730ff14450fb24d772198cbec8fa50777f09dc0e9e4c`  
		Last Modified: Fri, 09 Jan 2026 23:13:31 GMT  
		Size: 12.2 MB (12177915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859bf07d0f3a04b32a0f2b68af7ff42e7a50f1a6ef9870455b0f9374d000128f`  
		Last Modified: Fri, 09 Jan 2026 23:13:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4458790f6fe5b451cdeef8d4c9ff539a7e0c9eb7c59175e4bc95ab99b8684`  
		Last Modified: Fri, 09 Jan 2026 23:13:31 GMT  
		Size: 13.0 MB (13019726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21afbc4ca3417b31226893cc328253ed11d0db0fe6c11c08491e64de0081f87`  
		Last Modified: Fri, 09 Jan 2026 23:13:37 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47f5e0528317ccb7e894a915e892cc37e5a8d017d6c1692f14f87b48fa272c`  
		Last Modified: Fri, 09 Jan 2026 23:13:31 GMT  
		Size: 23.4 KB (23350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a1ff440cf89cfb2de0cb8083d437ea98e21549cefde30b60535124f1a59bd`  
		Last Modified: Fri, 09 Jan 2026 23:13:37 GMT  
		Size: 23.4 KB (23371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d8dabef176108faeff31897752dfe220229c0fb157ee71f4026b7e0398ce1b`  
		Last Modified: Fri, 09 Jan 2026 23:13:37 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b447c95847cc67130b245c032dba76d1babe31d60c465bc032b8bc5f13eeff0`  
		Last Modified: Sat, 10 Jan 2026 00:30:54 GMT  
		Size: 1.3 MB (1287421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866857564461b28e8b90c4d6e6e5067f8d5e074367b223a917871c5c83f9df65`  
		Last Modified: Sat, 10 Jan 2026 00:30:55 GMT  
		Size: 8.8 MB (8825592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b065b8b8819e82f5a268f71c75f8cf6706acd32e7d887af558cf047bac07b4`  
		Last Modified: Sat, 10 Jan 2026 00:30:54 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1b84f6d4249754caf6d0f03ca21bfd541092bcffa154ef88575493eb58fa3c`  
		Last Modified: Sat, 10 Jan 2026 00:30:54 GMT  
		Size: 33.2 KB (33179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a13fdf43065e79916b4e47d7c7369e402ad0554b705f17cda2b3b34ff26ab`  
		Last Modified: Sat, 10 Jan 2026 00:30:56 GMT  
		Size: 28.4 MB (28382233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d2528c000f96d1bcac282bf3052dbc47693569b44c503e493f43ddc08c35ab`  
		Last Modified: Sat, 10 Jan 2026 00:31:01 GMT  
		Size: 2.1 KB (2073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:b641a99c3002874d573d0cc4a9c9f25726838a0ed6638e36837bbb8240ec8f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 KB (47212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82310d7f6904f75516ac49c6bf27708f41d831888c99281f7becaf1c37aecd18`

```dockerfile
```

-	Layers:
	-	`sha256:97671cdb3fbc9b362efe52d4d03fb3dc1bbd1e015545660bcd240f5dda9a871c`  
		Last Modified: Sat, 10 Jan 2026 02:06:31 GMT  
		Size: 47.2 KB (47212 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; 386

```console
$ docker pull monica@sha256:c0fcd220fb9cdf860359c69ea075623293c3c5c0afcd6acdbdc43e5c5e9b2dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71731817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8811548962423d4936edf032942619c12d52be0df1d03ff6c37b77f07792fa8b`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:34:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:34:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:34:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:34:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:34:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_VERSION=8.2.30
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Fri, 09 Jan 2026 22:34:40 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Fri, 09 Jan 2026 23:04:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 23:04:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:07:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:07:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:07:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:07:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:07:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:07:23 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:07:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:07:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:07:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:07:23 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 00:12:27 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Sat, 10 Jan 2026 00:12:27 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Sat, 10 Jan 2026 00:13:58 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 00:13:58 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 10 Jan 2026 00:13:58 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Sat, 10 Jan 2026 00:13:58 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:13:58 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Sat, 10 Jan 2026 00:13:58 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:13:58 GMT
ENV MONICA_VERSION=v4.1.2
# Sat, 10 Jan 2026 00:13:58 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Sat, 10 Jan 2026 00:14:05 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Sat, 10 Jan 2026 00:14:05 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:14:05 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Sat, 10 Jan 2026 00:14:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecea159a0d603bf1e53c4ec7618b7333ef69ddaf0741abda78e4cd1fe977feba`  
		Last Modified: Fri, 09 Jan 2026 22:38:17 GMT  
		Size: 3.6 MB (3628695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbef4948aaa74a378ffa781e8755bb5eee329b35e7aafc6a79b76f3ad16e9ac`  
		Last Modified: Fri, 09 Jan 2026 22:38:10 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ead130cb73c697b23c4e8f0def4fab18675e07129c28c408dd4daa0cd273ff`  
		Last Modified: Fri, 09 Jan 2026 22:38:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffcaae4f4ea17994a20b3aa33a9ae318c13017de21564cd4dea4a44980001cf`  
		Last Modified: Fri, 09 Jan 2026 23:07:37 GMT  
		Size: 12.2 MB (12177909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179c9aa6045b6b91a9fc5527ac5df9a28cc88e8a248e783e31c32f60ad059dbb`  
		Last Modified: Fri, 09 Jan 2026 23:07:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873020125e97b927c6114a179510a70837b9cc927996f75813a7af75ad91c433`  
		Last Modified: Fri, 09 Jan 2026 23:07:37 GMT  
		Size: 13.4 MB (13394190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6cca6540b56787c92ae4870059ffe3be737c81a95bc796e7085a405b2ac0f9`  
		Last Modified: Fri, 09 Jan 2026 23:07:30 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ad597eac33ea5cedb6f40ba14178110582ae5f8a7a474e97626ad970689795`  
		Last Modified: Fri, 09 Jan 2026 23:07:31 GMT  
		Size: 23.5 KB (23512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a56e1b82731e3ae66f388c2577c4b5a61eba8cdae62c63d12ffbe6e17660624`  
		Last Modified: Fri, 09 Jan 2026 23:07:37 GMT  
		Size: 23.5 KB (23530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddbfd95a3f6ecc5c475c5d1f1879310793e1dfae99898265f030e6af9b76f2b`  
		Last Modified: Fri, 09 Jan 2026 23:07:32 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de597f1bfa3d35b39551dc14e4c94271bf3e241b74ab17748e1cf506ed2855`  
		Last Modified: Sat, 10 Jan 2026 00:14:21 GMT  
		Size: 1.2 MB (1216229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba41a7bd70ca20bb2b6293c21fb14a2e2d8dbcbea12e38f55fa8d5f8fb8afe7c`  
		Last Modified: Sat, 10 Jan 2026 00:14:23 GMT  
		Size: 9.2 MB (9150644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16a2d96d177cd2c03682ae0b2cccf9aaa3151cac455f1794866aa00a03ac8ea`  
		Last Modified: Sat, 10 Jan 2026 00:14:13 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2fa6af04906e58e117bd70b0207ab34904949a82e1c7d45cf07d2ac1f41e7c`  
		Last Modified: Sat, 10 Jan 2026 00:14:21 GMT  
		Size: 33.2 KB (33160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9689baca4b74bcc2a91fc42939c83a37db40937e32106ae4eb0d6e90c527212e`  
		Last Modified: Sat, 10 Jan 2026 00:14:15 GMT  
		Size: 28.4 MB (28382227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12030fb44c0e4c211af28bf283334145da8637e9e75616ec819508a7afc5234f`  
		Last Modified: Sat, 10 Jan 2026 00:14:21 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:f14ec4a6802e3b77d55a544e620c54e33cca8afabfb467f3178da8c2b0e94b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 KB (47009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d4b024beddb65735df3bf508b51479d38ba7018a7213ee6eb06427d8bdca3b`

```dockerfile
```

-	Layers:
	-	`sha256:17bc46f01b7d60214d47bfc79f1d581806646d1860180a8b7634e378da556d91`  
		Last Modified: Sat, 10 Jan 2026 02:06:35 GMT  
		Size: 47.0 KB (47009 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; ppc64le

```console
$ docker pull monica@sha256:6a15724edac6d96a34878c893a912575c8c0ed08f20ba2da6e198e88be13bc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72618255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f041985e485fc280972f661dc194ee5ddf6640f32afd90ab4f9388093c44402`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_VERSION=8.2.30
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Sat, 10 Jan 2026 02:11:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 10 Jan 2026 02:11:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 02:16:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 02:16:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 02:16:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 02:16:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 02:16:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 02:16:37 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 02:16:38 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 02:16:38 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 02:16:38 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 02:16:38 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 04:54:13 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Sat, 10 Jan 2026 04:54:13 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Sat, 10 Jan 2026 04:56:49 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 04:56:50 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 10 Jan 2026 04:56:50 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Sat, 10 Jan 2026 04:56:50 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 04:56:51 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Sat, 10 Jan 2026 04:56:52 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 04:56:52 GMT
ENV MONICA_VERSION=v4.1.2
# Sat, 10 Jan 2026 04:56:52 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Sat, 10 Jan 2026 04:57:02 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Sat, 10 Jan 2026 04:57:03 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:57:03 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Sat, 10 Jan 2026 04:57:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772e0a90d4aa4f209aab27b75a49043c6df83f144ec29ba8e6c8e964a8a165a`  
		Last Modified: Sat, 03 Jan 2026 02:17:29 GMT  
		Size: 3.8 MB (3768859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb9c8b89ecca8688bdf852690f34dbf7da2dc90d2e06d7221c85ff1070c08b`  
		Last Modified: Sat, 03 Jan 2026 02:17:28 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce8460d16487c23dd44b0afef57a49c4aeca53309e968b330dc8c9044d5e51`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb39f97b7bdfb92e95a6124a466fe4347d1c64542e7cc09c1f3fd1bc97257295`  
		Last Modified: Sat, 10 Jan 2026 02:15:29 GMT  
		Size: 12.2 MB (12177947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e47203ae67533bda39ed7f91c42df01e65bc514a42bf2b6b029c078f0cbf2`  
		Last Modified: Sat, 10 Jan 2026 02:15:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f60724c21b31aa517e142c6638ebe7487be287bccacf01a65b5234317cfb3a`  
		Last Modified: Sat, 10 Jan 2026 02:17:11 GMT  
		Size: 13.7 MB (13670421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42cd4168d976f344d566c1d1c25ef1b738cb2a772e3c73173371be912ad696`  
		Last Modified: Sat, 10 Jan 2026 02:16:59 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc6d3120d608bec41f7338de54ff48b56bded1ae4980e63b3ad3f368582d9b0`  
		Last Modified: Sat, 10 Jan 2026 02:17:00 GMT  
		Size: 23.4 KB (23358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357fd71c87ec9665c5ac254fd2d733fb2cd694bd5a4262800ab39d18348ed6c2`  
		Last Modified: Sat, 10 Jan 2026 02:17:07 GMT  
		Size: 23.4 KB (23375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f4af19d00c33faec70338ddb59d6a2430906860ba64fb2242d619a5a20d82a`  
		Last Modified: Sat, 10 Jan 2026 02:17:06 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397e0344d153605b0d49e6a45126e4066dcfac21f2437c5ea5a4d63b48a4837e`  
		Last Modified: Sat, 10 Jan 2026 04:57:21 GMT  
		Size: 1.3 MB (1310383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed315115cafb4feed4f907f6df2d4349ad0a55268a2639b6d43fdebcc6ae5c84`  
		Last Modified: Sat, 10 Jan 2026 04:57:30 GMT  
		Size: 9.4 MB (9385044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd81231bf179bf763a0c3ea917193e0254760729648245f2fe0490b87e0af23`  
		Last Modified: Sat, 10 Jan 2026 04:57:20 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd32a8e54961ebed5e86cbdc21fc3658184979adb9216fee4287c99e7842bc`  
		Last Modified: Sat, 10 Jan 2026 04:57:21 GMT  
		Size: 33.2 KB (33186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb954176269c9c435f1e3b4db2ba113fd8b88f33a38648d174c6775e1e71727f`  
		Last Modified: Sat, 10 Jan 2026 04:57:23 GMT  
		Size: 28.4 MB (28382297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7912d38bc02f7e083ba2d520a08ad8357145a917266bab4501e503d853916024`  
		Last Modified: Sat, 10 Jan 2026 04:57:22 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:61ccf5d7ad40897123d608cfc0f371b6923a5028275b7bee8f9706a277ce0b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 KB (47101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7051c796f58cc257f06f4664f8bd0292efe81a63df5cf6cd7cd5c9553c70ddad`

```dockerfile
```

-	Layers:
	-	`sha256:a844d51d552d272e17cd350f40a125454fe50b2d2a9fbf8b4c2c58b4df009d45`  
		Last Modified: Sat, 10 Jan 2026 04:57:20 GMT  
		Size: 47.1 KB (47101 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; riscv64

```console
$ docker pull monica@sha256:f5d0070b652fdce29395d5a2b20ef205596c09d0ddddf822b39ccd01126757df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70674956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c69dea70271a6fb4b0fb855634752449b553305f685775da366373e0bb8d1a`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.2.30
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Sun, 21 Dec 2025 10:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sun, 21 Dec 2025 10:04:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:27:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 22:27:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 22:27:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 22:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 22:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 22:27:40 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 22:27:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 22:27:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 22:27:40 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 22:27:40 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 09:51:34 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 16 Jan 2026 09:51:34 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Fri, 16 Jan 2026 10:13:02 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 16 Jan 2026 10:13:02 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 Jan 2026 10:13:02 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 16 Jan 2026 10:13:02 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 10:13:07 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Fri, 16 Jan 2026 10:13:07 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 10:13:07 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 16 Jan 2026 10:13:07 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 16 Jan 2026 10:13:53 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Fri, 16 Jan 2026 10:13:54 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 10:13:54 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 16 Jan 2026 10:13:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:00 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:09:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42683d32ff4c11db0af810048c8b5e5c15e75dae80dff1bd8822fc813b8e5aa`  
		Last Modified: Sun, 21 Dec 2025 11:02:06 GMT  
		Size: 12.2 MB (12177931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a906cfea781a04b86d6a5ef4b723593188b1ded9176591314f4e17c13aa5d176`  
		Last Modified: Sun, 21 Dec 2025 11:01:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36376cda8dc8d55758fc09458cdab81b3d7c1ba61568cc65bb46ed680cf767c`  
		Last Modified: Tue, 13 Jan 2026 22:28:30 GMT  
		Size: 12.3 MB (12327242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6218872532b9bcb0b848fb8e1ed9269c517bc3f2009ada8e001e85e288aa2d4e`  
		Last Modified: Tue, 13 Jan 2026 22:28:37 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d327b18e80b7b57725597053ee3634084ec86afac3082b51692eef5f4f08ae`  
		Last Modified: Tue, 13 Jan 2026 22:28:37 GMT  
		Size: 23.3 KB (23337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bdd3c098770bad0ac3d4a4b6e566cbc5063a4f308b61b537d8056004d6e8db`  
		Last Modified: Tue, 13 Jan 2026 22:28:28 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e400cdd246ff0f5cbd2019b9e78a1e7106dde92010fc9183cabc3cf01bd7bc`  
		Last Modified: Tue, 13 Jan 2026 22:28:29 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60cd306b328a0d759a99bb3ab1a8c37388cc9cedc22c3cbc1dbf14f7bfc6534`  
		Last Modified: Fri, 16 Jan 2026 10:15:26 GMT  
		Size: 1.2 MB (1231086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9201446591e8c486f8a40c1fcd74462ba958259879c3269c65af581c143bd6aa`  
		Last Modified: Fri, 16 Jan 2026 10:15:11 GMT  
		Size: 9.1 MB (9136377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56cea10e4c388693c72095dba229f0a371160cfcead39a46d402279536881a7`  
		Last Modified: Fri, 16 Jan 2026 10:15:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203e3dea321a21a57a5309699f6a96dc222871cd3dd2bc63deb1271b8e51881e`  
		Last Modified: Fri, 16 Jan 2026 10:15:09 GMT  
		Size: 33.2 KB (33250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca25d2b03435172adb614089efe1d4a25a54c1f40792895039e2fc7955d752`  
		Last Modified: Fri, 16 Jan 2026 10:15:27 GMT  
		Size: 28.4 MB (28382598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f636836faac9b44873c2db97be3b017d6843a7a8010162860549ae9c2d2eca68`  
		Last Modified: Fri, 16 Jan 2026 10:15:11 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:722342585ad65d764b7c2b7a35f5683973e8f30404da2a17e522c595c2f91ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 KB (47101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc44e3c6497fe5298eab0ef5add621692a57e046d65a93cdfd938602563f5d64`

```dockerfile
```

-	Layers:
	-	`sha256:0a0d4cf6965f9c9bc106e94fdb9b59e228384789328d56bb0667c2c0312da3d4`  
		Last Modified: Fri, 16 Jan 2026 14:05:41 GMT  
		Size: 47.1 KB (47101 bytes)  
		MIME: application/vnd.in-toto+json

### `monica:fpm-alpine` - linux; s390x

```console
$ docker pull monica@sha256:554b8ad451fd2101e31074cf18c6c48969687979444670493dea74c86cb55e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71695112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f78db1abd462e72e1d474179ed3118d238c3b50c2b1dbf79d59edd90adc09c`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_VERSION=8.2.30
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.30.tar.xz.asc
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_SHA256=bc90523e17af4db46157e75d0c9ef0b9d0030b0514e62c26ba7b513b8c4eb015
# Sat, 10 Jan 2026 00:14:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 10 Jan 2026 00:14:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:19:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:19:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:19:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 00:19:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:19:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:19:57 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:19:58 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 00:19:58 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 00:19:58 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 00:19:58 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 01:35:10 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Sat, 10 Jan 2026 01:35:10 GMT
RUN set -ex;         apk add --no-cache         bash         coreutils # buildkit
# Sat, 10 Jan 2026 01:36:59 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         icu-dev         zlib-dev         libzip-dev         libxml2-dev         freetype-dev         libpng-dev         libpq-dev         libjpeg-turbo-dev         jpeg-dev         gmp-dev         libmemcached-dev         libwebp-dev     ;         docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j "$(nproc)"         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;     pecl install APCu-5.1.26;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;         docker-php-ext-enable         apcu         memcached         redis     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions         | tr ',' '\n'         | sort -u         | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'         )";     apk add --no-network --virtual .monica-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 10 Jan 2026 01:36:59 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 10 Jan 2026 01:36:59 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Sat, 10 Jan 2026 01:36:59 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 01:37:00 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini; # buildkit
# Sat, 10 Jan 2026 01:37:00 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:37:00 GMT
ENV MONICA_VERSION=v4.1.2
# Sat, 10 Jan 2026 01:37:00 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Sat, 10 Jan 2026 01:37:06 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apk del .fetch-deps # buildkit
# Sat, 10 Jan 2026 01:37:06 GMT
COPY entrypoint.sh queue.sh cron.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:37:06 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Sat, 10 Jan 2026 01:37:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af672712b2dab3c8a68ddbd40990098668c349a31bf4fe54360519012d2e9`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 3.8 MB (3794529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e82f0b184abfa92d79d92b03514acd8b9f92c2ca083f9fa2e62587fde8871a2`  
		Last Modified: Thu, 18 Dec 2025 00:34:55 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b827f069b40835efda3a88ba34853291bec4baedd59564b9d33abc39667950f2`  
		Last Modified: Thu, 18 Dec 2025 00:34:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4783fa049b90173b098165838b30daf00e85cf447c023c311753a18c46a1649`  
		Last Modified: Sat, 10 Jan 2026 00:18:07 GMT  
		Size: 12.2 MB (12177926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60446855d5f39054d088a76a12634cf67a30ea23e7675e6101dbd9382f5a69`  
		Last Modified: Sat, 10 Jan 2026 00:18:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8e0fbf94ce18e149ab8f18bf5afb1aea8e23cf86d67d50bea26be006a3dfd`  
		Last Modified: Sat, 10 Jan 2026 00:20:09 GMT  
		Size: 13.0 MB (12993339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cde931922919471b91fd766d33903f8711e35c807e929677972093a13396115`  
		Last Modified: Sat, 10 Jan 2026 00:20:09 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac43b95f455b7561da842a05d8021ba8f1a10a658300593facdf7c18307671`  
		Last Modified: Sat, 10 Jan 2026 00:20:09 GMT  
		Size: 23.3 KB (23345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacff4e2cab440805327cfdab412b7d9bc0e5ed20c4d48da772a469a1febdc2a`  
		Last Modified: Sat, 10 Jan 2026 00:20:09 GMT  
		Size: 23.4 KB (23366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83dbed66c285cb37fba635671980db6a088f17e03483825e587e618c0e31ce3`  
		Last Modified: Sat, 10 Jan 2026 00:20:15 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b65acf31261b42f3f3e9d03eafca2585446ffaa1212c123a6ab1cbcf025b7b7`  
		Last Modified: Sat, 10 Jan 2026 01:37:19 GMT  
		Size: 1.3 MB (1288421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c9a8255fd53eb97400f5af598426d6ecf983b5ec7d8c33099a38bf6a6f771`  
		Last Modified: Sat, 10 Jan 2026 01:37:27 GMT  
		Size: 9.2 MB (9238804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ab70164785b80c640f9c69d41f4f76926ceaaca3ac0a205ddd147ae4bd783`  
		Last Modified: Sat, 10 Jan 2026 01:37:26 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0077bd3164c264a1d8ec1e655dbb0e5fc9e47d3b60f211c8d586b420b02f8757`  
		Last Modified: Sat, 10 Jan 2026 01:37:26 GMT  
		Size: 33.2 KB (33198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b078562bacb227571cec35385f8fcf837a27050c99b668a76bdd09257bb6fa`  
		Last Modified: Sat, 10 Jan 2026 01:37:34 GMT  
		Size: 28.4 MB (28382246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1b8bd8aeb9382382c042e5e9c5dc9c41c087ffc9e574921a388ca08921003`  
		Last Modified: Sat, 10 Jan 2026 01:37:20 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `monica:fpm-alpine` - unknown; unknown

```console
$ docker pull monica@sha256:57543c8f0d250b9c0a88c0ddbf9ab9c7b837078b46cb467ef3b38a634108b976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 KB (47049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43c5f84f716763cd4ff3378ebdc7054e89e1438fa759026183a95fc59bc1141`

```dockerfile
```

-	Layers:
	-	`sha256:976c6c75e1696fa5262e57bfebdeb81309dc3bf7c6f81c595cd05a917e87c7a8`  
		Last Modified: Sat, 10 Jan 2026 05:06:23 GMT  
		Size: 47.0 KB (47049 bytes)  
		MIME: application/vnd.in-toto+json
