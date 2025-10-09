## `friendica:rc-fpm-alpine`

```console
$ docker pull friendica@sha256:5f957d7089d75c4195ac9aef9b92072369f31cf6d27ab182f6af954069def3e7
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
$ docker pull friendica@sha256:f4a5792a639dd171d18d7b99753bf4898e2e6990378e15dd44db0323b1f3dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57210774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cbe853d0e44d0d9572f9ecebd5f3bc708739bd2c4bce20673748b87840b27d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2f8e296f161a6df6f9e38f530b29164527358ae5a835ec9540902834c703b1`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 3.5 MB (3463764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a14574d9b443903c59a6beaf7e1bcf42b816683f83bfa06b936dbedd14d72a`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a5ec08747e2aa91406eff3773626f48070eaa9c93fed1ba8f3d7a612080daa`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014952dfec7269bd4bcc1ecd2d914b8ebce366dbd6671f3b785e004e38506af`  
		Last Modified: Wed, 08 Oct 2025 23:34:20 GMT  
		Size: 12.6 MB (12602021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fcbbc3acfaa8ce094f6a16e827c849fb2ff561b8368b8fa6c20cd3c8d9ff38`  
		Last Modified: Wed, 08 Oct 2025 23:34:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdcc22455b7b86b0da8d662df6b112a742153089b8f6c79f362a42da058012b`  
		Last Modified: Wed, 08 Oct 2025 23:34:20 GMT  
		Size: 13.3 MB (13268688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0059c8b22e0b11b909968e1478e106cea87bbe8ec16bda3d5f3604031943c9b`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a805f6317d497be1dbfa5830b80465b47ce8f844972c20bd26b7e11cfaa9aa`  
		Last Modified: Wed, 08 Oct 2025 23:34:18 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b3e1b68ffd778b41e5e1e0b9d9932bf64172edec92afd4b12f356bf61cf552`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fadf64aca9df3665d652dbdd29b5dc8ce9b4223a32bf52c862dae8ab9d5f0a`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18326bca55a020559eac075c4ef5ec8c0bba39f81e8293c39b42df23dc08f115`  
		Last Modified: Wed, 08 Oct 2025 23:40:19 GMT  
		Size: 8.8 MB (8767181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e817a7254ac14b9628f210e66f50a416f792ad093a34d19da6d9c6f0b90a9f6`  
		Last Modified: Wed, 08 Oct 2025 23:40:19 GMT  
		Size: 1.0 MB (1031298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da30c7e8d092fbc40d1dc67dc7388625098a5aa591a5ed3e839ea1d1a870c011`  
		Last Modified: Wed, 08 Oct 2025 23:40:20 GMT  
		Size: 9.8 MB (9829232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfbed37f868ef2cc291275b1f8c47ae28a08857e1775c94b8dd6936b6c9fad9`  
		Last Modified: Wed, 08 Oct 2025 23:40:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5e034e8a776bf034c901fe6e991e7b23ced076f2102a36f1cf2f1ea036dddd`  
		Last Modified: Wed, 08 Oct 2025 23:40:19 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb30b06f86e9d7aee939798ab206358bffb509025f57f5f2531e45f80d7fe6e`  
		Last Modified: Wed, 08 Oct 2025 23:40:19 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f01443c768c1f758cc6715b77e64563a6a1110f55cc308276f9cd64f521977`  
		Last Modified: Wed, 08 Oct 2025 23:40:21 GMT  
		Size: 4.4 MB (4386665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b378829bddc97cbe62c18f3219583eb635861edbd0a406f99d8b2ebb889283`  
		Last Modified: Wed, 08 Oct 2025 23:40:18 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e546a558545cdc4fe62501c20a5102d4f056880f438a5fc1e59a2abc161be4`  
		Last Modified: Wed, 08 Oct 2025 23:40:19 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:f78d8f11e29b8db78b76a49cd938523a6594cfcb0cce22bb53a48f6892c39d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3af68b0348694511b666bf69ebf4eb0f06f15ca4431d812b45f0805a94cd737`

```dockerfile
```

-	Layers:
	-	`sha256:2f779a25e6f33b0e63f23190b0d5a45f65b787c5ac1348bb211d81b764b64008`  
		Last Modified: Thu, 09 Oct 2025 02:28:05 GMT  
		Size: 55.6 KB (55554 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:0580ce145192669eceab0603541f4df056716114f8087b4910e9d0c8b15819a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54191004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8098bcaa7ae58797bdf8b02f55429d870aff7502963dfd09319acabc374ca7bd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cdcb39afd821d13b22ca21c865ff19e58569c683f9e18b9a0ceb95c92b680`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 3.4 MB (3428334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8740db6975c9b8c5220191ade53612421b7da5301d9f3f7da94286205eb5ec`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc4035a2fd0c27d5270cc96e2d8cfb3e6e50f6a5677241510df3134795ece31`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9643c46440d442a3ea77f7680b646ca563c09924e3893a139f0fae39b0fe17b2`  
		Last Modified: Wed, 08 Oct 2025 21:52:36 GMT  
		Size: 12.6 MB (12602017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fd232e2ed6ec2be8585a876afb24be002ab0ca52eaaffe0602b53ec99008a`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ebc2b7684c32e73e8386b551f89d6b67b81d3ea7bba27fdefd855628b0525`  
		Last Modified: Wed, 08 Oct 2025 21:52:35 GMT  
		Size: 12.0 MB (11983688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f744d5bcb115c5143f8a956a038bd848a40c6c1cba3a35da7cc19e2df4f1e9`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77520ca9455202004fbf3faf0048cd387a9893e8ec1d93699b3b2c83c6b93f`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf4961f2b4ef141575ff94a1fe99d95871bd0975125a7075a4e23109130d18e`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5c84b4f3a4d7577bc1b755f1ebdbecf63cf09fc3dc54d97d3e2803e4a736af`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78752f359aed5526935eaeef502f5d1c9a35b88ad4f552e6808e27aad5fef032`  
		Last Modified: Wed, 08 Oct 2025 23:04:14 GMT  
		Size: 8.3 MB (8250176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd07b3ae2c46765287f759ec0ca8af2a11305f99e4c39fe1177d0a4ff6d9818`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 997.6 KB (997634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344b103a1825b0736b5658fc7d7bc059138e22b61676eff19a83bfdbed0fe0b3`  
		Last Modified: Wed, 08 Oct 2025 23:04:13 GMT  
		Size: 9.0 MB (9023486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9311d965029dcc15a463b80dfd4bf2263b4a2b09153e6c6aa66a8b154a54f5f`  
		Last Modified: Wed, 08 Oct 2025 23:04:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f79a21b707df185aa77d39634495e93d0cd1efc4a05a2a01adcb025d162a1c`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74059eedcd25271d7dff031f1a685597ddd05250fcc74b72d8e5dc80f52b68b`  
		Last Modified: Wed, 08 Oct 2025 23:04:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f323d21e190b1395dd4f00215884e2bdb53fa2b5012ac7e972daec6aeca1721`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 4.3 MB (4342531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad3815dfddc3c196f6aaf0f1a15b061c59c054263556afc5e971af5bfa99d57`  
		Last Modified: Wed, 08 Oct 2025 23:04:13 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78f1119ba4c0eafa4ce5f229b550eb4d8d81cdc21dfb58ee636b86c3e5fdf3`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:5b69858bfca3f943e04976abaaf5f845f7279553a05e370bb468986e719ac6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1062fb79b1abc2fbb16f80a3b72ddc51539c5f59cd2567bda21c1dad23c861a5`

```dockerfile
```

-	Layers:
	-	`sha256:9a7ee8df4f17d7d79deb88d97082df847c4e06ec87ba9b8af00fb06c1d000ef2`  
		Last Modified: Wed, 08 Oct 2025 23:28:25 GMT  
		Size: 55.7 KB (55688 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:1a48dba65c9c6ddc53208b31053d1d5aed7153c387b44a4ff3b4d39ef9e53ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51907849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce68ecf5b2851889cc6c9ba454edf85578b22b32b9178d68e23574d43a96cde0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd31953efba831f10d0cb18b5b3ad75edf03f314e7bbe38c1aca633e797fb`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 3.2 MB (3244402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b71c74c2ecafb3a798b10fd0c6397ad7786a6849c4856db6dd514a2c975c4`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c7f53a180a3a248d39673c498c7ab85a1a6d5183694c33d3038f736b071339`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ae452ce63af9658d481ffccc2ad1c744f0e444c5aba07d691b2bdbb9dce03`  
		Last Modified: Wed, 08 Oct 2025 21:53:32 GMT  
		Size: 12.6 MB (12602014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafbcc1dbfaa222ffc2a08f1c645d03c40816a9ad7154fe580dc4f88638f2d3`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469404dd41d3961db5905a469aba22f0ca5a2b50cc4ef6f27a787fd8969b7299`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 11.3 MB (11290087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611eba00f6c7e0ca133eac77c4d2469a32de3c937f62d6604ff7616b2fd03b8`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4946eff1c882514c3fb48260ba445a5ea3166606dd48c64255490e71b4da599`  
		Last Modified: Wed, 08 Oct 2025 21:53:30 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800d7396291b673444e3f1ca3abee6e42f50100bbafedb89359d1bbe624fe1ef`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9da2b8b4bf4b148499be92fb2365fb19dd97a47810a0c299a0d23f148cf37b`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1086c3c61788a364640d9976e9462f4902ea063b9abef6564634606befb6699`  
		Last Modified: Thu, 09 Oct 2025 02:28:28 GMT  
		Size: 7.6 MB (7629144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd335bc80f1a8ea6196dc25ad6e11dc05e22c6d1a7fc3504182bccff8f738700`  
		Last Modified: Wed, 08 Oct 2025 23:44:02 GMT  
		Size: 997.6 KB (997598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbeee56c9e4151e0bcf5c506b14ba6b96514ee501273871406e0e693153185c`  
		Last Modified: Thu, 09 Oct 2025 01:14:28 GMT  
		Size: 8.9 MB (8915778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe0194196ce81129ac040afb2d06e01421f209b5c0d94994bafdfe75fcc9444`  
		Last Modified: Wed, 08 Oct 2025 23:44:07 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec994fb3c14897452be93f2d298d119ac4d1668fccf1763ed5d9b00f4c0c2bb`  
		Last Modified: Wed, 08 Oct 2025 23:44:09 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77c2fa249e3aa32baa8b0b8299dc3c5c135aa44b3b3aa72b0bd6160f3e689d`  
		Last Modified: Wed, 08 Oct 2025 23:44:12 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1159a0fdd24258396a550e501ad6b2b1bc6a8dca7c31adef87306dff8fc928`  
		Last Modified: Wed, 08 Oct 2025 23:44:16 GMT  
		Size: 3.9 MB (3948243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a93385ceda642750943a9411b2bc361d9f11f06f9e75d418827fc3a03390c4`  
		Last Modified: Wed, 08 Oct 2025 23:44:23 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392d24bf71af7c2b660b1f3e3a493ba961bfa98391127a810708ca4be299d12f`  
		Last Modified: Wed, 08 Oct 2025 23:44:26 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:cc243d1a37b7143cc1637af607cf34cfc3422463ef8b90453abfc20ced60c2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d8521e05cefcd662adef9ef2bb2e06eb13c67a9910f4613e145a37f5bd224d`

```dockerfile
```

-	Layers:
	-	`sha256:92afa4529bb88dc44b568fa7c9a481e4daa31fa26e8fe0f50819256c393fd345`  
		Last Modified: Thu, 09 Oct 2025 02:28:10 GMT  
		Size: 55.7 KB (55688 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:013b4e38f120eef4f7b13cc3394d3487135c9d0bf75291952b274c33ee9a695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57476752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd070b4bf5e80c93ff7c854fa50b4c80f479d24ffe8ecc483561c3c862529bb`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3e41c2bec91c6a90481f49cd9f7a03a7d1dbd5d60ce7c5743431e60b7d710`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 3.5 MB (3466806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b621ccd53774b77e761ded3f6cfa38a6c70de2968d763a229a32620219f1de9`  
		Last Modified: Wed, 08 Oct 2025 21:38:05 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9695a5b19f8045abdfdfdba80a7cb2d67c597ce00657b1b8914af7122d3ff6f`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebb674d348d7bbc3a447314380a4eb2158b7cd2e4f9bbed10e0b9ce37af4e83`  
		Last Modified: Wed, 08 Oct 2025 21:38:08 GMT  
		Size: 12.6 MB (12602011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736ac14f3ae9d84197d99b5d9ded705973d83185f0d582651f07ae3bd6dbe5ff`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54de2111690e343d01da97a959c419582524f4f27a6284397fc4a5f59dcb59`  
		Last Modified: Wed, 08 Oct 2025 21:38:07 GMT  
		Size: 13.3 MB (13252360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a18f9f6d12709e6de4dd76cdb1d4becef27de271aa590b300b3bbff216238a`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed75515c438605782fbe38189fc3ae4dc33c1571cc0e21a0037a8d15eb5661`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd0980473342d6525da82928bbf700163f81885d0f9f1cf04017cc39fffc376`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbe33dd0bd206a9b0e87239de20bf7735c0fe353b7765455c3a606f2323ed1`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4165cf00e4f9cfba385fc96640c10d5cc64bf7bb43ec291d084d20983f2947b6`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 8.6 MB (8640308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d969896ff9250883fe3928d5f0515d7b5c44571837a0c0ff057a006dd405ace`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 961.0 KB (960967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772e97c691e5dc3d9a19b3cfd18cd7a7192f6e24f1599b9dae983573e461a363`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 10.0 MB (10026303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f123ccb186ddf799ce148ec00ad4ccdee45691e084e2be3786ccadc0adbf2af`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc99954c97fed386ad8bf65a0bd4ad732fb4830f59152a328cbffe98678c82f`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1a52a4226b54f2876f0dc04e340d930ffc1b660efd95d4ec9168ac59f75b7e`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99668c9d43f3c2dea625c75ae2c712c0597635cb142ec3606cadb3b65e7fde7`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 4.3 MB (4330894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fd4851b90fa63d6ca60d25e0758212ef822803d69b06aa00d5e06c90cb54a9`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf443a266f9c3009eee42987448a0563917adbe4139d841f00ed5216cbee82b`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:31de6d1b2ec9bc6f7ace55e2f306273977c2a2bf62488c07c72dc6623541c21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2307ff873a8f83ff29e789a8c8a3d1eb436515ebb032002ec5971e96db2e3dea`

```dockerfile
```

-	Layers:
	-	`sha256:ff0be01c404f24664682622919805d208d1ec0955722c7e844c116052df0ba4e`  
		Last Modified: Wed, 08 Oct 2025 23:28:31 GMT  
		Size: 55.7 KB (55722 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:cd1487d56926550bba0525ed6474523f5cb3b72be10ecabd8c841453b01c7b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57595313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a868aa62e810b75644c15f02c9aa869c53e5bd9eeb87c2fd4b7cf05d41e013`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44e12fbc69b1f156d8436eec520233e385936119e6e0a134082ff123e16b8`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 3.5 MB (3522953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d58ed34924355103745542522524dcc6e0fbe84c3aeb4514d964f5f13593de`  
		Last Modified: Wed, 08 Oct 2025 21:29:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834a1d273fe98862d2876a4b50f8329c53bc213ac93598ead0a75cdeb2e0141f`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2c0e8a295ce017176da8f2dd0b22b2e9ad62dbade4a4899661a219fc0fb8f7`  
		Last Modified: Wed, 08 Oct 2025 22:18:01 GMT  
		Size: 12.6 MB (12601992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebff2d2e144484dbc07c92fda4ab6b679d071f3bb77c3d0efd1b8064c5bb24`  
		Last Modified: Wed, 08 Oct 2025 22:17:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d028b32894ac2aab87c098c7e23a0f05f3e95aec43114ccf54a21aa366535d8a`  
		Last Modified: Wed, 08 Oct 2025 22:18:01 GMT  
		Size: 13.6 MB (13577998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10aec0f569c9e4902cbf9d66e166dcbbbfe6b61419999b211d219048a93e2c4`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5db0495d5a7730774dcb84ad77c626fb2287541938cc40337778b70420e1aef`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aedb159c872f256a2a413e338389f972e446f639c2f297b2ae2d6b0fa13c630`  
		Last Modified: Wed, 08 Oct 2025 22:17:58 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e55aa185dcebdee08ebd308c270df822db903158cf3dfedb10187179fd12f7f`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f51caffec23d0bd758796c3860d7555a57f67e8e3618743b461738bdfc571`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 8.8 MB (8849539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3dbbe422ea489415c2c6b17435c64898fe5cb42da7ecab442042bb9db066eb`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 1.0 MB (1006304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceb53862a64f5b85f903eb61181e71c22e07c277ca88c9eb0b045bf69c7950c`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 10.0 MB (10011703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47ee3042aa855bfbbc139b6cb68d259bf83c14c84b312b76e6e4afbec2cb0b4`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ed5e66ada738711f2da447161d2029c7a19dfef4d9c55ba41325104d77feea`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff29914d99a9a8f55a937ceb37085aac4bf730225992408afac766906ee2ff9`  
		Last Modified: Wed, 08 Oct 2025 22:22:19 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d910364a93642a97abe481a2dd715a35ef7f038f1fbd4163c5d06520644c03f`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 4.3 MB (4346476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c67280f673e675dad82d17dc28aab89c69f025375bb8936358ca380fe3237`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb63f11411a7bf2e9cbc6e3e3b380c9a28fccbe1d26f73a9d71536a72f2a6c8`  
		Last Modified: Wed, 08 Oct 2025 22:22:20 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:6eff7cd2bada744e3bc080cc8bd6ba70efaf9be9025ab959e1d93a33806b201f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39cf4943065cd89ddba810f2341d524d6daf1d4e31c913b2b54c6fc5468ef8`

```dockerfile
```

-	Layers:
	-	`sha256:4be42bdc37d3007b91b072d3714ea4f11690c8eaaf5b282a9bc4c8fcdb3b8d7d`  
		Last Modified: Wed, 08 Oct 2025 23:28:34 GMT  
		Size: 55.5 KB (55527 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:9dca80b8b006720083da7031409d3f1cef69492b76d0fe0a0c12747545ce0b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58166159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e972512786d2e0e0ddafc6b3d624e54fab002dba84c5773e45da15649ac418`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0b42d58e391ad0f1f5d13bfd2403af675d228d3b129185fb0eb3df12bc8866`  
		Last Modified: Thu, 09 Oct 2025 01:39:30 GMT  
		Size: 12.6 MB (12602014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e665f371dd2830959b271d25aabbd16ef8d11adbb707c39a43673eb2057ddfd1`  
		Last Modified: Thu, 09 Oct 2025 01:39:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53022fcbac5d41db808326bcb87e5da06a60086224c11cf16f1f3ae311e1f20`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 13.7 MB (13735090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271a15d264e42e304d6cc2c5e0e2ff96c58aacd02a2af6117e82b04227fe084f`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ad3e97e677aec19e1e0e54d17cb21e34cb506ac4dd8279b8830340fdbddb9`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84967c56e95e0d072a7a114705e830de8b6468b0bfea1f3bd8e0389441f5c34`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfcd5347e9bb3a574c8a9e66143009c0949d4ee66dfd42ccad3f4c834279113`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882d2ec5553ea2444d694c1c5b04dab3ddf75fb18ebb2b05f6006c1aefe6c406`  
		Last Modified: Thu, 09 Oct 2025 06:02:35 GMT  
		Size: 9.2 MB (9199993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc4f7a4ab6168effd028fb562372f5d9b0049098a8e504d22ef7c752a192df9`  
		Last Modified: Thu, 09 Oct 2025 06:02:35 GMT  
		Size: 951.3 KB (951254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca3225b7b49dbeadd06804e91a2cd099c4b0a0d38c70a7adf1c43a42c20ea1`  
		Last Modified: Thu, 09 Oct 2025 06:02:35 GMT  
		Size: 9.8 MB (9833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fc77018c3e8b158f09f0327f15c3e08c85a92223793108a1031db061a71cd9`  
		Last Modified: Thu, 09 Oct 2025 06:02:34 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39060772abf342d17b5080bb06965d7503c515cf4211b84097435ca4147384a`  
		Last Modified: Thu, 09 Oct 2025 06:02:34 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec6dc7c5eef2cdbe602e0b68b6444e51d0bc8bfbb6bbebe83585a9112a5b03e`  
		Last Modified: Thu, 09 Oct 2025 06:02:34 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfe8f384593909f829c8b958940d7ff762fea88d0c964e450d9e8d8ca8e4b3e`  
		Last Modified: Thu, 09 Oct 2025 06:03:18 GMT  
		Size: 4.4 MB (4438760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b0a51aa777547b2479e8a4812f83e7d3b99455fc5cbe6b988a8a5edac59425`  
		Last Modified: Thu, 09 Oct 2025 06:03:18 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726fe246ee9813a8e3cfdb07d16c8517e431f6b07f12ffba4b754965b661f1e1`  
		Last Modified: Thu, 09 Oct 2025 06:03:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:2e71d59494411e3abfcac318f8d6265f08bcb2433a03cd1372123fbc256b91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27469409d563736e9bd7a6664d4c7477c42f1867712c583229c69c4e9fd16a45`

```dockerfile
```

-	Layers:
	-	`sha256:31fa0c85b41072a4b5bf4801b9413405fba7da36496ca206184b3d699e91d4f5`  
		Last Modified: Thu, 09 Oct 2025 08:27:58 GMT  
		Size: 55.6 KB (55589 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:119291118cb7e4f7431d496194ccec38285a38803c936d7dd70ded48681d1f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58345303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56450d5ca7011965784e17231767e4030802c283268c308520445eb09e84c509`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f40758817c562000fa033f5597679b300b136bc52ac8009f321d4bba962d9b3`  
		Last Modified: Sat, 27 Sep 2025 20:34:02 GMT  
		Size: 12.6 MB (12601912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2ef97e09374d14c7b37786bcdeeb71666fecc48c4b9067ecced783b2bf1c4d`  
		Last Modified: Sat, 27 Sep 2025 20:34:01 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bedc0a7e2cf95442e95fa793591cc5f31aaff286dbde4d8079962859a701b5c`  
		Last Modified: Sat, 27 Sep 2025 21:29:22 GMT  
		Size: 15.4 MB (15373339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d6e53eafaf2c23a067208c3b95f7a88dca91bd132b454c95d27d12b6944991`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f285d32a741198cec1b6611f9887f5322ef17e9ce5f2906dd925a25cb103434`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d66d9d4cb4a9ad433444fae2098bdc6cf5037aeb7c22f8cdbd6f065471e853`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d15695a95e791f746bdfd0d72e163b51f08ed4ad7ba6d07528e8c2b55dbd1fc`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ff9a4569114dd07420f8b04dc680e294fd3c587e329b94ac6664927301ee6`  
		Last Modified: Sun, 28 Sep 2025 11:30:00 GMT  
		Size: 8.5 MB (8544355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fc74c24cd7ff09c56e1b9c16b9907ec0193e65c40836775c8b1001efa23088`  
		Last Modified: Sun, 28 Sep 2025 11:29:58 GMT  
		Size: 1000.7 KB (1000657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f73dfa0d2c899208c5efac1e47766751ac23cd93fcf62e174b119262ae0fe5`  
		Last Modified: Sun, 28 Sep 2025 11:29:59 GMT  
		Size: 9.3 MB (9257656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de563395c80e602165d2c1c19998b87ed329a765117bb005cbc88660a20eb60f`  
		Last Modified: Sun, 28 Sep 2025 11:29:58 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074c36e7426d7293b763395791e4c7b909f9f387d3fb63287d1664f5a727c78`  
		Last Modified: Sun, 28 Sep 2025 11:29:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9169f9dfe321356bb18b96e09673da30d4e16c8dbaea13a6c6b43223b0aa7a4`  
		Last Modified: Sun, 28 Sep 2025 11:29:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be4785f85e85f8d9a0f919c650947bd6df86ed717970cc670dd7ec17458e120`  
		Last Modified: Sun, 28 Sep 2025 12:38:09 GMT  
		Size: 4.4 MB (4401591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f31f10d637ed23e969ec19fa3f641bd1d68d2da726d47c8204dcb8b331d0e5e`  
		Last Modified: Sun, 28 Sep 2025 12:38:08 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68565c484f1c57ff83322ddb171a5ce2ddeeca2aba7e3b8c8e267fbd806d7da0`  
		Last Modified: Sun, 28 Sep 2025 12:38:08 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:a57c06ceb7fdf4b8dad216935d13789b68fa330429100ae7f3cc9681d7d8cbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca97445330248d73776b642f1624f8556356fc02d0a673d117fe3468e991a08c`

```dockerfile
```

-	Layers:
	-	`sha256:9763f167e448305ce684c490ff2d1a4626d451f27c5318e833d47ddbb8059bee`  
		Last Modified: Sun, 28 Sep 2025 14:28:16 GMT  
		Size: 55.6 KB (55598 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:b33512b20dad5e68ce0539e255160f8f42a80a392ea845a0598277a75aae748b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60234538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27735633dbc9e5627ddfd79c892f3dad072ff48856c22b8074b37a11ccafb0f9`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2149689de406e21c39f1da3fa3d9788fda15f8300744f3cedaa8a558d9745e4c`  
		Last Modified: Sat, 27 Sep 2025 00:40:20 GMT  
		Size: 12.6 MB (12601914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17097d343a1adb55100bc03bbbdbeb0a0806e36ecbd3a26baaf26d1377d0d746`  
		Last Modified: Sat, 27 Sep 2025 00:40:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4835cd8742df784ee5ad33421fa12f372a4f78d63cea47cc03fb18f0157437`  
		Last Modified: Sat, 27 Sep 2025 00:44:14 GMT  
		Size: 16.0 MB (15978565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85153c2334bfe9fcf93b974341e5b20ca36531d01db990e1b9a7629b889bfc`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e45f0aab43e7731dc8bf87bfe21e2e61bb18edc653b39d1339d2c890c30a29`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ad6307ff0214e8fb7c417270b4ea1ff5f0678778b7518229226579eb45b736`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edabd5783f9862cf298dcd5ee3d46771273d3b06c4bb92af0c2059271805dd34`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845709fd60806cd252f402330e5346e64a9a0c3b107271563e2424d88de1244f`  
		Last Modified: Sat, 27 Sep 2025 02:23:13 GMT  
		Size: 8.9 MB (8910117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe5c47b0d73fa00cec54211012b0417351bbf40403e3c0a4fd5a98e162913a4`  
		Last Modified: Sat, 27 Sep 2025 02:23:12 GMT  
		Size: 995.3 KB (995252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c73b0cee5b655bd631b97dbb69aaae58216072a0709c80d055555b2783f603c`  
		Last Modified: Sat, 27 Sep 2025 02:23:13 GMT  
		Size: 9.8 MB (9766686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442e37d1833f9149aafdea544bd7f34f33f0254d36794871d7b7ba41638eb46`  
		Last Modified: Sat, 27 Sep 2025 02:23:12 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4e2fee534fada09eff498b5e1329365c4ab2261e0180ef49bc44c5b6bc70a1`  
		Last Modified: Sat, 27 Sep 2025 02:23:12 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459865f038386f33f61acb8a73e5ee54247209a9ca159e2460d13bd7e5e712e2`  
		Last Modified: Sat, 27 Sep 2025 02:23:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a405a23d035dd815b90175bb58811685bdbc8c1eb3ac1442ccf4978807c2bcc`  
		Last Modified: Sat, 27 Sep 2025 02:23:13 GMT  
		Size: 4.6 MB (4598365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda9ccebdbd588c5000da95974b3bf13009d4aad1fd98e65fcd81a5280466db`  
		Last Modified: Sat, 27 Sep 2025 02:23:12 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c367c3497364450bfdeefb8be02686ffed3a3375920e23ad6baea75a3a2c85`  
		Last Modified: Sat, 27 Sep 2025 02:23:12 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:344e3a8a52d5030fbda2b9f9addc3ced4d7a4e8ce6159b8b3df3b164305e7c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbc0d82bede5d0cb2e08be419c4ae0b96fadd151f7bec956315baa2bdb58ec7`

```dockerfile
```

-	Layers:
	-	`sha256:371945699a0d544323987f568b9b3a552305bd303b0f3dca1d38053942b652ec`  
		Last Modified: Sat, 27 Sep 2025 05:28:18 GMT  
		Size: 55.5 KB (55545 bytes)  
		MIME: application/vnd.in-toto+json
