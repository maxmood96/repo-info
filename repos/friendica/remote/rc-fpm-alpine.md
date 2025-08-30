## `friendica:rc-fpm-alpine`

```console
$ docker pull friendica@sha256:6b3197841fd6ce5f86e3dc254f9572d1c92ee07d908f6d55ce46eb782a16d4e6
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
$ docker pull friendica@sha256:4ecfa620f5ba1b5566c12f0a88e86715cb0a3a804ed716fc8673c792dce1f72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59652183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950c45d965c4c3884f43e4ebe111e1592fed736d03eea34c532029e3d61d6aba`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10ac87811a7151f2d455ecd66e1f24914759aa556bf865115e9b5451c34c6`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 5.9 MB (5927523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fc0402d547809980039811ae9b42dfcded62490cdfd22f86eeae02a5401c4f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5118a89a65a7879c4cdee30e47c63bad49e3b3db33a51de3fe326c3d569fc205`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd1735270d6e1518aaee894fef4efe6676e548396eb6350a2823bd039d45d65`  
		Last Modified: Thu, 28 Aug 2025 18:19:55 GMT  
		Size: 12.6 MB (12604759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b287e8c3fc7e356d999ffd59f3ff23eaeafabb55d3e982709ea8418d30caa7`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8c7c6fddb40b2fb483e7c0cdb28a715ad094759babae305cc3ee8b3324cad`  
		Last Modified: Thu, 28 Aug 2025 18:19:55 GMT  
		Size: 13.3 MB (13265060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca0b473638630b0d5752cba198cb4c45e865cc6f571d15a657778b8c9573f7c`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadbc3591c836d34e9c40cf1dbc676c2da1c2c323afd6e29624fe20bf6143a7f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 20.0 KB (19959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff2d0bf89e370e10b4bdf5193157afcda7091db8c80f48573111444634e51a`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 19.9 KB (19950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a961078f85baeb62fad90d7f53e5a386185ce08cde9f06f1cbaa0c3d91b7e81`  
		Last Modified: Thu, 28 Aug 2025 18:54:14 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c801b7006c533b8ae2aa2f43f7d1c05579426a3b5571499edd79fc5136527`  
		Last Modified: Thu, 28 Aug 2025 18:58:47 GMT  
		Size: 8.8 MB (8754613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b143f764bec4d0832f01a7af37ffb4632c36b5f96ce467a4f32bcb62ea06c1`  
		Last Modified: Thu, 28 Aug 2025 18:58:46 GMT  
		Size: 1.0 MB (1031307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd2d934fbbf2e5fb538ed12192eb92bf77e5ab0eebae08f935057bb7882684`  
		Last Modified: Thu, 28 Aug 2025 18:58:48 GMT  
		Size: 9.8 MB (9823495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501fe2be7592d2df6553ea2e37f4965bee65559552c2e70a1f2b910827042786`  
		Last Modified: Thu, 28 Aug 2025 18:58:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968832fb15d70d9afba8f84584eea848ffdec367f02150fc3bcd4a1b273e4d0f`  
		Last Modified: Thu, 28 Aug 2025 18:58:46 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f1b346f54095bc19b12da40a474ee38d3c7f62c5429fd393db55f3f7d34176`  
		Last Modified: Thu, 28 Aug 2025 18:58:46 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b08fd3e5c53c2b3599196b824ba680c3ed8e3db9b4bbf54085df83c23f7bd4f`  
		Last Modified: Thu, 28 Aug 2025 18:58:46 GMT  
		Size: 4.4 MB (4386520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918035d4b74d973a05d3125dba840c6393ab8ace3dbd8e2f7cf7c72b9a04ccc5`  
		Last Modified: Thu, 28 Aug 2025 18:58:46 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a40d6f892b31fdeee2bb77c7de7a58fe1ff96521b0cbac37ed5f25142146a1`  
		Last Modified: Thu, 28 Aug 2025 18:58:47 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:709025d2aa50943d4a62603852972d204a2b7723ca60f94b78c3093fc3a00c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc79d2ca0e2102dd6d6e2673c898ba5381e6fd3d06c2c87bcfbf3182e2400ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b2fb6b9fc0340a4a0ca58f882fe9b45748f20bf90a73a0edcd61cce5be9481e`  
		Last Modified: Thu, 28 Aug 2025 20:29:31 GMT  
		Size: 55.6 KB (55553 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:f0e5eee5b6923bda21c92e9498f3b25bb5e69ad311886a5023878aec0624a1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56778010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02275788c6d2cc64a5195d0562787bddc55849d4f7451028b70e54e9190469d2`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ffb49c82cf16fea2b2658c93683845111cd140ee61f49d53a82c3343d66eec`  
		Last Modified: Thu, 28 Aug 2025 18:50:06 GMT  
		Size: 12.6 MB (12604744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dede99cf30270dcfe20bbea8569fb35edb90a7f2526cf016a454258c5bd825`  
		Last Modified: Thu, 28 Aug 2025 18:50:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d46d83cb43634c3a9d6d3ae51bc364e0a22f932446846a5076f8f853c5b633d`  
		Last Modified: Thu, 28 Aug 2025 18:54:48 GMT  
		Size: 14.6 MB (14591980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720229cca20b0fac0004477dea0d6345a3bb1f6cfa25abecc961966d9b0fc077`  
		Last Modified: Thu, 28 Aug 2025 18:54:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94728b4b4e6e7e475cf1d5bc67e2be88a5b5f9280e3041dd6233847e30fcfcc6`  
		Last Modified: Thu, 28 Aug 2025 18:54:41 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47051b49d7293aeec1bb0d509def29db4e079b0d9b723e3b05d57fc971e003d`  
		Last Modified: Thu, 28 Aug 2025 18:54:41 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a2f3a97e3f7a9b96a80c2275a22d9dcb266c7d0ac5725c9c782dec1d4fbe1f`  
		Last Modified: Thu, 28 Aug 2025 18:54:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6a20e375109f90c2a2e09138b0b433e72096c31d40ad1ab63c97c5a1ec580`  
		Last Modified: Thu, 28 Aug 2025 19:40:09 GMT  
		Size: 8.2 MB (8247571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fca25a8e5f543c1f90f76ffde0eef4bff962e2993b39cbff713be1b08ac852`  
		Last Modified: Thu, 28 Aug 2025 19:40:09 GMT  
		Size: 997.6 KB (997562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a3a32b4d93746f6a86ecf5692343d54d2c105279b193c3ae70b69f45e34c0d`  
		Last Modified: Thu, 28 Aug 2025 19:40:14 GMT  
		Size: 9.0 MB (9012194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2861d6155e91d9192937465221364d1b65fc37f3c9919d9bf32f2e69344e1a65`  
		Last Modified: Thu, 28 Aug 2025 19:40:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63868ce9fe845b26a0099c2fd23a52e88f7fd60c2b5cf24af7edcbcee24c0e8`  
		Last Modified: Thu, 28 Aug 2025 19:40:09 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561461e5d430fdcc7ccc485c15d6015f196c3dd51a15d5571fc616fd00d795bf`  
		Last Modified: Thu, 28 Aug 2025 19:40:09 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854dc852a3d7abbf4f6a44cfbea5587bcd175bb84ab3dbd5ffb38b566a231dc`  
		Last Modified: Thu, 28 Aug 2025 19:52:52 GMT  
		Size: 4.3 MB (4342235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed39146d84f0bfefbd23f30eae4773ac0aeae7755ac433e632c3e1fd78e1d2`  
		Last Modified: Thu, 28 Aug 2025 19:52:59 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d90d97db44d7f43da4a19aa32ffb93d0e019f31c111ba488d1c8b454c51cca`  
		Last Modified: Thu, 28 Aug 2025 19:53:02 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:58a07dc69874b4a2f4e7d666e2b4c9e1ca68347d1654c4777b520215876f5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39005fba90ccf00031a49b7c86da64f89a5f386e2be213b0b62ecf20fc52725c`

```dockerfile
```

-	Layers:
	-	`sha256:42767d8d2022a8cf15ec75bff3c8868d0e240bd5f9026a9950801e6810d3f981`  
		Last Modified: Thu, 28 Aug 2025 20:29:34 GMT  
		Size: 55.7 KB (55684 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:9cf6ff32fa966ce209c4c3216fe8a446b3169156c56f4f0e4448c35a2272714b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54311329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c85fea71809da961286f7c1255671b93f34ed0d8248cd8f6541041da766012`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2918785e629efa03cf38782364004ea1df208a39271bb2a5151ecbdbdb5e9ce8`  
		Last Modified: Thu, 28 Aug 2025 20:03:12 GMT  
		Size: 12.6 MB (12604738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c080e32941e053d3c4d92eca9329f64f69bf58840130e5db6255bd511a32de`  
		Last Modified: Thu, 28 Aug 2025 20:03:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a86ff043135e8a3587175ac0ba432c1acdee5ca304ed4477948583608bef45`  
		Last Modified: Thu, 28 Aug 2025 20:06:43 GMT  
		Size: 13.7 MB (13712718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9bee49b296b37bcbf26ac2c8aedada04450e543c19a85a69590598d0aa1d5b`  
		Last Modified: Thu, 28 Aug 2025 20:06:42 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a3c3be5bdfd0c6f6cc03a2c1af4fdaac6e2fd0409d9f6a665b1395e69a5876`  
		Last Modified: Thu, 28 Aug 2025 20:06:42 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810a87995c24f58eefe7bf06ff573bb8a75904d22b00909fa46b1550d49cc8d`  
		Last Modified: Thu, 28 Aug 2025 20:06:42 GMT  
		Size: 19.7 KB (19723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6b2a0a3efb00c15cea158646e74fb80e4d2c75a3d4b9fb6ac7d03f3740e257`  
		Last Modified: Thu, 28 Aug 2025 20:06:42 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d79e400d2c587666bde82d32228b6b0a968fc18510fc5791345e8f462888c8`  
		Last Modified: Thu, 28 Aug 2025 22:21:41 GMT  
		Size: 7.6 MB (7622119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8838499b56643eecce23fa7d7231c97c2a02fcd9511dac53b5c0f6736f0abc40`  
		Last Modified: Thu, 28 Aug 2025 22:21:41 GMT  
		Size: 997.5 KB (997528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd16d2995655edeb0c711ac61b5aada55d47159c2ae9276f9cc1673a164f3`  
		Last Modified: Thu, 28 Aug 2025 22:21:42 GMT  
		Size: 8.9 MB (8907322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b57e86f87a585e4c0dfde8cdd6e3aab3925b4aba71c6e954715d82527879f`  
		Last Modified: Thu, 28 Aug 2025 22:21:41 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc90a02c0549ecad12b444cce5e32a22180bd870c69cc405ee49cc8c3eb594cc`  
		Last Modified: Thu, 28 Aug 2025 22:21:41 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb569b1795a2e033ce73368c372ce18e9a027dbd2bf21cd51057a1f1a69989d`  
		Last Modified: Thu, 28 Aug 2025 22:21:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6faa71b41916a298d6450070b3e3e710d90a1b5cf7d9efde2c22d549a13b87`  
		Last Modified: Thu, 28 Aug 2025 22:22:05 GMT  
		Size: 3.9 MB (3948187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cc18350cfa8063eaed0964bcec09acdfada23dbb97932c3f3c4b5fa8f50a36`  
		Last Modified: Thu, 28 Aug 2025 22:22:04 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a952efcf2097a07195f24957275444500cbd59e467aba8825fb608fbec0ac3`  
		Last Modified: Thu, 28 Aug 2025 22:22:05 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:d05f8f3bf98e09873741e83238f56d3414198babb602b934d5b9d28252236980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514cfa5306a917d6227a6f4792e38c2a37929f34c0072e9b5817b4e3d60ca125`

```dockerfile
```

-	Layers:
	-	`sha256:5a40e23d92bad0adfdd6359a5d0ce6bb2792b77ae8b1e132e6d07f40c145e63d`  
		Last Modified: Thu, 28 Aug 2025 23:31:06 GMT  
		Size: 55.7 KB (55684 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:677848e5547dba87fd30913faa8e8d55202e39c39ae61891e68eb09bab2ed483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60671062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81672cae3ce70a9257df7e78d5416125801686697b342b824a55c1eed4ec77c4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb46ec3ec285c20759c8abcbd1fba586aee25c6fbedc58e70878ff9bbf9d07`  
		Last Modified: Thu, 14 Aug 2025 22:51:06 GMT  
		Size: 3.5 MB (3454714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e261bfce6cd6273c06f83b374dbb38f92be17c8f1164bc775f5b69489eb88a68`  
		Last Modified: Thu, 14 Aug 2025 22:51:05 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff0d60a0178ee618748f0a5b1b04c9c64b64af3eeca8d0b1566e182adf144e5`  
		Last Modified: Thu, 14 Aug 2025 22:51:05 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf4676eacbdefe39bfac32e05cda23795bc9daee2e796b169fe7f1bb5b999c`  
		Last Modified: Thu, 28 Aug 2025 19:55:42 GMT  
		Size: 12.6 MB (12604750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312dbb78ee6211e9f8bc4c4092f74a8593ed65c1777538e94ca527ec39b4919d`  
		Last Modified: Thu, 28 Aug 2025 19:55:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01008e7f0b09c8f5f61ac4bac060e1ad2a5139049bd4bac4c4b6e22df88537d`  
		Last Modified: Thu, 28 Aug 2025 19:55:39 GMT  
		Size: 16.5 MB (16479599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873d66094b6e463be49f00fa09ce9d07f868a8c395a389c8c0b1701e95be00a0`  
		Last Modified: Thu, 28 Aug 2025 19:55:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3714a1bcf92550e69c247bbd370a34367a32b0c6e1220f8981efc0bc9ab516`  
		Last Modified: Thu, 28 Aug 2025 19:55:38 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8046e282f403841e2727bcb0cb2aff44d4b29ac405ccb01fcc4596ab329a80`  
		Last Modified: Thu, 28 Aug 2025 19:55:38 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533610671fba9be4595d5b9d0a7869e6d3311d9b5c9ab48c54e04811e92d1730`  
		Last Modified: Thu, 28 Aug 2025 19:55:38 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40346161a3a3a3975823926159d071139bbe8fbc2ed740dc759ab86afe067fcd`  
		Last Modified: Thu, 28 Aug 2025 21:38:51 GMT  
		Size: 8.6 MB (8625545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c2fce494194bf83486ca0ba3fddde9649a0ae8326cf99feda468e90d1ef04`  
		Last Modified: Thu, 28 Aug 2025 21:38:50 GMT  
		Size: 960.8 KB (960829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da9fedfcf6c6116d08874e527fa686e02f182556554ffcf8318fd364ebe6b2`  
		Last Modified: Thu, 28 Aug 2025 21:38:52 GMT  
		Size: 10.0 MB (10025409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e34fb69380c019c5d02883f712b44d7fd1c4e247d6235a85096d773c920b405`  
		Last Modified: Thu, 28 Aug 2025 21:38:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b91ef008b88d48d5d1288851972352a1b3185c90061ea3f7af15935f8d1341`  
		Last Modified: Thu, 28 Aug 2025 21:38:51 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d642a48b06344031be60b8de9d406d749905f14a8200d6bb2ac4d37944939`  
		Last Modified: Thu, 28 Aug 2025 21:38:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979ede187a610a51b578092ff59b4f4173fe2b106b8a178965f6d6cefa04c85`  
		Last Modified: Thu, 28 Aug 2025 21:38:55 GMT  
		Size: 4.3 MB (4330633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627d0cb6b36d8e07cb7b913381f6df2bab3ff4ce9938a9cccc6450afec50ec08`  
		Last Modified: Thu, 28 Aug 2025 21:38:51 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02f455ad79907b731662a3e1aea4ac35993c5077c6e8c1afb0dd7a438080703`  
		Last Modified: Thu, 28 Aug 2025 21:38:52 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:ade20acf936d15a69c4167639cc74ad7c49b25f813eb04b65f6968d300db2a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874d4b105eb3052484835e7fae5eaf3017950fe4b57ef39d87be991ddc2bbb26`

```dockerfile
```

-	Layers:
	-	`sha256:e8c1a02cfe2e60223b6b153da172c761ac6b7a9b7d612365a93618bc0f00c396`  
		Last Modified: Thu, 28 Aug 2025 23:31:10 GMT  
		Size: 55.7 KB (55722 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:d55bed0f4200619180ea2229d13e887739f8a30dcf6f474338d62a971621965f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c464ae8ae75eda0ad90dd4888ee701d60b5d0e2ef78e9ddc324a760bb6d2b44`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a59919ff7785468d660110ee9507b13705f5565f639b7d7bca52a140856b5`  
		Last Modified: Thu, 28 Aug 2025 18:21:34 GMT  
		Size: 5.8 MB (5794083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33e8e8baf1e334700853edab49903aab1f8ea7b65bc8ea9036cad309a3b7118`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76198f21a38b8e65970b7af97c8146cceaaec7b8de4cf4fce2e437c8d7c1ded2`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0592096578de3942e0d1a4c0f06e422ce9b189222d19d93f037d9a2a7cd776dd`  
		Last Modified: Thu, 28 Aug 2025 18:21:35 GMT  
		Size: 12.6 MB (12604751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ff3610c46e30d8afb952ca77229101670ff07b031f0081af9be71a61f790d9`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f9edc9ac84dc15c4aeb3c15f82244bce0018deaef4c21466f4176f60271d3`  
		Last Modified: Thu, 28 Aug 2025 18:21:35 GMT  
		Size: 13.6 MB (13576202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a6a5ffb0b2a909ed36d16b6d5edb06ad2441db4e65f12a3e54b31a4257f002`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c4b3d6bd1e1a984ffcff35fb9de7fde05ffe9612a5162b6623b81891a7738f`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 19.9 KB (19939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860d1b0c44da61c8fcd2da1c6fc38bb05b9af25db92a95654b50e27c114639d`  
		Last Modified: Thu, 28 Aug 2025 18:21:34 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264286dd6fb0223c2ba34bbb87fdf4e5aa440f4c3d17067731cb9bca46215247`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a26414d3376046b9ee6afd0c9a4653c2225af6cff8c044a7943da17620878c`  
		Last Modified: Thu, 28 Aug 2025 18:57:53 GMT  
		Size: 8.8 MB (8834908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3e783e16435f62ed9e84b364a2dbc8622751981f4f24131cadf371523d23ce`  
		Last Modified: Thu, 28 Aug 2025 18:57:52 GMT  
		Size: 1.0 MB (1006349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5fff085be1c5a334b5a7f18a235ff604e7eaeb1dfc058e027404c52323e9d7`  
		Last Modified: Thu, 28 Aug 2025 18:57:53 GMT  
		Size: 10.0 MB (10001217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154e5cbcc2b525851403badb207e2d0d9b72fe18bb79f70686461f52d02db682`  
		Last Modified: Thu, 28 Aug 2025 18:57:52 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d32337c26104442f10d560412da803f81cb9b6d9e72b8fe6b74f0b2d9c0163`  
		Last Modified: Thu, 28 Aug 2025 18:57:53 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e86ebb52f6116e52f77944d2f1eea1507b87ac64ee5107ddd38418a14312ba`  
		Last Modified: Thu, 28 Aug 2025 18:57:53 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8cb06f367748d9c893a1e06bb4f804eff0718ef0d92c8bc165d92197937ef`  
		Last Modified: Thu, 28 Aug 2025 18:57:54 GMT  
		Size: 4.3 MB (4345947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae4dc3aa1fa2dc24a8521e2968f95894db2e2a235dd9e632ed77049f3a4dbd2`  
		Last Modified: Thu, 28 Aug 2025 18:57:53 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf972f4865262bda33e42dbdfb77d0426f2579de14c72847f8f3d5ca4159cbf`  
		Last Modified: Thu, 28 Aug 2025 18:57:53 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:ae67ac70298cf39e2f57ce82f3c77a50ae8e86710d95e236fa04ec5459d9892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195b9b99b8738d28e5d60cabe9d6befd6844612204b6de114b4ebe5a86b5e725`

```dockerfile
```

-	Layers:
	-	`sha256:d2247da8c561319c3bc474003eb92bf80eb9da73c1fef0eb8d994cab589d554b`  
		Last Modified: Thu, 28 Aug 2025 20:29:43 GMT  
		Size: 55.5 KB (55527 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:9e9bcd078c387226efe6ddc894fd2922ac0d3c590152f8df44a72665b2220911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60943461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af9ace66b79dc13262e1efc6b24e9b194b78e11d171add3547e5a99b3d4eed5`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a10f54e3cf46392e1b1d8a3fdbbd55dab891b479c19b6c11b26198bda8124b`  
		Last Modified: Thu, 28 Aug 2025 19:57:53 GMT  
		Size: 12.6 MB (12604760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a936478d6b913e27fb074f07561c747b02dab3a8fe48e6c6fbf14865eceeb23`  
		Last Modified: Thu, 28 Aug 2025 19:57:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e99d0934860d123930b0f3ce8e29285163bb043083cc3be4014881e857a1`  
		Last Modified: Thu, 28 Aug 2025 21:34:44 GMT  
		Size: 16.5 MB (16538318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a098c7d4b8ec8a02be2b15dc1ea5d06268a80cd2e730952958bb882956fde47`  
		Last Modified: Thu, 28 Aug 2025 20:49:11 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ff391b7201b718c4a8c8577e5381d40dd1056318e2f9a533f25bc898641b9`  
		Last Modified: Thu, 28 Aug 2025 20:49:12 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dc4f32f1d2c4a913b9449cbf1916b70f80fd75d15e0da2a9bbcda789983b50`  
		Last Modified: Thu, 28 Aug 2025 20:49:12 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c397b784b8c9ebbf0ee026cc5b635254377a9ca084c93e24ad4e7917a32b01`  
		Last Modified: Thu, 28 Aug 2025 20:49:11 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f71bfba9cdff45342cf136371f989f73f93cf0dd69bb67cd964ab76256c49a`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 9.2 MB (9190904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b2f9791f691c05641fff14e7bb3652eb3617baa3e2a5bcff78398f29fbf22`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 951.1 KB (951101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941235b02a5bafa8532a240b23e348dbac5777b979b193670ec1700ee91cb634`  
		Last Modified: Thu, 28 Aug 2025 21:54:34 GMT  
		Size: 9.8 MB (9822596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa81366ef2a9bc274e83e44c0bb10d1db0526b4485bebba822bc3567447a31a8`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dee30ed4976c340abf58b38116d287553c450a4246a04f1319a6914744c347`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549f2b4b4e552b81ec39115bb5c23158542c34e238b759be9250cf51ff3c8d9a`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da54d024b2811f009aea68dcfb759c96f0c608ded01b87f44e81230d1be60610`  
		Last Modified: Thu, 28 Aug 2025 21:54:34 GMT  
		Size: 4.4 MB (4438680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b07d2ec30c9dc7b5d4ca9752886444e056832927fc21fe1ecfaa6e48796fe08`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051fc0364347f800f737af0bca6baf8f9f822d225fbeeb4e39d7401507818aed`  
		Last Modified: Thu, 28 Aug 2025 21:54:33 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:9e2d5573eb00f215a937a9972432e5af236d16c7a8545510cf55117377ac5019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3502437834c0fa2c0cede2ff654e86d69e3063650d5da4c44a1d3540a7ad07a2`

```dockerfile
```

-	Layers:
	-	`sha256:765a8e4496990b70cccc8c18d05510c739fd4ea849dbffccbb7363911876a3c5`  
		Last Modified: Thu, 28 Aug 2025 23:31:15 GMT  
		Size: 55.6 KB (55590 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:f929fbfaa77f6ea88611fed67afdc50169de74aac682930140f75ac6d64c29f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58341120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ebe14306d314e956e8ef6e95fba003fc2713ed90385f61ff567e068e38b63d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
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
	-	`sha256:d96000ef7021911e67902fd12f051a526237f6a40c66c9589b2b5db98f38d845`  
		Last Modified: Fri, 29 Aug 2025 08:42:41 GMT  
		Size: 12.6 MB (12604754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173261600f62a02225c3dd6df60f7d0a44148dbb7c1bf44389ea5f88029aab29`  
		Last Modified: Fri, 29 Aug 2025 08:42:40 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f759c295dc7087e8e44b12601a6243ce9d0b68556cb7dd836a31e1a354039e31`  
		Last Modified: Fri, 29 Aug 2025 09:37:36 GMT  
		Size: 15.4 MB (15373062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ddb2aaa91684a31108ea7ed7c148f3d4ae2212e874c73bca68046872a7fd2f`  
		Last Modified: Fri, 29 Aug 2025 09:37:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575111e7d18cc70bb28ca7721c58cbb317134aaafdb48c0adf9c807cacbfe999`  
		Last Modified: Fri, 29 Aug 2025 09:37:34 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58c2996917687d3006e674955ffcb615931acc0cfd5d4cfde159698ea50802e`  
		Last Modified: Fri, 29 Aug 2025 09:37:34 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017a3609db60858a05c6121b9978debbf6f84e4f57ee5552d8a3e55be90de17`  
		Last Modified: Fri, 29 Aug 2025 09:37:34 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1585bbf61ea7fbdeff28d0f9fc30ea71567e9fda784db9523f88153404272e`  
		Last Modified: Sat, 30 Aug 2025 10:02:53 GMT  
		Size: 8.5 MB (8543770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb07eb01c32717fae53e989018bccdd3b4b399aef61196f2f49672e7a81fad2`  
		Last Modified: Sat, 30 Aug 2025 10:02:53 GMT  
		Size: 1000.7 KB (1000658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eea75445cd4d827d09350458253669a05c59b9929ea31c548c8aa2975266a57`  
		Last Modified: Sat, 30 Aug 2025 10:02:54 GMT  
		Size: 9.3 MB (9251470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd0ed8530c2637761608a65f834299fe1eb31b561756e917f7f459d1fc5aa31`  
		Last Modified: Sat, 30 Aug 2025 10:02:53 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423ccc97ea6e564cf16bce6aa4e987b1506d7509a9f410cdea20d8f4e1d751f2`  
		Last Modified: Sat, 30 Aug 2025 10:02:53 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc5b9f6a77d57e3b097f2a53c8d7b9f59b5e99a63ac7c19b58b823053ab4286`  
		Last Modified: Sat, 30 Aug 2025 10:02:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d834ae4382b8ad038666c94905d36b8206d9edfb6891b8c97011ed392b892c`  
		Last Modified: Sat, 30 Aug 2025 10:04:36 GMT  
		Size: 4.4 MB (4401612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab6be7b4f9e41a07c9a4efc3425ebb8130fc23ec1c87b90d5c4284bfbe4904`  
		Last Modified: Sat, 30 Aug 2025 10:04:35 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf802c95930e975c0c9cf8a4ec06776d4222dc121227417fa37c487731c5e44`  
		Last Modified: Sat, 30 Aug 2025 10:04:36 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:346f22e95ea1a163df85f30d1601c234d77cf7a3168480b522afff9010760c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717450c4d9c6e359f685a173b57868dd74a1cfc8d5882c76c5b0970ab662b3ff`

```dockerfile
```

-	Layers:
	-	`sha256:2b2848be8cf321670a6ad4eb2f40f5b9f45e3c3b55c4215fceff943fa8f5dfb9`  
		Last Modified: Sat, 30 Aug 2025 11:27:59 GMT  
		Size: 55.6 KB (55598 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:82b7cb3fb2652385bd6b91c48a9c11672b68de1bc53784b5dba15f439c6a4b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60227348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c2a44791ae9bec559e776023832103f476e4886641c0cf43d07f2afec375c8`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.25
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
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
	-	`sha256:94903378f3b1382e25208bbf4d2f2bf4ec6d6054a11c010e0850482b24b4b478`  
		Last Modified: Thu, 28 Aug 2025 20:07:49 GMT  
		Size: 12.6 MB (12604752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2da20a0a8075070cdc568bcd5656adf420efb26b4f5279eb977d339837798ba`  
		Last Modified: Thu, 28 Aug 2025 20:07:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a930a5c92c7194335de66a2a3435ab1f956999846dc4b5af71aec10268563c`  
		Last Modified: Thu, 28 Aug 2025 20:12:07 GMT  
		Size: 16.0 MB (15977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51444d55c82ece6604ddac3bf7c8556d9b6c3e61139c07ce157dbc4dadab54ff`  
		Last Modified: Thu, 28 Aug 2025 20:11:57 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ea380a829b85f6dedf47d4fb4f62ec350af376df98def3baf953c1f64d270`  
		Last Modified: Thu, 28 Aug 2025 20:11:57 GMT  
		Size: 19.8 KB (19755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fd432ecca732571d14bb008e969db19db1a361864ff7212629bc6ba58f7264`  
		Last Modified: Thu, 28 Aug 2025 20:11:57 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86660aae37d90bfca12f28200d6d589951a6d51332e05e769efc5d8068b97a`  
		Last Modified: Thu, 28 Aug 2025 20:11:57 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dc8903d61bc31c143fc0ef21a5524fdb5416472675167a99ccc1d9f047cec4`  
		Last Modified: Thu, 28 Aug 2025 23:35:06 GMT  
		Size: 8.9 MB (8907436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5b6d1beb4e2bdc26fc02541292e0fb957b4d2a2a181fb2e71bfb815969c95`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 995.3 KB (995257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94ef31b52897250e12320c296904af800a82078ff5935ebb808ef5ac5b2c17d`  
		Last Modified: Thu, 28 Aug 2025 23:35:06 GMT  
		Size: 9.8 MB (9760058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a846c237b7e40af2335007793da77f16ad1f2889bd07299e4b0a6d3ac832d702`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbe0bcca58e30e6570210515641a05d9694c7eda3d55fc2669449c172cb9c32`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c0d70c8ceb21995797148824b510f273f0ba5851879514ed792dc9c2000ead`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca6624e9cad695779e55f9c71a6dd5a6043a6211861e9ddb90910cb16234a1e`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 4.6 MB (4598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e528a6b3eb58938fdaaf5e48e1bd3caf5aaa08f04e582d3edd7c3b1ed83797`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fa88a29f5c0dd21a0b47056bac0604f4ca67e2d39481549c7a1835014ef59b`  
		Last Modified: Thu, 28 Aug 2025 23:35:05 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:43bac00e747840f4f75ac6e9aee70c7c9b33ea2594f5db2d95e2a7aa2b2dc7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df53fb59666ed0ed04c934427c12c8503eca4cc4838e1a10fceeb82df43677e`

```dockerfile
```

-	Layers:
	-	`sha256:7441a4418cad0e3d9331b4ae252695c795b6f6451984b04a49ae1daf09269181`  
		Last Modified: Fri, 29 Aug 2025 02:28:01 GMT  
		Size: 55.5 KB (55546 bytes)  
		MIME: application/vnd.in-toto+json
