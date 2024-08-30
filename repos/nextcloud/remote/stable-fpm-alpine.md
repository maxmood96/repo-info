## `nextcloud:stable-fpm-alpine`

```console
$ docker pull nextcloud@sha256:7a5ac2e89f4299b3c7c36a29b3136c61204df4532c532bcf05698e13870b10d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `nextcloud:stable-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:034ec2f332553595a3ac7bda23e91ed51d0174a7016fb14641edfc82aa44b2e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303349403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46c1f7fda4bde58e64c3415ecf8ca45309076dec8fa6cde2b9395d53d9a6b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:21:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 23 Jul 2024 01:21:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 23 Jul 2024 01:21:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 23 Jul 2024 01:21:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 01:21:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 01:21:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 01:21:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 01:21:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 02:37:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 21:56:23 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 21:56:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 21:56:24 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 21:56:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 21:56:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:04:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 22:04:27 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:04:28 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 22:04:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 22:04:28 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 22:04:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 22:04:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 22:04:29 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 22:04:29 GMT
CMD ["php-fpm"]
# Thu, 01 Aug 2024 23:30:58 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 01 Aug 2024 23:33:58 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Thu, 01 Aug 2024 23:33:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 01 Aug 2024 23:33:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 01 Aug 2024 23:33:59 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 01 Aug 2024 23:33:59 GMT
VOLUME [/var/www/html]
# Wed, 21 Aug 2024 17:36:04 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Wed, 21 Aug 2024 17:37:06 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Wed, 21 Aug 2024 17:37:09 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Wed, 21 Aug 2024 17:37:09 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Wed, 21 Aug 2024 17:37:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Aug 2024 17:37:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae0d9dfc4dada15e6a030ba7b9c9a3b16f9f5a7597a4d46ff24226e91b91db7`  
		Last Modified: Tue, 23 Jul 2024 03:55:04 GMT  
		Size: 3.3 MB (3272601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce295ca8623e5dc914104e970c5496db996db5f2abb336389bcbadd10465d21d`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3eb99f3c122bc8d6c22107602ed9c22fce771289b54bb2598142d1626f693`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca219f0486d17775ac640649d34f40f15cd04f0915086eb25299aa36448c83d0`  
		Last Modified: Thu, 01 Aug 2024 22:26:12 GMT  
		Size: 12.1 MB (12120810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e5f41964d3750eb928c1bf3ca13c886c78bce9122b80fe564e104f8a2fd527`  
		Last Modified: Thu, 01 Aug 2024 22:26:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa92ff570db6ee8544f2b105e5355f8100ce5fd4481071bf8661d3b728b52af`  
		Last Modified: Thu, 01 Aug 2024 22:26:38 GMT  
		Size: 13.3 MB (13328853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9a0cede3246ce708db7365698a9006db0aa601407f0662f5ec48522176cef2`  
		Last Modified: Thu, 01 Aug 2024 22:26:33 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcb9e907bc11fbd7ec07deacea75e2a0c049c784c3ffda59427a2339ee5abba`  
		Last Modified: Thu, 01 Aug 2024 22:26:33 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f020807e5e161d8e38981df307228b448898102b5bfada92671fc05321b949`  
		Last Modified: Thu, 01 Aug 2024 22:26:33 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923a617995d0c15d8fd9c26965ea76f2e2ab3dcb16c964b8e8a7fff88779e4f9`  
		Last Modified: Thu, 01 Aug 2024 23:43:19 GMT  
		Size: 43.1 MB (43067140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d033c55d8e8100b07db0cb8df5414ae7599b7e741359b93b71842a74a765fb69`  
		Last Modified: Thu, 01 Aug 2024 23:43:13 GMT  
		Size: 7.3 MB (7346416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d83c1d6b1c3fd352245b51a128f48daf76249a56618208e7130a8e5dab8a7`  
		Last Modified: Thu, 01 Aug 2024 23:43:11 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db130757beb3c150b0c7d079a0d28338646bde1415fcc16de399582cf060965`  
		Last Modified: Wed, 21 Aug 2024 17:41:40 GMT  
		Size: 220.6 MB (220550798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007d9469814f4b852954bc3fe4bb6c68808311f9cd56abdda8c2cea43fb518fb`  
		Last Modified: Wed, 21 Aug 2024 17:41:14 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3534dd302eae8908eefff0b365396dc150d1e938d046bb1daa7e271aefe6422`  
		Last Modified: Wed, 21 Aug 2024 17:41:14 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:b8e187fc5a7364b517d0a3d233f37fe3b835cc3d4e72c0a979cf53bd34c9290e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295429712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a584019439c9051593abcaf9f6f32068e2c0e8cba5c3e2c3c434be12bd1863c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:39:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Aug 2024 19:47:57 GMT
ENV PHP_VERSION=8.2.23
# Fri, 30 Aug 2024 19:47:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Fri, 30 Aug 2024 19:47:57 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Fri, 30 Aug 2024 19:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:48:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:57:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 19:57:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:57:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 19:57:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 19:57:25 GMT
WORKDIR /var/www/html
# Fri, 30 Aug 2024 19:57:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 30 Aug 2024 19:57:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Aug 2024 19:57:27 GMT
EXPOSE 9000
# Fri, 30 Aug 2024 19:57:27 GMT
CMD ["php-fpm"]
# Fri, 30 Aug 2024 21:07:27 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 30 Aug 2024 21:10:26 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 30 Aug 2024 21:10:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Aug 2024 21:10:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Aug 2024 21:10:27 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 30 Aug 2024 21:10:27 GMT
VOLUME [/var/www/html]
# Fri, 30 Aug 2024 21:11:43 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Fri, 30 Aug 2024 21:12:50 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 21:12:55 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Fri, 30 Aug 2024 21:12:56 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Fri, 30 Aug 2024 21:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 21:12:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b73c0725ffa83a6f37cb6278d75c3f071ce0c07a7e252857342e986871d461`  
		Last Modified: Fri, 30 Aug 2024 20:22:43 GMT  
		Size: 12.1 MB (12139341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6016697711a53cfe675a8fab3cd72090ff9b60296789328195ffab253fd58cb6`  
		Last Modified: Fri, 30 Aug 2024 20:22:42 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11572704dce17bc6dd7af07fcbde24f81d060bf98a69852bcc69d277f57335f7`  
		Last Modified: Fri, 30 Aug 2024 20:23:12 GMT  
		Size: 12.4 MB (12353082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251d60b8a75c81dab55dfd2ecc518e2982f5a5dc0f671c20188341309c1c4d91`  
		Last Modified: Fri, 30 Aug 2024 20:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95c423810c6aecfc5d6a9f280b157763f8cf9dd1a06ff9e1f47062c788811f8`  
		Last Modified: Fri, 30 Aug 2024 20:23:09 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e9a47f8f6ba1274af66987658efbbf78740c878a3a1ecd565f4955d1288841`  
		Last Modified: Fri, 30 Aug 2024 20:23:09 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e91390f9643688849b97cf6542d92459abc1c7c0fc8d7f6164d669a0ceb45`  
		Last Modified: Fri, 30 Aug 2024 21:13:23 GMT  
		Size: 37.0 MB (37011781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f3168bd7c8f9e3bddb79d394b9febf1433257af8eb940954ab21af5ba6c39`  
		Last Modified: Fri, 30 Aug 2024 21:13:15 GMT  
		Size: 6.7 MB (6706198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f2688aecd8d8854de093ab93e93fa510b1e62731a50a7cfe091f949eec818`  
		Last Modified: Fri, 30 Aug 2024 21:13:13 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d0002c48c959b2f73b2ef9274c780d390d75cab6c86275ccb9ab3794a24ff4`  
		Last Modified: Fri, 30 Aug 2024 21:14:36 GMT  
		Size: 220.6 MB (220550787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf8bcac625cbe9b5314fa7a13b674d54bfefd4668e70c3ef90543da4679e7f8`  
		Last Modified: Fri, 30 Aug 2024 21:14:02 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b24dd50238d2678bef30ec0447162c30846da3f5939af35923e7f1c1413267d`  
		Last Modified: Fri, 30 Aug 2024 21:14:02 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:f06a73ddf59004be21a8957f3f49e6ce787d56821db9af6e8dbb64dbe74335c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (292968936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c067e3afc0c4d4afd2675c056dee8c42be18631a1632ec36e4bad1da830491`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:31:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:31:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:31:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:55:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 22:22:10 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 22:22:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 22:22:10 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 22:22:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 22:22:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:29:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 22:29:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:29:09 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 22:29:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 22:29:10 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 22:29:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 22:29:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 22:29:11 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 22:29:11 GMT
CMD ["php-fpm"]
# Fri, 02 Aug 2024 00:00:42 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 02 Aug 2024 00:03:18 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 02 Aug 2024 00:03:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 02 Aug 2024 00:03:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 02 Aug 2024 00:03:19 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 02 Aug 2024 00:03:19 GMT
VOLUME [/var/www/html]
# Wed, 21 Aug 2024 17:19:28 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Wed, 21 Aug 2024 17:20:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Wed, 21 Aug 2024 17:20:28 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Wed, 21 Aug 2024 17:20:29 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Wed, 21 Aug 2024 17:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Aug 2024 17:20:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180cacd553caf3105e2789da4e96b6baf6c08c56bc611414731c44b274a4a0bc`  
		Last Modified: Thu, 01 Aug 2024 22:47:21 GMT  
		Size: 12.1 MB (12120811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d072216e350e288ce6ae22b78c5e5c16625582cfbc6c595e467e413fda580bf4`  
		Last Modified: Thu, 01 Aug 2024 22:47:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4386b01c59f3b65dd0e40be63e7cab161b888470a10f952e1b8f8f7e6da87168`  
		Last Modified: Thu, 01 Aug 2024 22:47:44 GMT  
		Size: 11.4 MB (11402641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31443b9505643672cb6993dacb497e3e2fbd3dbc9386c404c413c96dcae2aac9`  
		Last Modified: Thu, 01 Aug 2024 22:47:42 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d76958aee596e88de26363a2088f0297b97ad374e1d70c774cb20257001ce39`  
		Last Modified: Thu, 01 Aug 2024 22:47:42 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386d07e6df4c914defb485785b5c5d459815570afba6050393742c674642b6fb`  
		Last Modified: Thu, 01 Aug 2024 22:47:42 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7d7407e9b93436f9ab9fefbad9f237ff028d46bde74a446374c62838b5d7a`  
		Last Modified: Fri, 02 Aug 2024 00:14:37 GMT  
		Size: 36.0 MB (36013265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ec398cbaf4fa978a213d75d6eed646ef2c479074796b045d83d151457bb4ef`  
		Last Modified: Fri, 02 Aug 2024 00:14:31 GMT  
		Size: 6.7 MB (6673875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f15355aafa385092ef129ed2b5711e4f373f1d623c04aa0d8a23d0e5e3e3a56`  
		Last Modified: Fri, 02 Aug 2024 00:14:29 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae9626b26f69fea1f0e762f80bd80e5a5ef30ccf4776d2236a562f567bfade4`  
		Last Modified: Wed, 21 Aug 2024 17:26:14 GMT  
		Size: 220.6 MB (220550590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90eaac919d4ec7f4fa6a32c5d10e138ecb55f63129eef611704603a7bd1b30`  
		Last Modified: Wed, 21 Aug 2024 17:25:42 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a27301a53a4bcd8f3eb9f6cf19764137c255c103c7f4ee549159d89a06715a`  
		Last Modified: Wed, 21 Aug 2024 17:25:42 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:f76ba3bdf006d8a2d54b7fc5d1653657cc2ca0f27b4bcf96fc68fb2a9c35eed4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305136195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71838b6381892c311e6c38aab95c23fba9075b4f7043a1ef28dc0be50fd4ea09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:30:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 23:30:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 23:30:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 23:30:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 00:43:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Aug 2024 20:50:00 GMT
ENV PHP_VERSION=8.2.23
# Fri, 30 Aug 2024 20:50:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Fri, 30 Aug 2024 20:50:01 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Fri, 30 Aug 2024 20:50:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:50:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:58:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:58:04 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:58:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:58:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:58:05 GMT
WORKDIR /var/www/html
# Fri, 30 Aug 2024 20:58:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 30 Aug 2024 20:58:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Aug 2024 20:58:06 GMT
EXPOSE 9000
# Fri, 30 Aug 2024 20:58:06 GMT
CMD ["php-fpm"]
# Fri, 30 Aug 2024 23:08:56 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 30 Aug 2024 23:12:15 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 30 Aug 2024 23:12:15 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Aug 2024 23:12:15 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Aug 2024 23:12:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 30 Aug 2024 23:12:16 GMT
VOLUME [/var/www/html]
# Fri, 30 Aug 2024 23:15:34 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Fri, 30 Aug 2024 23:16:22 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 23:16:27 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Fri, 30 Aug 2024 23:16:27 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Fri, 30 Aug 2024 23:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 23:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67b7b2cc1dee7c76c722fd018bbe36b766d85539a4118bc3c7c10d0bbe0a680`  
		Last Modified: Fri, 30 Aug 2024 21:27:37 GMT  
		Size: 12.1 MB (12139345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cc075d1a6b04bc77e38c320dea3a41993741d04426d7a020dbf4bf14bf759`  
		Last Modified: Fri, 30 Aug 2024 21:27:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3104ba9a03794c5af4056b3a62a2d1efff327c6854764cd344fd6be1c662d524`  
		Last Modified: Fri, 30 Aug 2024 21:28:08 GMT  
		Size: 13.6 MB (13597679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9f53f55f203455f555fb5a7c849f4d0fcbdadceebc80c7e962605b2700062f`  
		Last Modified: Fri, 30 Aug 2024 21:28:07 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b586ae5d02f4940f37595e15daa8a75dc5d6e24eb8dad3a401632d5eda4222c7`  
		Last Modified: Fri, 30 Aug 2024 21:28:03 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f40b4d1e56e8912b965fe6592593fa9fa638429e0d738b0fe2edb6aa0da8ae`  
		Last Modified: Fri, 30 Aug 2024 21:28:03 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42edf28ba6a1daf541a205e54bb119f41b417ad02051b63121a78a3bf0229a3`  
		Last Modified: Fri, 30 Aug 2024 23:18:07 GMT  
		Size: 43.8 MB (43769591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b217bd20fb9acb78be3b4979b7f192591a4b3cdc56dd370c984b0116d4333c`  
		Last Modified: Fri, 30 Aug 2024 23:18:01 GMT  
		Size: 7.6 MB (7627372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ee847275df29718fdd5d5950fd43b7af24257045ebd7fdb876688548d7a980`  
		Last Modified: Fri, 30 Aug 2024 23:18:00 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dbb63dbea5023c11f0a279cd28cc79f7eeb6628b35baf3ee19377f01e130d6`  
		Last Modified: Fri, 30 Aug 2024 23:20:26 GMT  
		Size: 220.6 MB (220550873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9cf55880a950454ab398490fa08cd0546bf7cd10536065d36f4d32ec61207`  
		Last Modified: Fri, 30 Aug 2024 23:20:05 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3b896794133a5659338a24acd5c082b3d8bccb3b908df63773f063d5fc3755`  
		Last Modified: Fri, 30 Aug 2024 23:20:05 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:5b265aff787516c1f48795e7d1756656cd4842d0f2b2a34e9b1b1ff8f6e13df0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301882140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b0f565a3e5cfc7cce15b5a3254e26a5ee0bec319609690fc717d42b1444b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:58:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:58:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:58:53 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:58:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:58:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:58:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:58:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:58:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 00:08:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 22:55:25 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 22:55:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 22:55:26 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 22:55:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 22:55:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 23:08:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 23:08:52 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 23:08:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 23:08:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 23:08:54 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 23:08:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 23:08:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 23:08:55 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 23:08:55 GMT
CMD ["php-fpm"]
# Fri, 02 Aug 2024 01:52:14 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 02 Aug 2024 01:55:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 02 Aug 2024 01:55:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 02 Aug 2024 01:55:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 02 Aug 2024 01:55:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 02 Aug 2024 01:55:41 GMT
VOLUME [/var/www/html]
# Wed, 21 Aug 2024 17:49:38 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Wed, 21 Aug 2024 17:50:48 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Wed, 21 Aug 2024 17:50:52 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Wed, 21 Aug 2024 17:50:53 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Wed, 21 Aug 2024 17:50:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Aug 2024 17:50:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3702ede31b739c37f265c096aaa90041a249a222cf13f8141408974d1da345`  
		Last Modified: Tue, 23 Jul 2024 02:14:27 GMT  
		Size: 3.3 MB (3322587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd32fd053b31656313ffe5c4d6a711c2bdfbac32689ec3ed4eb1993c89d7c5cf`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c734d1f76ba06cf1de68095cf88223f8aecf6242e60ae0985e4b555bd937308d`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45b7c4aa719c59b7fe7fb0befe844f4c3d28e474917ecb4a3a01aeba778254a`  
		Last Modified: Thu, 01 Aug 2024 23:42:28 GMT  
		Size: 12.1 MB (12120808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b06c719783e091b88ced85d793761529bf28920e90152689d465395817cd13a`  
		Last Modified: Thu, 01 Aug 2024 23:42:27 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92771c5b38843d12dcfb73f19e0ed6710db4edb2579fa36ee02c516f3ebf283`  
		Last Modified: Thu, 01 Aug 2024 23:42:55 GMT  
		Size: 13.7 MB (13694852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7930a04b44d0337833cb375dce25bdfc8f67f7b27fbb81975ca5d4b3dc22e`  
		Last Modified: Thu, 01 Aug 2024 23:42:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88064674d379f589d24d595a06bf5d21a17da42d7bbc81fcdb952460599515df`  
		Last Modified: Thu, 01 Aug 2024 23:42:52 GMT  
		Size: 19.7 KB (19715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ed364e2d8b70d9472a316903b7d2c2c2386ec3c56680cd124c139444c2a322`  
		Last Modified: Thu, 01 Aug 2024 23:42:52 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa01d38e1d8942248f1c966d50fff90299b98c333aa139630b811c4d22468a5c`  
		Last Modified: Fri, 02 Aug 2024 02:07:40 GMT  
		Size: 41.3 MB (41251655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072399ec192d9ee55c1bf386ef168f0427fcfe7a70cdd43e5affb436a015c47b`  
		Last Modified: Fri, 02 Aug 2024 02:07:31 GMT  
		Size: 7.4 MB (7433680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d78640800d8d156fbd9ccc778f202265df4254506178a7d1c26b79b1fa980b`  
		Last Modified: Fri, 02 Aug 2024 02:07:29 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb88809d68f0856208963c3169b1ec28a655b9227456db5a4aa44e3fe4e89bbf`  
		Last Modified: Wed, 21 Aug 2024 17:56:50 GMT  
		Size: 220.6 MB (220550592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fff920dae6a01131446a492bb93c877891a07ce5168daf17ce68a46bcf34563`  
		Last Modified: Wed, 21 Aug 2024 17:56:10 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeb39832e18a0fa20194b6805b7afb83d04941e05159ba60622b2ff437b2865`  
		Last Modified: Wed, 21 Aug 2024 17:56:10 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:7896fdcc3bb44fca27afad4019ac970e66324953e93c934991199b63ef6a756c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309408892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9596c60a2cd6d82491343bd15567695916b7e909c1dc2864ab3a5177cba23bd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:55:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:55:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:55:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:55:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:55:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:48:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Aug 2024 21:12:10 GMT
ENV PHP_VERSION=8.2.23
# Fri, 30 Aug 2024 21:12:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Fri, 30 Aug 2024 21:12:11 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Fri, 30 Aug 2024 21:12:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 21:12:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 21:17:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 21:17:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 30 Aug 2024 21:17:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 21:17:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 21:17:39 GMT
WORKDIR /var/www/html
# Fri, 30 Aug 2024 21:17:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 30 Aug 2024 21:17:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Aug 2024 21:17:41 GMT
EXPOSE 9000
# Fri, 30 Aug 2024 21:17:41 GMT
CMD ["php-fpm"]
# Fri, 30 Aug 2024 23:04:36 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 30 Aug 2024 23:07:21 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 30 Aug 2024 23:07:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Aug 2024 23:07:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Aug 2024 23:07:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 30 Aug 2024 23:07:24 GMT
VOLUME [/var/www/html]
# Fri, 30 Aug 2024 23:11:38 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Fri, 30 Aug 2024 23:12:37 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 23:12:44 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Fri, 30 Aug 2024 23:12:45 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Fri, 30 Aug 2024 23:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 23:12:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea931861c5de5183556532dc6b8b142a8ce8c2b331268d669fc95323009238de`  
		Last Modified: Fri, 30 Aug 2024 21:44:29 GMT  
		Size: 12.1 MB (12139353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9df7d1d6892aabe831708f9c85e36f8df27faaafb595bbc224b1e4770be5a28`  
		Last Modified: Fri, 30 Aug 2024 21:44:28 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98ae526a9a009f85b9efe3e2f8212f794bd02eea345fe07c92dd3f5f1bb8a89`  
		Last Modified: Fri, 30 Aug 2024 21:44:56 GMT  
		Size: 14.1 MB (14055852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b92b765453d62868a0cddb46c623ba4d3ab1c7c614cc5a480bace7e886b6ee`  
		Last Modified: Fri, 30 Aug 2024 21:44:53 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a67efc185c77fc36fd0ae5ee394979c4be7b9ab432148966f0a249c771a079`  
		Last Modified: Fri, 30 Aug 2024 21:44:53 GMT  
		Size: 19.5 KB (19489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b4e3cddbd735de8ec5fccb34381bf91398aafa8fa7af42a4419650bb13874d`  
		Last Modified: Fri, 30 Aug 2024 21:44:53 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d455c9a748dbd954b4b4fb560afb3f93ff28d72a0dba47eab95ca42ecfe08d`  
		Last Modified: Fri, 30 Aug 2024 23:15:20 GMT  
		Size: 48.5 MB (48542405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf91e5078fd4e61e61f755398652f45bf19cfa431300847e771d7a048061944`  
		Last Modified: Fri, 30 Aug 2024 23:15:10 GMT  
		Size: 7.1 MB (7108260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ce911fa1e0d8f4cb94896c58336ebba92dae2cb9213ad459f3246f2a262570`  
		Last Modified: Fri, 30 Aug 2024 23:15:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa8fbce1447fab5f5f5ed1a2e01df53f0614c13ef1a1727b63b2767090dcccc`  
		Last Modified: Fri, 30 Aug 2024 23:18:11 GMT  
		Size: 220.6 MB (220550828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2fc1c158ea4f4e5a832a96bfb37fcd4a62029ea0bb09568936101b7baec99`  
		Last Modified: Fri, 30 Aug 2024 23:17:42 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aca7157a62cc17a3eb49495eaf6c91d2c24bd4e0b7311670723278b615c66`  
		Last Modified: Fri, 30 Aug 2024 23:17:42 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; riscv64

```console
$ docker pull nextcloud@sha256:d059c4aa36711c956d6131f8c2275a255bda1cd3fe03c90cee3a654eab0564fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299149342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0183b2e7be4ffbcf080cd7660cb288ae5cfdd35b3b321fb52218a3dddcb1e84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:40:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:40:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:40:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:40:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:40:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:40:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 06:05:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 23:26:04 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 23:26:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 23:26:05 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 23:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 23:26:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 02 Aug 2024 00:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 02 Aug 2024 00:48:35 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 02 Aug 2024 00:48:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 02 Aug 2024 00:48:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 Aug 2024 00:48:43 GMT
WORKDIR /var/www/html
# Fri, 02 Aug 2024 00:48:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 02 Aug 2024 00:48:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Aug 2024 00:48:46 GMT
EXPOSE 9000
# Fri, 02 Aug 2024 00:48:47 GMT
CMD ["php-fpm"]
# Fri, 02 Aug 2024 02:59:06 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 02 Aug 2024 03:23:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 02 Aug 2024 03:23:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 02 Aug 2024 03:23:49 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 02 Aug 2024 03:23:51 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 02 Aug 2024 03:23:51 GMT
VOLUME [/var/www/html]
# Wed, 21 Aug 2024 17:18:28 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Wed, 21 Aug 2024 17:22:48 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Wed, 21 Aug 2024 17:22:58 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Wed, 21 Aug 2024 17:23:02 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Wed, 21 Aug 2024 17:23:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Aug 2024 17:23:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66e2d9485d0a2716d7e24ddfd4cd99998480bc594d4435d34aa9faa254a91e8`  
		Last Modified: Fri, 02 Aug 2024 01:32:04 GMT  
		Size: 12.1 MB (12120806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ec01bccd4f7ed959676eb7dc010e0bce387541308c7002b426daef6f4c993`  
		Last Modified: Fri, 02 Aug 2024 01:31:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d649a9c54a434d93bddaf3b707e62cb354f00c46ecaae84c4a871cdfca10d2f5`  
		Last Modified: Fri, 02 Aug 2024 01:32:52 GMT  
		Size: 12.2 MB (12225653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11720b3797eb494d5691af3a8a1d83c04567ee0261a1e6a2a030ecdf2f002ba`  
		Last Modified: Fri, 02 Aug 2024 01:32:41 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afbfc941da118624f03c70ca8260c0616613d1ea29be0bc23488bb9dd5fe53c`  
		Last Modified: Fri, 02 Aug 2024 01:32:41 GMT  
		Size: 19.5 KB (19494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a94cf69e546c51d1951c7815bb0322fa9428452a2134c76bab0042711476af8`  
		Last Modified: Fri, 02 Aug 2024 01:32:41 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d1de103ba3de7b2f5a804d5ddb8b7541fec1ca931b16c76760665a08a8447`  
		Last Modified: Fri, 02 Aug 2024 03:38:41 GMT  
		Size: 40.6 MB (40625842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d5bd5585d01789642b5748a165897075032135a64b8352e8dfd9c0cd3abce5`  
		Last Modified: Fri, 02 Aug 2024 03:38:06 GMT  
		Size: 6.8 MB (6818930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbaee2fa1b41c59f8553aad9c77e08ff2583c7aee3df6212fb33a72f87b3b4c`  
		Last Modified: Fri, 02 Aug 2024 03:37:57 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f5ed4715bba3d382fcbb2faf87adad4955f036319aa5d2942b191fc88ed3d5`  
		Last Modified: Wed, 21 Aug 2024 17:30:14 GMT  
		Size: 220.6 MB (220550566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83febf6f40dc4e84a3871116964505268abc07f2afe31c5f3b3dc8be1ecbb6e`  
		Last Modified: Wed, 21 Aug 2024 17:26:51 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7995a52d1e84632c5053a36750c3f61f888a3b603cdda4647773d88bdbaf3d`  
		Last Modified: Wed, 21 Aug 2024 17:26:51 GMT  
		Size: 2.3 KB (2319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:stable-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:67f88a18225f35eda610ec9835f83d9942388414d5c8315c3286dd42e047732a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306382023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b375d171ddfcd9c38122a67567a18a5f19cf9854ef41efde988666e71cb70fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:33:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:33:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:33:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:33:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:33:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:53:39 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Aug 2024 20:43:24 GMT
ENV PHP_VERSION=8.2.23
# Fri, 30 Aug 2024 20:43:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Fri, 30 Aug 2024 20:43:24 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Fri, 30 Aug 2024 20:43:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:43:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:49:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:49:24 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:49:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:49:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:49:25 GMT
WORKDIR /var/www/html
# Fri, 30 Aug 2024 20:49:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 30 Aug 2024 20:49:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Aug 2024 20:49:26 GMT
EXPOSE 9000
# Fri, 30 Aug 2024 20:49:26 GMT
CMD ["php-fpm"]
# Fri, 30 Aug 2024 22:14:55 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 30 Aug 2024 22:16:51 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 30 Aug 2024 22:16:52 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Aug 2024 22:16:52 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Aug 2024 22:16:52 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 30 Aug 2024 22:16:52 GMT
VOLUME [/var/www/html]
# Fri, 30 Aug 2024 22:21:13 GMT
ENV NEXTCLOUD_VERSION=29.0.5
# Fri, 30 Aug 2024 22:22:21 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 22:22:29 GMT
COPY multi:93e628175b4469d463083705f9db1d7b4d090629cd6c12433f52a951b154a5c4 in / 
# Fri, 30 Aug 2024 22:22:30 GMT
COPY multi:aea9ca1c1203dc95e0f5b2d2738e3c7d37564bdb8350411b15d39b9ca1d1fb05 in /usr/src/nextcloud/config/ 
# Fri, 30 Aug 2024 22:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 22:22:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bfb05ce80b1ae366ea2477578b23264464f3e2898b0c923f3e72cc856e59b9`  
		Last Modified: Fri, 30 Aug 2024 21:14:15 GMT  
		Size: 12.1 MB (12139343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc21e161154529bdab2fadb157fd0d6b7ebf34801417e050af9e045fa0a743f8`  
		Last Modified: Fri, 30 Aug 2024 21:14:15 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842aab5c2abd95760ca8c823de3c920b2d48880dcd6ee210c07f966095430c5d`  
		Last Modified: Fri, 30 Aug 2024 21:14:34 GMT  
		Size: 13.5 MB (13518593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506ea6c855899d08c36ac7369ceb595f2e3e39d38bf9f93f6c691dab493b19d4`  
		Last Modified: Fri, 30 Aug 2024 21:14:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4f61161398108d2e15da7d310ad3c5d8e8b563c99b51570ff1f66a4e27fb8d`  
		Last Modified: Fri, 30 Aug 2024 21:14:32 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712aac414103b6651991246cc20af64e3087a7670e6953e839354b22863642ef`  
		Last Modified: Fri, 30 Aug 2024 21:14:32 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29eedb8d4f9c27920ce0e39c3f9ad3a248a0e773ec1229f12e0ef55848c125f`  
		Last Modified: Fri, 30 Aug 2024 22:24:07 GMT  
		Size: 46.1 MB (46077855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc009782c68986466c735606f7565d8a0ff3ba368b2138fe4d5e41a669f09027`  
		Last Modified: Fri, 30 Aug 2024 22:24:00 GMT  
		Size: 7.1 MB (7126981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6c7511c2b0b908c04b470c970f2e49622e0f8639177bee7f64c524675a1b6`  
		Last Modified: Fri, 30 Aug 2024 22:23:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4733fef8d0b1b08a1c2a31944b77d68f1e5feb668abad5ee7eefc278aeb5ecac`  
		Last Modified: Fri, 30 Aug 2024 22:26:15 GMT  
		Size: 220.6 MB (220550762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3242534b23927c51fe58e6dae1f4f8b6c682028563290bee0932325fdedd14`  
		Last Modified: Fri, 30 Aug 2024 22:25:51 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5fd7a538ca8856b9608dcd7219633e1efdf8c5f4f98ec9da89bb295954dc31`  
		Last Modified: Fri, 30 Aug 2024 22:25:51 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
