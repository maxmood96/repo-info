## `friendica:rc-fpm-alpine`

```console
$ docker pull friendica@sha256:646f4bec3a61ced148dc397e3d741cc418e72f7d201c1770073c2973035846e3
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

### `friendica:rc-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:1704006f86c5705c5bd080b1189d7b37184a632a9d6cd828e0b3a7a58b2503a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57892541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772f8e734b3c55a412ad466271249e94a772ef3cda8c3468b6bb212ea467ce10`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cb6cbcf5d0fdf140591bbde6e2c3ad8d2deed71627440f5c05b66952cd945c`  
		Last Modified: Tue, 12 Nov 2024 02:36:59 GMT  
		Size: 5.6 MB (5583571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450db5f67b4f4e16b843a978a2070b6b4db69c3265e1940230a758fd6c7911b4`  
		Last Modified: Tue, 12 Nov 2024 02:36:59 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c7589779dd5b114c16f5991f83e297fb1dd78138175a629641aff0ad6d4d36`  
		Last Modified: Tue, 12 Nov 2024 02:36:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add35aa614f988cb1013a4e459362d9f185c021b889f9d0f43dd1c072785f079`  
		Last Modified: Tue, 12 Nov 2024 02:36:59 GMT  
		Size: 12.1 MB (12147074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe91edfb63694475766071f4bafc71fdead84b271179128b20925736ffbc86`  
		Last Modified: Tue, 12 Nov 2024 02:36:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b631f69a50482605c93516ecf2dedeb2a02abd5b5015fddfec8bf2c573ab0`  
		Last Modified: Tue, 12 Nov 2024 02:37:00 GMT  
		Size: 12.9 MB (12871479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d43ac99c0d24f49bb456d2af8b2d854faab87b8148fd2d8d41bee83e43288e`  
		Last Modified: Tue, 12 Nov 2024 02:37:00 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b337462186ad41790d90217dcfb3e130e271d4ec22c5e14cccc0bdcca243e90a`  
		Last Modified: Tue, 12 Nov 2024 02:37:00 GMT  
		Size: 19.7 KB (19665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933a7aeaf1f46be65fa454e2bfeb8bba5fec90d72c07b522cea26d8348da1d2`  
		Last Modified: Tue, 12 Nov 2024 02:37:00 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a095366187dd8eb57e6496fe91c02a07921d5fc891d9bb6f0c5013ca74ec192`  
		Last Modified: Tue, 12 Nov 2024 04:00:52 GMT  
		Size: 8.7 MB (8651839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9e118516f2ecad1432a7a2b288ca37331753f7fae1f7a420726e618b47dddd`  
		Last Modified: Tue, 12 Nov 2024 04:00:52 GMT  
		Size: 1.0 MB (1031139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c381146d7a341d8a166b369a04f7827184502380f3cf61c93b0d4ac998a9e336`  
		Last Modified: Tue, 12 Nov 2024 04:00:52 GMT  
		Size: 9.6 MB (9635374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c247b900a474a0dadab3f3c95a68a2475234eba9eacce4f99e84b79a1ca1a816`  
		Last Modified: Tue, 12 Nov 2024 04:00:52 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f55595980fd4a5e776b863d14a2f221607773f262583fd043bbc765c6842588`  
		Last Modified: Tue, 12 Nov 2024 04:00:53 GMT  
		Size: 4.3 MB (4309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd7bd5494b599d976aaeecb1274f9a7f0c776839b682cc08e1854b49f195eef`  
		Last Modified: Tue, 12 Nov 2024 04:00:53 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a39dc52a3418bd12c6a84e369012c64ba7a26d2c369857930d927d4b9d92c6b`  
		Last Modified: Tue, 12 Nov 2024 04:00:53 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:e7b3b43644c48de14c809f3914759bd1b0a2ecfbc66092949d6576a2fad706e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 KB (44773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7826ba6e60186a6a9f7ff36c58866d727d57482a0da7bee6290f14c93a2028`

```dockerfile
```

-	Layers:
	-	`sha256:1a1016760ad7a281c2565711824a4c9b741409c980406bbe9a3ad2c7fa13ecaf`  
		Last Modified: Tue, 12 Nov 2024 04:00:52 GMT  
		Size: 44.8 KB (44773 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:ae7aca4a34ab29c7849cccd8215d50ced9a959632b44301d047b943e9d20985b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54848925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbb82727cb5c21bc9a125fcc5147930b6aa564a71fabaf036bb7630c74a2bb0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16a21968d13b6f074ff255ef2b1d51d6ffc6b9e377ba15f82dd5e7765cf8624`  
		Last Modified: Tue, 12 Nov 2024 04:50:28 GMT  
		Size: 12.1 MB (12147064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f713afaa52541a426ed6fe1180ad4ef20abf39c2646926e880019be65e6e5d89`  
		Last Modified: Tue, 12 Nov 2024 04:50:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bb19744dec009397af1b514a5a143743977e58f1175e5661b707c375bf9f61`  
		Last Modified: Tue, 12 Nov 2024 04:53:58 GMT  
		Size: 11.7 MB (11715395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ccf0028faf1ed60a487e074dafaadaa9e66e472cb31ecd2609f04fb72de6d`  
		Last Modified: Tue, 12 Nov 2024 04:53:57 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9feba6d3eca43f708fd7507ba296e98d3677920fd4adce2ef274ade7b215985`  
		Last Modified: Tue, 12 Nov 2024 04:53:57 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66a3eb06b8ecbbb06820fc3da4581c65832b5c633bfb77df303e98ea8e0a2be`  
		Last Modified: Tue, 12 Nov 2024 04:53:58 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5e748ca2fc3d2f33a9ba94224c6829398ef1df0399cebbbe94604a0b52d9fc`  
		Last Modified: Tue, 12 Nov 2024 16:26:09 GMT  
		Size: 8.2 MB (8201533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3323b67491ca1c2adc4b631922b426f6f19f552196974c80e576dad4e5ec72ab`  
		Last Modified: Tue, 12 Nov 2024 16:26:09 GMT  
		Size: 997.6 KB (997556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea842e26933a180eaf8328137b4e1152ca733c2d6f879b2998b94f514e4d737`  
		Last Modified: Tue, 12 Nov 2024 16:26:10 GMT  
		Size: 8.9 MB (8859397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef629560707e5748d43aa711cb02a5e469f46ac2c114140c27a983554aa0fe0`  
		Last Modified: Tue, 12 Nov 2024 16:26:09 GMT  
		Size: 648.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9563d96360a4e7ab8226df4ca7cb416ba5b9c3b87e147e15cdcc7690a71b0d06`  
		Last Modified: Tue, 12 Nov 2024 16:26:32 GMT  
		Size: 4.3 MB (4287237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc494d7c00760c3c8cae69fca29962705aa7ae117438f1cd30b59f3152b23d4a`  
		Last Modified: Tue, 12 Nov 2024 16:26:31 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c2769e4ab10218a563b78dccc8db9e21a50b97458dcf7df1b2afdf362057e8`  
		Last Modified: Tue, 12 Nov 2024 16:26:31 GMT  
		Size: 917.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:b41519c9f47f675d561fcaf98f619f91f62fe31ce631f6365b8b9e609f779574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 KB (44879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d311e9447939a3150d373e6f278b323075d9ffbd22258690941d59c3345da5`

```dockerfile
```

-	Layers:
	-	`sha256:58d1d0522dcf7c6c83cf35a59045f29cfaafeb6c448c601672dd1d9670607d4b`  
		Last Modified: Tue, 12 Nov 2024 16:26:31 GMT  
		Size: 44.9 KB (44879 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:7de1ea216658649be5799f336c80fea4f2484aa45c198020af3a43f250e8f3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52342535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2019e5bc979c8acf42efd1d190240c02d944c31077d1ef070bbcda87fac7574`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8891b9ad797d2ab4286de450552ad1b01432f19b40117a77957da9b776aef79`  
		Last Modified: Mon, 28 Oct 2024 22:51:29 GMT  
		Size: 4.9 MB (4893353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b3a40bd171b3a6ed00704448d5305b7d2f7669e004cdd18e65546b736dc82e`  
		Last Modified: Mon, 28 Oct 2024 22:51:29 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde5bf81ec482329b1688271c76052169e5a044348e29d19a69c9659d09e46e0`  
		Last Modified: Mon, 28 Oct 2024 22:51:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70944fb86567cf2ce66531adb4d9047a53b7e66ff1c8fe1ded8e5f4f62a865f4`  
		Last Modified: Tue, 29 Oct 2024 00:48:54 GMT  
		Size: 12.1 MB (12147071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbebe8652711954b61acd4bf1d4123151000c6054a172a67882fdd3fe5c46c`  
		Last Modified: Tue, 29 Oct 2024 00:48:52 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab5cd72769d63ec227242951343acf30f5bf135bf5451f32ae9f89e0ff76ca5`  
		Last Modified: Tue, 29 Oct 2024 00:52:13 GMT  
		Size: 11.0 MB (10980773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b779e44457f1ac6e9ca2d89ad8fc932ef2ed858a6f7f056a99e26643b21f3ca`  
		Last Modified: Tue, 29 Oct 2024 00:52:12 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85940ab9aa35082a97b0d903e64515c442bfbd596cdc7472decaf013517aab`  
		Last Modified: Tue, 29 Oct 2024 00:52:12 GMT  
		Size: 19.4 KB (19449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92a9ed907a7f774006699d75f22519d0bae34bb6678d3d6e872d0530b389f22`  
		Last Modified: Tue, 29 Oct 2024 00:52:13 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7da6b3d42e9c09bb5b933a1dc4f9f6b0a46b913cd27d99925706a0ce967c0f`  
		Last Modified: Tue, 29 Oct 2024 03:02:36 GMT  
		Size: 7.6 MB (7559809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031a21fadc0661db72b5a6c4466b76d0c7a7ed192c65b8941173241de244612d`  
		Last Modified: Tue, 29 Oct 2024 03:02:36 GMT  
		Size: 997.5 KB (997545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4ab60014136e27dbb5b2566c3b037ad3dca9f016b0cdb6c63b5932c63e83ac`  
		Last Modified: Tue, 29 Oct 2024 03:02:36 GMT  
		Size: 8.7 MB (8733491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869c0a2f1dd1c9b0643ac097105b7b43033dbd65da6fa3b12358081c1d054626`  
		Last Modified: Tue, 29 Oct 2024 03:02:35 GMT  
		Size: 641.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd36e657c4b418d234772d50a7d29791f2ff6c0d0270ff0b054d5d2a74899cce`  
		Last Modified: Tue, 29 Oct 2024 03:03:50 GMT  
		Size: 3.9 MB (3896875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d09544a689a8332085e5ba585fce82d0a2cdd4c6483514b2440c317791a8e1`  
		Last Modified: Tue, 29 Oct 2024 03:03:50 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d106a89257895cbd2f141534d117c4431e37becbb8770609d79342420cd54d28`  
		Last Modified: Tue, 29 Oct 2024 03:03:49 GMT  
		Size: 917.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:a1a750726c52bcfe1071c12e7b74566f9dcfbbbb94b1c9636f9d8c8882253ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 KB (44927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0491fa81a3658643eb943444c974acbe37a961788e7c7ea9c1519ea4a004281d`

```dockerfile
```

-	Layers:
	-	`sha256:f48323d08ea3ff346b57d148faebb91fb9020e6497cbf8ab2ace8ef7d446671d`  
		Last Modified: Tue, 29 Oct 2024 03:03:49 GMT  
		Size: 44.9 KB (44927 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:bbaa0bc81467c92a4536d2ab02dc30e54eda216a823ccce89a8fd0f5188c5e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59099717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73f334b99aaffbad53ca0f3648b87149f03717c216840d5172c8f216b7f88b3`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264df05ba819175767d82cc01697d7f7d371d0468273ffffb308b6b85bddcc7d`  
		Last Modified: Mon, 28 Oct 2024 22:31:50 GMT  
		Size: 6.0 MB (6044737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19693f1fe8f6d96ea9523a5fd361b05163bd3c9b0476d400db2e699e40aaa92`  
		Last Modified: Mon, 28 Oct 2024 22:31:50 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebef5cc9bae3e7065c78400102c221ef766371a514d412f543ac0fdb2cfa943`  
		Last Modified: Mon, 28 Oct 2024 22:31:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd417feaf3bffdeefd75dadf8b52fb5dff29776dc331d53f5cd12943754bb61`  
		Last Modified: Tue, 29 Oct 2024 00:26:45 GMT  
		Size: 12.1 MB (12147064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b809c2d3d6f5c42b99242804a80524bb9f5dd7941ccb1c413520af51505f27a`  
		Last Modified: Tue, 29 Oct 2024 00:26:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3acf5d05da258835cb82e874eb0e9dc91484690f62b816745e60fbbd87add9`  
		Last Modified: Tue, 29 Oct 2024 00:32:00 GMT  
		Size: 12.9 MB (12939197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c9524377b9e4f51eaa1196550ddcc467867a56f81c0c835c163b0cf6f157f3`  
		Last Modified: Tue, 29 Oct 2024 00:31:59 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5f1df733dae0f188c35e1f94cef0a3090d61501d9cf417e7a25bb91ce43f00`  
		Last Modified: Tue, 29 Oct 2024 00:32:00 GMT  
		Size: 19.4 KB (19436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3e87b5158e41bf92857c5f529fbc7bc7ee748be51165ae349b20d0aa2c2f95`  
		Last Modified: Tue, 29 Oct 2024 00:32:00 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c464cc599e6e61916445a0986200e2d23c1cc39934bfabd997d4eb8ae5200fe`  
		Last Modified: Tue, 29 Oct 2024 03:31:33 GMT  
		Size: 8.6 MB (8622502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca4bb5279d0f1f2e163fc2f35d550d1e5a03c1f150c8b38f84b3d1bc8333507`  
		Last Modified: Tue, 29 Oct 2024 03:31:33 GMT  
		Size: 960.0 KB (959966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c448a4e4b0c551bd29238e38f1044d1bf6afd0cd29e17fcd4e2afa6f4be967a`  
		Last Modified: Tue, 29 Oct 2024 03:31:33 GMT  
		Size: 9.9 MB (9909120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c16dfbcdcfccf920ef624cbf11cabab2df85ec15052fbba5fb331c20bc996b`  
		Last Modified: Tue, 29 Oct 2024 03:31:32 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04272d447dd27d055298ff2c761a5a7f9dbd20ae3d018a0f3f50876ab9d36441`  
		Last Modified: Tue, 29 Oct 2024 03:31:34 GMT  
		Size: 4.4 MB (4351356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4437ecd1acc881f2f7722e8775e2fe0d566fab71a29d0ee00668995845659`  
		Last Modified: Tue, 29 Oct 2024 03:31:34 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a77557c3770245c8ebccf078c036b9229a73eadefa8873b19197414e581c9`  
		Last Modified: Tue, 29 Oct 2024 03:31:34 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:444d63e16c891b56d1dde0ca8c6027577fe6829e00d8b485438844381dc08553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 KB (44955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b220d6ff8e8749591e97ff7303b22a6e1afedc38147250d449bed0ebfa59b43a`

```dockerfile
```

-	Layers:
	-	`sha256:f82b15ed4b91d1bbfc910f0e769b9e66b081208be21552682e3eb3369805f3d7`  
		Last Modified: Tue, 29 Oct 2024 03:31:32 GMT  
		Size: 45.0 KB (44955 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:644f093e8b2364b77d407b891262daba6d5fb029683b907122633ef9e312d027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58211361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c29bb1d4291f1d2cfd0ad47e560620af9d9bc0334c1791c635cc52fd79135ee`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db649f25283ed04e6ec39fa50ae376194ebc362ee033fece84e72a9c66354a97`  
		Last Modified: Tue, 12 Nov 2024 02:36:53 GMT  
		Size: 5.5 MB (5468338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76fbdb40d3f0602cbaed484d24d8913aecba97f23e49cc3f872f8ffabcd0c67`  
		Last Modified: Tue, 12 Nov 2024 02:36:53 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b197d513011af66d2c0a0da50f8b9b8c26b09c50d572a38a48f5b6c51b4ec`  
		Last Modified: Tue, 12 Nov 2024 02:36:53 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f582210be7cd636b2ad400eb9cf60a9538e3059aa6f1f6f41546ef7efbc86a`  
		Last Modified: Tue, 12 Nov 2024 02:36:53 GMT  
		Size: 12.1 MB (12147067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4296d14b7d7f7597f046640439626aa12d4db28903e40f512d59d9d24e51e5e9`  
		Last Modified: Tue, 12 Nov 2024 02:36:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480004561e51c4e529824cff6ab7ea67e9239cc645e018dd7f8159c7982137a9`  
		Last Modified: Tue, 12 Nov 2024 02:36:54 GMT  
		Size: 13.2 MB (13222525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b50f22b7601a195d52e923d0ed382768a1be9dcbeb4c0ba06d617b83d8572b`  
		Last Modified: Tue, 12 Nov 2024 02:36:54 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eabef9ac5e500311c2c0c2bd0086f39caba4e357d1c7f11d855a6cd63e8e775`  
		Last Modified: Tue, 12 Nov 2024 02:36:54 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43183c68ef938e9f3d742fa22cca56a340ae6bb3a5db3834208380ff4e73a2a9`  
		Last Modified: Tue, 12 Nov 2024 02:36:54 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88c9c7c62b1743ebf624277a1717ac759330f3b60d532c0eae18cb2432d01c`  
		Last Modified: Tue, 12 Nov 2024 03:10:25 GMT  
		Size: 8.8 MB (8773497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22acc66a25a80f38217ef06393ea05a6914603d74cce7b34c4b24d485154560b`  
		Last Modified: Tue, 12 Nov 2024 03:10:25 GMT  
		Size: 1.0 MB (1006394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3c0ac2d2d8e342f9ee5d0a476cda472556fc21a3afa85067c6ce174925dcee`  
		Last Modified: Tue, 12 Nov 2024 03:10:25 GMT  
		Size: 9.8 MB (9793497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8c3402d03feda52891ea69952301425d09ecc7948f7864dde2f51a755ea7c7`  
		Last Modified: Tue, 12 Nov 2024 03:10:25 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af92118788df3af167e5cb9c607acd7f6c76ba2beef9c170d07f7b17d8731824`  
		Last Modified: Tue, 12 Nov 2024 03:10:26 GMT  
		Size: 4.3 MB (4292490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b567fad130eaa2a4e5feed3970ea4776b9553d6ec609cb6c5d2c2ea6db30ea`  
		Last Modified: Tue, 12 Nov 2024 03:10:26 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701f83a1531d0276a09ba607224cd780e0ff418e390aac2891067c973540d20c`  
		Last Modified: Tue, 12 Nov 2024 03:10:26 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:45fa7ca94fec1b4c796b468335db79d2c4591cb8dc800b5a0c38a8bfba3934c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb82379f08d455c9d773cb50185bb6b08aab740db4ac58cccf13dbc5027a9bd`

```dockerfile
```

-	Layers:
	-	`sha256:962dc4c7e4abbe98cb0e72facdd20bb997fa86f46027ce603d2cb09d24242851`  
		Last Modified: Tue, 12 Nov 2024 03:10:25 GMT  
		Size: 44.7 KB (44742 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:bf4dca1d1f7075113ef25d18bf0763586d71d02648cb22b42cf3c9eac2adf5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58817958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a212ff5cf92c22160038b76f5f6605f4b65c41f99205e208eadfb77793aeb1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48f9318c9527e225b5f7831218b9775867de1e9b273f142782543bdf1aaedde`  
		Last Modified: Tue, 12 Nov 2024 06:02:25 GMT  
		Size: 12.1 MB (12147074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca9c80a35068f3abc1e0bce7e6bf34bf81702e65c62017c827f8dab16ad2ef6`  
		Last Modified: Tue, 12 Nov 2024 06:02:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaf6aea0419bcebba6a862b6562e53d2c7105816a53768ada08dde4265c4916`  
		Last Modified: Tue, 12 Nov 2024 06:05:56 GMT  
		Size: 13.4 MB (13367160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdd409830e39047ae54bfd704f53e774dccd591ad24178c8b430b810b198f14`  
		Last Modified: Tue, 12 Nov 2024 06:05:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054070b4b2c242189979f58dfbea2299397c851779be64fe3ccb9bed79cfdb32`  
		Last Modified: Tue, 12 Nov 2024 06:05:56 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4457a46ad896ef3faa76aa45be07f2cf5bf39d336dba93be5c566632c6e9c0`  
		Last Modified: Tue, 12 Nov 2024 06:05:56 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc63d9a288106f887b669d7d4574665fb4adcacb8c110f647882d463068afea`  
		Last Modified: Tue, 12 Nov 2024 16:37:28 GMT  
		Size: 9.1 MB (9129685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1cc53183e7e1c2723e33556a74549a2016a0b6b5588cace5f97870fb4e8bdc`  
		Last Modified: Tue, 12 Nov 2024 16:37:28 GMT  
		Size: 950.4 KB (950417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dc4dd85abf00f22cfa8700f08ddd2f058235413b0b3e5a7137c2a1349b64cf`  
		Last Modified: Tue, 12 Nov 2024 16:37:28 GMT  
		Size: 9.7 MB (9658843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a1a7d45c9563807ac396a73259e038cc45794c3ea8a3ed0538ff1bc2922188`  
		Last Modified: Tue, 12 Nov 2024 16:37:27 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bb52859b94f82319172288360b74c28a75636bbc45eb01abcb0622a6ab7bd4`  
		Last Modified: Tue, 12 Nov 2024 16:37:29 GMT  
		Size: 4.4 MB (4381619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7b265ab0ab227f9b1e66c26ca2d3d33baf27f92d70c3f7187a46a8906f7dc5`  
		Last Modified: Tue, 12 Nov 2024 16:37:29 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307eb80c27748e049e2cc525c34dde589c18a36b073dd51d5e2e7216922005f7`  
		Last Modified: Tue, 12 Nov 2024 16:37:29 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:c44bd857fc92e7ef595835bda3fe08b47845ac1b60579c32b7a252e81babeb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 KB (44807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2711c072be16367bedca105bb7ead6211b3c34b5442a5b200f45ac12107de2`

```dockerfile
```

-	Layers:
	-	`sha256:5e1189ca4b7ae716fe2039e6c73eeb0b5b0c27a7f8f60bb5aff4b1e5f5f26a03`  
		Last Modified: Tue, 12 Nov 2024 16:37:27 GMT  
		Size: 44.8 KB (44807 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:1a4e80f8b4ccd2c1053ff932bc14f720bff81f1245319899d33946cf75e2f1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56215165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423f8704d52591b0afa12c6816c90c95118c90099478340e6bf41c6e17275d57`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14391b845efe8f32408c641795f24e3b175713b8e7e5fee53145db363ba666da`  
		Last Modified: Mon, 28 Oct 2024 22:54:02 GMT  
		Size: 5.4 MB (5382189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd895c60b79aa63ccd3bb5c8881ca76d2d0caf2b25c46c0711b34685be1c8d`  
		Last Modified: Mon, 28 Oct 2024 22:54:01 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c40e42554f2842dd08828ceee5281acd84fad864cfff2639b39d4f6c134a146`  
		Last Modified: Mon, 28 Oct 2024 22:54:01 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3da01a311cc6223e6c9f6b3e6f92ddf83a86a61ac52153b3d531c37d3ae0a7`  
		Last Modified: Tue, 29 Oct 2024 04:08:05 GMT  
		Size: 12.1 MB (12147080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de03b526f999be1ad509003bc1d2ad712f70e044e3272c552d149dae6dd73a90`  
		Last Modified: Tue, 29 Oct 2024 04:08:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43965508bbc3b58a28058e0e90c71737074c5855c1b2f27a50d24d970fa2c6fc`  
		Last Modified: Tue, 29 Oct 2024 04:53:31 GMT  
		Size: 12.2 MB (12229961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57913cf5a4e25c37f9bc53d08da9120b19a9bac878243b1beb363c1ae4268c8`  
		Last Modified: Tue, 29 Oct 2024 04:53:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e453dfbaf3e0566f4b0ec8ed557c6caf22f47357d8a512466f9f74a2c34ad0`  
		Last Modified: Tue, 29 Oct 2024 04:53:29 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c28e1b91430795283633797d164cae11b781585d5a9e1564d40541621aa23f`  
		Last Modified: Tue, 29 Oct 2024 04:53:29 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da0db770576850639ab1800ffeeeb11e27c18df61773419b13942f59a76d37d`  
		Last Modified: Tue, 29 Oct 2024 10:53:55 GMT  
		Size: 8.6 MB (8587360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe54d40ec95045640f02418f9a88facb1095cc567b59d5cb37ee4c1d7f197fd`  
		Last Modified: Tue, 29 Oct 2024 10:53:54 GMT  
		Size: 1000.2 KB (1000223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59742cb5021dfccc37487e80e8fe4451dabbaa869b9d7f1eb983b4caa98c67e`  
		Last Modified: Tue, 29 Oct 2024 10:53:56 GMT  
		Size: 9.1 MB (9083599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da31dc6e5b28214bf19ddad91a933bbf3293df0643aad161a1718cfec16d8b3c`  
		Last Modified: Tue, 29 Oct 2024 10:53:53 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc309c1751d9caadd7dd54e2269911b384810d54ddb18ab05ccb49f38ac1dc2`  
		Last Modified: Tue, 29 Oct 2024 10:56:23 GMT  
		Size: 4.4 MB (4375148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e706054172e7445f05fad6efedcf6507a7d4104c0be4882c6a1c0420ad7f204`  
		Last Modified: Tue, 29 Oct 2024 10:56:22 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a3f197e09f4182bdc0896cbf8309cb124f7502c0d4e38826669efba3dbf503`  
		Last Modified: Tue, 29 Oct 2024 10:56:22 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:48e5f2d5eb2b46eada55cd3046dfadcec5f7f1665bbe4026808d85543eb70b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 KB (44861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c76d16b134c726986bed7630602ee11e14f23816442a4e959ed8e673375200`

```dockerfile
```

-	Layers:
	-	`sha256:cd8fbe19dc65abd3f39ad8b95f53342aa864119934686ccf6331b7875f560751`  
		Last Modified: Tue, 29 Oct 2024 10:56:21 GMT  
		Size: 44.9 KB (44861 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:c10ca1ae20a9ba25e4b40ae48482fb1a5810eab49a6e1082b1add75881d973fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57930799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3dd9d68a4335a91f716c8ccaf939e899a09c737f320f96b492bbfea2407d25`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.25
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158e1a1fd0b2858e6d2273d854776681414260488a4eacc85eb382e65b038ecd`  
		Last Modified: Mon, 28 Oct 2024 22:24:29 GMT  
		Size: 5.5 MB (5530891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12dd8b0c5e061a98a59e1b4355e05fcd6718a2721a5b5d8646d6c3142b0aea`  
		Last Modified: Mon, 28 Oct 2024 22:24:28 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eb97483a4f916d04074d8958a40ef8a540bb57479c459a219658abd26db869`  
		Last Modified: Mon, 28 Oct 2024 22:24:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f60f9ddbda9307c748838effadbccd6e13dba3f6c0b4c675222ef4a5ff7a70`  
		Last Modified: Tue, 29 Oct 2024 00:23:52 GMT  
		Size: 12.1 MB (12147071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f217c109a1da9fdc75f229b5671c27bbeb531d7c20b294858e2c99ac6ccc610`  
		Last Modified: Tue, 29 Oct 2024 00:23:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc45f7d99c5bf20c1a5b82913d6606ce3d0a0d421e4af7e0918875a5cf7b17`  
		Last Modified: Tue, 29 Oct 2024 00:23:52 GMT  
		Size: 12.8 MB (12838968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b2fb4b33faa1225cdfc603bb2e7dc164fb6f20d6ecb0ba6b9e4a66cae270e`  
		Last Modified: Tue, 29 Oct 2024 00:23:52 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e8e93d13b7e12a454a6e1e366f383de3d11205dad40183102859ff635ade99`  
		Last Modified: Tue, 29 Oct 2024 00:23:53 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6141de54289713f280396aa61a8f6419ecabda7010e87350ea536561280a2a8`  
		Last Modified: Tue, 29 Oct 2024 00:23:53 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481287f860937b0d3b4fe7edcfc98e6514062add9edb69abc42bc298590de025`  
		Last Modified: Tue, 29 Oct 2024 03:26:20 GMT  
		Size: 8.8 MB (8811195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a878dc8160713823e5e3aa5c4f6cafa7199aed225be493272fcbeb6b71285a7`  
		Last Modified: Tue, 29 Oct 2024 03:26:20 GMT  
		Size: 994.7 KB (994677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fc7a5e9ca7a5c7b9626bca9d1d20447e1dfd79097488effb6ac3a5d0907b99`  
		Last Modified: Tue, 29 Oct 2024 03:26:20 GMT  
		Size: 9.6 MB (9574207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cc01cf6a58407bdfc74094297d15928f96a41b32247079b1af99a38389e871`  
		Last Modified: Tue, 29 Oct 2024 03:26:19 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d8e6f3d9d6f9c8cf89e05c5d8027128e691770cff4cb5255d64e161acc74c9`  
		Last Modified: Tue, 29 Oct 2024 03:32:39 GMT  
		Size: 4.5 MB (4534057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369dc63f23be7f9435d39f0468e03276da34935a106819a4a2edd01b0799b74c`  
		Last Modified: Tue, 29 Oct 2024 03:32:38 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46442b888452efef2afac391701149e479f4503896f9a307832a815e15ce9672`  
		Last Modified: Tue, 29 Oct 2024 03:32:39 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:eb6fe3ed2f8e7ba67676dc80b04f45649d7ddf4820724eb0dd44b6359d0ae2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 KB (44815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358148f24e93c285179e044b19835ef6ae28eb5f5e392083ad8da6e89d3a9918`

```dockerfile
```

-	Layers:
	-	`sha256:3aa4a3005ef009d21496261be2e828f3c2fcf9f06335afa0c4dde8e7a40a6576`  
		Last Modified: Tue, 29 Oct 2024 03:32:38 GMT  
		Size: 44.8 KB (44815 bytes)  
		MIME: application/vnd.in-toto+json
