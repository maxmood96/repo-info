## `friendica:dev-fpm-alpine`

```console
$ docker pull friendica@sha256:2e7c45f2c67503dc0483aded3a0836f073c41cfc353ba3b53b402d58d99308a3
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

### `friendica:dev-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:4320e1832f7a1d158162086bb8a224ad359d0c29e7fd68cc5eaf3bd6153c5c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d069afc8f557532a23cb792c908ecad48b74ab343b0fdded0ee9b60134e1ac7e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef952cbf360f9accebc7c2beaa1888046fd2decdb103e9cb37ca7fe8901e8448`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 5.9 MB (5944405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb247df7bed499a5b20b7a8f5275f005942ae29ff269444f08485852b0a82ba`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896673d396d677374e76584f6148d05009f4bf9cb800ff16ece4e2b1cf7f785`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b045c0c09a16557279905f885315501ebc707dad24429e3f76c4ba889eaea8`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 12.6 MB (12599155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c8125335db3c68c8f6abc01bbf84258e57476bb185eff879d4c1a3466b8eb`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d7dbac9207c1e11b7b23ce6aad0740e3ba427719588e966776cc44421a861`  
		Last Modified: Thu, 03 Jul 2025 23:05:44 GMT  
		Size: 13.3 MB (13261724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ac6221624b83e2f407497538d9cda65f3c6bb6028088b26532eb138997df78`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80922a9956d152b4e0a3bc8fd473151f805337d5823f8bd37b68e79cdb206f7e`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26906d4e70978b9475681f326ed2a302b23ae885e81ae8770bb41a1c51135f3c`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4226ad16511c854708eeb106b22f950a04e5db658db5aee0703cfdc687c5a9dd`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a984f63f71fe7e45cab9f387760b0f75dd5cc0aa4e5fda2bde1d13635a6dc097`  
		Last Modified: Thu, 03 Jul 2025 23:15:39 GMT  
		Size: 8.8 MB (8750895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ecda59a8b93698dc9525f45aee6880035d9d8d7eb0c7c5f22973f35e6e7435`  
		Last Modified: Thu, 03 Jul 2025 23:15:38 GMT  
		Size: 1.0 MB (1031306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b0205434dd0304b859d0d20e21597ca99168111ebe94af03e5483cb65359a`  
		Last Modified: Thu, 03 Jul 2025 23:15:38 GMT  
		Size: 9.8 MB (9822609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242e184cacc208ae47d20c55d043b6a9c2a563447fc23f8c9371993fa132f01e`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351d978fe8549f7c32a860936e64a01462f8c920221ec8b4eadce0d66cda041d`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d49e1c69fc622b5f459ee4278da8d5c6b0bb32b1e61e332644b93123488b5`  
		Last Modified: Thu, 03 Jul 2025 23:15:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c27d0c6432729bdff9e091c3c8cb15279d2e1f69aef50c1806c75a6f392a660`  
		Last Modified: Thu, 03 Jul 2025 23:15:38 GMT  
		Size: 4.4 MB (4386688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31b736f3db47e92ea06d7ae9cdc660dead3d247af19a645fdf31d7abdbe3e7`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88dfe60dbae0018a150e8593c05b8494b5e786184bbabc48d10c40450f3ad62`  
		Last Modified: Thu, 03 Jul 2025 23:15:38 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:cef3c157a0e970cecd23c5853eb648ed51c74f81aa0d44711b906da494927f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b7b05d35666ef95236700926d656324a9a31009fcec6e0b23685a3df3d6180`

```dockerfile
```

-	Layers:
	-	`sha256:9ac2ad0a33dddf98b7b53ac8f5f548c626b5bf7eb6a8dc1216e27f32740d4644`  
		Last Modified: Fri, 04 Jul 2025 02:28:57 GMT  
		Size: 55.6 KB (55567 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:a6eebef5a5a568e83c7c17fdd0ea87cccb50fbbea3d5cad638442968f808c14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57290148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1cc4847790641db71f4d61ec8ab133eb6663bbfb28c879755d6399fa94c8b0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146672ba2c374cbf86842c858594d7c0b44ab2080ad5e2ec35b1d430d956546`  
		Last Modified: Thu, 03 Jul 2025 23:34:21 GMT  
		Size: 12.6 MB (12599121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb5f1af16a6958fa9af152ac28632aff56dd315585de1020a729fb999c3dee`  
		Last Modified: Thu, 03 Jul 2025 23:34:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d236cf740ccc769ceb4ead8aa9d45e86ed16335a52d930c4fe0a9c0557f9f`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 15.1 MB (15107434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14679d7fe0b4602f2402b4899b623f618df96d2ba33280d5cf4a4afc825bb7`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7a906289e5476e4a4fbca6e72f2a28c1274a886810de274c3d9d075537bdba`  
		Last Modified: Thu, 03 Jul 2025 23:39:43 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab072a5208326c03096cd254e9205b7fd25f2fe20d9e8723ba9f85b55faab72`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a3d59f66b3f5f865439aa342092b634c80b67cc2b0976838e9806ffba9bd8`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551a5c87183be17c7f60f960c8ef68c4914d47a9e594c9bcb3c5960dd0f2a3e`  
		Last Modified: Fri, 04 Jul 2025 01:12:08 GMT  
		Size: 8.2 MB (8237733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e9a6062da498a3196d3332afd6e354347f749654929e1b862c388a31e68025`  
		Last Modified: Fri, 04 Jul 2025 01:12:07 GMT  
		Size: 997.6 KB (997640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c5cfcfd2fdd5aa531391c615065aa9b403bdd3e4b83305f37e63936f117ac0`  
		Last Modified: Fri, 04 Jul 2025 01:12:08 GMT  
		Size: 9.0 MB (9012833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7359ef65c289371a97e17a696020db5e13cfbc37058884e2e0cea92d71b2a0ba`  
		Last Modified: Fri, 04 Jul 2025 01:12:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1f5f00dec3dae799662c3dd72f980276c5737747c1bb75d4d7177570fb30a9`  
		Last Modified: Fri, 04 Jul 2025 01:12:06 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33edf8bb8013a4ff03a238618f14b79f3d64b9960361e2982c95dfcda0c2a12e`  
		Last Modified: Fri, 04 Jul 2025 01:12:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556d3bebd6cafb1b1e8d4aba9cbac6a85cfa383fa97e4e453762764e3c77f868`  
		Last Modified: Fri, 04 Jul 2025 01:12:18 GMT  
		Size: 4.3 MB (4342668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf7368718f5388c64f5f5c2779624f016a91f9f79b4675251915aabecd86105`  
		Last Modified: Wed, 25 Jun 2025 20:21:17 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071f421976208e8641c77af4ea7b9a7b08fd45d142dd4c172ede0ecb138af020`  
		Last Modified: Fri, 04 Jul 2025 01:12:17 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:4031a30b111a4aae0bd1021eaa917089b0e50defdb85f8a0d23207314f6eb846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9deb304560a356a388a58cfa342454ea4a34071d9c6b741e47b0eb180672de58`

```dockerfile
```

-	Layers:
	-	`sha256:5377f61d8bb33d3eff7617a109b3626d065d8b924aaa4ad5d0e6e176ce4f5600`  
		Last Modified: Fri, 04 Jul 2025 02:29:00 GMT  
		Size: 55.7 KB (55697 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:d7fdff51b2d00550c85c71ef61236c14a0f4e5b3606acd8fde4ba485f17d9df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54782544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a459fdd75ca07468a38f9c6e5c2dc8d7f560dc04865eb0af1c3ec07027d152`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10b98e00e904012800430f69cf8aa74332ce1ebba99fec9635378d4af95147c`  
		Last Modified: Fri, 04 Jul 2025 00:56:41 GMT  
		Size: 12.6 MB (12599135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f60ea7cbd06e3b78423de30e2481ff24a10dc4900a14d875723aad2768ad1`  
		Last Modified: Fri, 04 Jul 2025 00:56:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb773ed9018828b3805869de0c29dadb3d8afe8bbeb5822a9bff92c509f1546`  
		Last Modified: Fri, 04 Jul 2025 01:00:37 GMT  
		Size: 14.2 MB (14183204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190e2dc48065b7d79d07964079aaae471c5266f4ff8a5b4a74844f8c4ab4873`  
		Last Modified: Fri, 04 Jul 2025 01:00:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232d95fcde3e122763b3e8cf8c659f3cd57854c41b3dcfa893ff0c0154ae3cc7`  
		Last Modified: Fri, 04 Jul 2025 01:00:35 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb02f2dc6fc67eb54948f0631c60eb801811b049464f631461da3fe4d7b8b0`  
		Last Modified: Fri, 04 Jul 2025 01:00:36 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2ae500fa45bd59acbd59702482718a33f1d4d98384e11ef6d394ccf019f51a`  
		Last Modified: Fri, 04 Jul 2025 01:00:36 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90e06ec570e1ef83036b4d7f14dc0afe6ccf41135394c4fd29c2b2110a54074`  
		Last Modified: Fri, 04 Jul 2025 03:36:46 GMT  
		Size: 7.6 MB (7620724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faecc8aa890064bf7f73d3ee78fb2f8e7ea8c8427b2fb133e5e3daa6f94e2dea`  
		Last Modified: Fri, 04 Jul 2025 03:36:46 GMT  
		Size: 997.6 KB (997575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e51e0e32c2a0cbcdc6fa90fa459ba05678685363585803e82414a06c57a453`  
		Last Modified: Fri, 04 Jul 2025 03:36:46 GMT  
		Size: 8.9 MB (8907654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dc5f30b4fb0646843ee31857c149d5eb778f52eea26f4a40d58a003f9d8819`  
		Last Modified: Fri, 04 Jul 2025 03:36:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2818a44ac160c2612ebba89e7c860683ccab49c6de59197eb9dbc7a996179ab`  
		Last Modified: Fri, 04 Jul 2025 03:36:45 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f640f4c0a85bc3d59e3d22f054545ae5628c20f16e958ca9784620978af5d5b`  
		Last Modified: Fri, 04 Jul 2025 03:36:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45519a2c71da6f21e3ec9cdc22f42f8811e3886133b84762f2e936fe2935ce4c`  
		Last Modified: Fri, 04 Jul 2025 03:37:38 GMT  
		Size: 3.9 MB (3948281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0f88b735afcb9995568fe0bc8e2e6c577ea7e4bb654598a1ad35f61ae9c128`  
		Last Modified: Fri, 04 Jul 2025 03:37:37 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2431397897d79beeb820079ae995d6d1d0f15f8fcef7f619e63ad52808dfe4a8`  
		Last Modified: Fri, 04 Jul 2025 03:37:37 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:24fc5189983f5d0756ebe91e5bf8205caa4c9b0609bf0a7c3df30a5ec719141b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6a244ea0f08972567ab8dad47a75d82ccc195225cc14065030d044ce5b6fb3`

```dockerfile
```

-	Layers:
	-	`sha256:4bc25fe06dce04903e264ff2238b18547541e1f4b4d7539af6de1442cc948b06`  
		Last Modified: Fri, 04 Jul 2025 05:29:31 GMT  
		Size: 55.7 KB (55697 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:bd9a793b87f0b10f40db984f49deb31ef22a43f5d58332301ed8acac11fb3f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60212521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd39160f0265ee8905159634f3d7f17188ab5798ba4317772d5124ff0afd12a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c1dc6ad948ff6b6024c13aeb8e1504ab7c78c613d2c0c92070d4d25d125ea3`  
		Last Modified: Fri, 04 Jul 2025 00:22:31 GMT  
		Size: 12.6 MB (12599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f819ea982f77ab1a8ba8076019600ba3f9145ff91f7458fb0dcf5614950956`  
		Last Modified: Fri, 04 Jul 2025 00:22:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37d5631afd1425fe5eb2c8e749a3c65200e29d24c36d318080ca48b2cd90c53`  
		Last Modified: Fri, 04 Jul 2025 00:27:41 GMT  
		Size: 13.2 MB (13248864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934bc624a617ff8f7747e6413a288c2e89d5b658c0f017d2ea39ba3f3c409a0`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba469df90540c13439c3903a06bc064d1b88891a0ac0890503f07e7e9392d5be`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d902dfe696ab15d26a6522405d9b7fd7cc42fd2a15a790f9700e3a1b3344207`  
		Last Modified: Fri, 04 Jul 2025 00:27:40 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77b378ed1259e9def290ea50e62e695383be8cb81433a8155ef802d3ebf414`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e5fb4d320e31f5b9726141051e5cee72e679912d1e6e1cbdd388bec0d4ae8`  
		Last Modified: Fri, 04 Jul 2025 04:33:12 GMT  
		Size: 8.6 MB (8619958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c3a10eac4800266d63427083683c54ec3882bc8bde159a0a9bd024175df0f`  
		Last Modified: Fri, 04 Jul 2025 04:33:10 GMT  
		Size: 961.1 KB (961067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584c1dd4bf906cfb539db8314742a86686da4ef507e62f570096898b0332235`  
		Last Modified: Fri, 04 Jul 2025 04:33:11 GMT  
		Size: 10.0 MB (10025305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a74474fec7fad45f0f1632ebaf5b0d350935cdeaa51961dadcf25aea76abadf`  
		Last Modified: Fri, 04 Jul 2025 04:33:09 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a851d452fc09121e692fc48da1b5881b7470f30231ee00439ccc5f6341667e`  
		Last Modified: Fri, 04 Jul 2025 04:33:10 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac4f14025f8d4670eb5b1bfff40a1d48e3bb4f618aeebc5e9599814498de42f`  
		Last Modified: Fri, 04 Jul 2025 04:33:10 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc09d6e6728a2295ff359689ff12c058e9d976e62b36ac1ab475d4fa5549e6f`  
		Last Modified: Fri, 04 Jul 2025 04:33:10 GMT  
		Size: 4.3 MB (4331017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f33e90baa8b1972f41c5ffd1bc3a5dea1f885e6c4bafc9d00fdaa9c2d8f3d`  
		Last Modified: Fri, 04 Jul 2025 04:33:09 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767024ebfc66107af3a817553240f9ea94a3a2f22d30d2cd69fb83a9fb26eede`  
		Last Modified: Fri, 04 Jul 2025 04:33:09 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:fde434497c6992e08757dfbb68048781e0c081c955b8c6b8fffbd939e5d7cb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb4850cda86c5629140f057e3986fe5a7abef25d63e39c6ada4c7d3c0ec05d8`

```dockerfile
```

-	Layers:
	-	`sha256:20b40b81379eaeff3a95d45f9f86186095f8fe79a05411eeb579e5db94dc295c`  
		Last Modified: Fri, 04 Jul 2025 05:29:35 GMT  
		Size: 55.7 KB (55736 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:44d45a94d45f2544ca615a8f38c82aa284382bbbc0e0e6360d6491126b4ebde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59854831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1ce7300adf6f6f4d557e68bbc0875654c5848feb9901d08a557f50691019b9`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807332f552a5d43d50bf321942aaff6f62a51ea718c4bc5c92889c7da5518cc`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 5.8 MB (5806969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5952ed3b34bc2bb95e5d92041b0d1e2f1102370e20445fde4e6ae170753fd54f`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26cd4edff9c58bc8c1207c850646d9dfdfc9668c692e2b02ccedbcd463e458`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b172088b57748f502c5aa1cb684e21421b0497fea01813cd1a37fc90acd2`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 12.6 MB (12599126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0cd325f2b5b783c7b8a674f750116f3312bd602ddc978c5b9f679705430ed`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a1d58746e581f9623e1af350bf3217a46d1bf2421a049c667ce7611ed9234`  
		Last Modified: Thu, 03 Jul 2025 23:05:47 GMT  
		Size: 13.6 MB (13572591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86069b8c031ffbd54f99dcbf2ae53e9e0957fc9842ceeaa4a5c8036b2f82643`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aef072b2e721a30c9933cc7e4efd20c954bbd7be2cf4635995276b751a09425`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b7b0119a26af8eff640f542e3e4ca243bddb6c7bffcb62f9018e53e27a28d`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bce8958e293647dbc8485a223c57de84e18b7d627799a89f7217e466b8dc86`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d7f31485b2c4021fec0e78fa999da90d76bc2dacd93640524e27f86f1ed83`  
		Last Modified: Thu, 03 Jul 2025 23:15:53 GMT  
		Size: 8.8 MB (8845811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f697e8afe6b66e67e5d2f8a0fbbdfcd36a71736044f22be2a6a8ae66d82f8275`  
		Last Modified: Thu, 03 Jul 2025 23:15:52 GMT  
		Size: 1.0 MB (1006237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdf61239834b0c732933e46e4d7136eb2c84dfc2373aa459f536d65b15f34ce`  
		Last Modified: Thu, 03 Jul 2025 23:15:53 GMT  
		Size: 10.0 MB (10001809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6805d7598c4a2b5f639c62d740d2cf2034a12c8cf0996665fe1dbe6252578b`  
		Last Modified: Thu, 03 Jul 2025 23:15:51 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84f2afd4020cffb3b3f787fa0598c54b3f1d0a6cf1da42bb99cec3fbccbe61b`  
		Last Modified: Thu, 03 Jul 2025 23:15:51 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d49e1c69fc622b5f459ee4278da8d5c6b0bb32b1e61e332644b93123488b5`  
		Last Modified: Thu, 03 Jul 2025 23:15:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d2fe70cfd27a689f4a81c3648f76d3f001d7e48653ca70eceb530c932852f`  
		Last Modified: Thu, 03 Jul 2025 23:15:55 GMT  
		Size: 4.3 MB (4346561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fe1f75dbea8d63f8a0f59a4301e6b84ae0c87474beb9ef4f4b067a1055ca64`  
		Last Modified: Thu, 03 Jul 2025 23:15:54 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786b1bd44e7a83c07af77030ccbb971152239a1293d23cd406a6d32b71535ca`  
		Last Modified: Thu, 03 Jul 2025 23:15:54 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:4c5c573ba1adc6c6ad81b28b8d87f9f482a2bb3228d601516f9d49acd504a3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f2c70d31ecb6da2b75049c6ba93c46246c430c4b82e0db21bbbfcc66466d99`

```dockerfile
```

-	Layers:
	-	`sha256:379c03431670a2c7641688ad67185502a6d8c4ac17b5b5e2652b5b0c8101d6f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:11 GMT  
		Size: 55.5 KB (55540 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:255415f6230c123cfcca6bd515402941dbda5e3cc97e5b68c58756877ed7da8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60476360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf752f0a83c9ef014683bee51e0456927bf803593d8fe5bfa9659c0cbf20387`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daa18a322ff81fffc7ceb1c57d422d1adf54055433564c7dc442f903760a8f1`  
		Last Modified: Thu, 03 Jul 2025 23:54:52 GMT  
		Size: 12.6 MB (12599136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3f6203202b10d68495a456bb29733beccaa33785d2412fb041f620278679d`  
		Last Modified: Thu, 03 Jul 2025 23:54:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e866d6eb8c3a035680c0d3efabfbca205989bcd4bee91b8a71c55a705ce9184`  
		Last Modified: Thu, 03 Jul 2025 23:58:30 GMT  
		Size: 13.7 MB (13732933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531b83a89125d0ee7a5f425580e0142fe836b2078ec7b9b0a04717c2d8c675b6`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316ae9dff514804b8e62c75c316fc9f7a2a98cdcf43b08a879887c8865e8d2`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 20.0 KB (20007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068cb2008a5c83784fe82cf109b583e810ad10f6cf9461dba75b4bc3693fdfd`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3a1077df05c4646ceddd1e7ac63a985083bf3e92537bbb928a3367fb9045a`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cf4c26990b5ec970c7d5b4ed21346cbe78dfd89dee5fb5626d9f201f8326ba`  
		Last Modified: Fri, 04 Jul 2025 03:00:38 GMT  
		Size: 9.2 MB (9195016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a89abc995ed6cf41ad82427623bf2b9eb1a704222ae1c0c8dd780e2e3489d8`  
		Last Modified: Fri, 04 Jul 2025 03:00:38 GMT  
		Size: 951.4 KB (951352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1f06b795ea167eff452870b10d61f5319821a10dc721afe0b0784976042ff7`  
		Last Modified: Fri, 04 Jul 2025 03:00:38 GMT  
		Size: 9.8 MB (9822708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c302ef54172765332601d4666dd5aa981685bde862762aec7996e01cbbeea193`  
		Last Modified: Fri, 04 Jul 2025 03:00:37 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c199134899315fa15b69bc9f3eddc5ea9ac1729ae4df44806c9130fdf4bc0469`  
		Last Modified: Fri, 04 Jul 2025 03:00:37 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a7d6f825aeaadc46c5aac603caa60a523ca2a1f34886ced74acbf520d1e74a`  
		Last Modified: Fri, 04 Jul 2025 03:00:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac70283275d62b03a88ea97f47eed8045b514e1d3bd2643e9b635927a23ea390`  
		Last Modified: Fri, 04 Jul 2025 03:00:38 GMT  
		Size: 4.4 MB (4438765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef804d1e2c4b6abc79f06a475b8cafabe0d5d212fdde988570d9bc5af9cea8f`  
		Last Modified: Fri, 04 Jul 2025 03:00:37 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89ce99f78d4c627179c9e5cc029e856a7901c5d65ae669cec6b99609a4d29e9`  
		Last Modified: Fri, 04 Jul 2025 03:00:37 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:640deb2bb51a6c5efef3c985f572210ce81809fb0795a5accf06a79871ff99a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7b152606e16c9bee6d91ee29d93f2dd13846236407035d16dfd46248d75f2b`

```dockerfile
```

-	Layers:
	-	`sha256:0ef096cfc541e4b3855528f3206aaea29b03fc0054f5bea07572cdacb3049187`  
		Last Modified: Fri, 04 Jul 2025 05:29:40 GMT  
		Size: 55.6 KB (55602 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:d18347bc2ae7075b580c1b7faa9be9a35ae53668e08e2fb9cf31bde4a5975084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55707621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4ce394f46296343ec844ab62b5d7ffb812cd3ba3918206d843ac4248a1379a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.22
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5cafa4d9818b0979221ee32a634774fa7f630af34e28dcd203e49994f474f`  
		Last Modified: Wed, 11 Jun 2025 08:15:56 GMT  
		Size: 12.6 MB (12576232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27333500b47fd459f2d6ae7fe8c9965e6a2e171e3413cd3721da70944d32400f`  
		Last Modified: Wed, 11 Jun 2025 05:27:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94ea32cb34db450a708bccf88f34888f12a69e81197c5e562becd545f55c0e`  
		Last Modified: Wed, 11 Jun 2025 08:16:04 GMT  
		Size: 12.8 MB (12758742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5d92b246a6d60b990cacf09bb2fcc12451ac7c1b17f7396ba16c682667c7f`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91e11dba2e3d8f6f7071f2936da54d2416010d1a7ee5417246d3253bf6623e1`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8195a02efbcbc128ec081a88ee47bec8eef940c0795b5cbc4df768899a7937`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a159d59982da6923f201118958fe2300484b8b87fc234f3931bd53e5ada97eb`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b2d539f425f897748387cfa4001c1404a32806fbe0e9482da3606c50de4e2`  
		Last Modified: Thu, 26 Jun 2025 11:27:53 GMT  
		Size: 8.5 MB (8541740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350b572f9349450a8bef714d9f4d488ec7482da5d90845211b514adcb2c22aa`  
		Last Modified: Thu, 26 Jun 2025 09:15:14 GMT  
		Size: 1000.8 KB (1000807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca25561db356fff2f9b5cda71291ae18c23b40f156f02ffecbac4ca19eb82665`  
		Last Modified: Thu, 26 Jun 2025 11:27:53 GMT  
		Size: 9.3 MB (9251530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae7384f571279f348568097838156d91107ca6b23fd93eaf173bbdc77ff3c7a`  
		Last Modified: Thu, 26 Jun 2025 09:15:17 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f5434d07759ad3908f8eb0fefcf5d35c97e7d213284ed8aee21953e124d693`  
		Last Modified: Thu, 26 Jun 2025 09:15:29 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60999ab7af04461dc52b7f7d3c2d37431187b6a07611c96377cf37e21e2926c0`  
		Last Modified: Thu, 26 Jun 2025 09:15:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68c8b8a8ea17583e257a9126b2e3516258fbc886306f8d5ef8b7cd297320ed3`  
		Last Modified: Thu, 26 Jun 2025 09:09:28 GMT  
		Size: 4.4 MB (4402057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8064cc85092052567cf38be4756782e121f9c2f8e107db1938bfbbc0e820d9b8`  
		Last Modified: Thu, 26 Jun 2025 09:09:27 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713063dedd4037bd68711b6dbe2ca9863c977760fb873e15c517eb29c0e17d9c`  
		Last Modified: Thu, 26 Jun 2025 09:09:28 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:b41406d95509f2228e1def2e1405b2c16f61c5f3e974641f7afdb3026eca1afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e3921831463241cf289473e795f3ed93305a645f5844a6556c1af708f30b3a`

```dockerfile
```

-	Layers:
	-	`sha256:f779a018cabfd26a9b4717521b56965ac07a8e2347c60b973581d23c31a1e027`  
		Last Modified: Thu, 26 Jun 2025 11:27:48 GMT  
		Size: 55.6 KB (55611 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:d61511d85f2a5567e9b56912dff2b50629d623480d9fa1748eeed842c6e192b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59713152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b3738a3ec2f378647af3b4e55a4046e2c6fb2ec2ef16358afed75ab3dd8a0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Apr 2025 16:08:36 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Apr 2025 16:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_VERSION=8.3.23
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Apr 2025 16:08:36 GMT
WORKDIR /var/www/html
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Apr 2025 16:08:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/html]
# Thu, 17 Apr 2025 16:08:36 GMT
VOLUME [/var/www/data]
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416dc488e82ac5d95b592019f37aa9b64fdb6535ead41862f2acaa1677ad8e8e`  
		Last Modified: Thu, 03 Jul 2025 23:57:30 GMT  
		Size: 12.6 MB (12599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ba56106dd7084cdbb4d9ab2d30f1b097ce958de942d3197fc708ee1f3e636a`  
		Last Modified: Thu, 03 Jul 2025 23:57:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25d63e1e4d6962369161cd89600b93f34b435063aad41926a421597342eb6e9`  
		Last Modified: Fri, 04 Jul 2025 00:01:25 GMT  
		Size: 13.2 MB (13210606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56deef95c718f1fbe14547d0fcd0e8682120447b39ddcddabbcf51078ea78e27`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4071eca4de4ffe44b642f2d9e429cfb38ffed2ba8f05c01b05987bd9e09168`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b47a68df718bf2a7d4445bdade317550e020b85d2aa4a94525ae1ad4b31a8`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13964924a7e5d79c0c083de7d22047114b2d6303f4218c86261b01153e6269f`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff89084f5488a9db3f5ae086640ee30a8b139a8673ee692206f9f77637d80a4`  
		Last Modified: Fri, 04 Jul 2025 02:24:44 GMT  
		Size: 8.9 MB (8909946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab3b71575ae9d5a44367e94242d044b30e7edc8e9b1f25bad415a195ec5000d`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 995.5 KB (995542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf3d61792cf0f9edf0f2db02f9d2d744b6e87f9dfc8c70e8996587b4aa6ccfb`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 9.8 MB (9759649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2c7451efbe17d1eb7a4a234802b958abd4b127302599dc17a4f0c61ae0031`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc73bff154c5e645d976c49f34ced9d4cde2ac51c31ae468bed2d832c5c8755`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e3449b635065859a6faa1b7c2c5dfdb4220a85c8cba6f74ca5eca2ed62b388`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23e4b6d8899590dac69a2cd8b439489cdf5319df38c334a1afa406bb55e41`  
		Last Modified: Fri, 04 Jul 2025 02:24:44 GMT  
		Size: 4.6 MB (4598855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7286fd5b886506e5ad3153b47bb5191f59e83a47ab9dbe80b758edb3fd69964`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49045fb5ec43703dc360d14468d4ba8e066e4dbc49225c965a23f558b2cbc6b7`  
		Last Modified: Fri, 04 Jul 2025 02:24:43 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:cdb20471d481c1b307217493b03b6937ca05197b31e1a96ebe130f3253ecc1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf113d4c8e87108fe578ac6909c9b53daa7c06e34c3cc5c9de675f07b9512d3`

```dockerfile
```

-	Layers:
	-	`sha256:41413b5da08a851e2a312b355f0449a8f3b0573d73a03c532451e027010e8039`  
		Last Modified: Fri, 04 Jul 2025 05:29:45 GMT  
		Size: 55.6 KB (55559 bytes)  
		MIME: application/vnd.in-toto+json
