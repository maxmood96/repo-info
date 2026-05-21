## `friendica:fpm-alpine`

```console
$ docker pull friendica@sha256:3c3051b1b840cbfa978a8854d30b540791ad326b652cb03cd3d9af7943433833
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

### `friendica:fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:42f9100da9cbb3d2245f8c86ab888eba658ee8fb3619a88c3a280e66b87cde9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114808480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994e9df1348f40cc04b578279bc95cee14b2d844800399f9f22d61a17be6033f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:46:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:46:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:46:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:46:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:46:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_VERSION=8.3.31
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 07 May 2026 16:46:31 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 16:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:46:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:49:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:49:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:49:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:49:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:49:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:49:22 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:49:22 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:49:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:49:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:49:22 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 18:15:18 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 18:15:21 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:15:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:17:09 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 18:17:09 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:17:09 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:17:09 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:17:09 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 18:17:09 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:17:09 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:17:09 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:17:09 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:17:09 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:17:09 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:17:19 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 18:17:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:17:19 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:17:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:17:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16323142a7bea87118b505294f1beb54f6faccf68ce249b72a731c6974fa22`  
		Last Modified: Thu, 07 May 2026 16:49:29 GMT  
		Size: 3.6 MB (3587616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9471adb458466f769f3eeb941bc465d4fd6b5e6f27753435073b57e36acd12`  
		Last Modified: Thu, 07 May 2026 16:49:29 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ebfc0da6ac84a857843c5052ca8d352ac8b4047594fc3dabbc71e4370280f0`  
		Last Modified: Thu, 07 May 2026 16:49:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c61fa94d7da787c35e4a60bdc3c5c6bb5eafa2bd30bc94294c4664758a07ba5`  
		Last Modified: Thu, 07 May 2026 16:49:29 GMT  
		Size: 12.6 MB (12627235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b43e8756c663de765f89841392219b5d7271cec0d77bfa3764189362f8969`  
		Last Modified: Thu, 07 May 2026 16:49:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a27baa42c1531ed84d6cd9eb48646d46f48745d29227af2db4fcb11ff7cd49`  
		Last Modified: Thu, 07 May 2026 16:49:31 GMT  
		Size: 13.4 MB (13373653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b073a40c2801fb025b9c924760b97ed44316e5cadf77178f4487c3aae84ce6`  
		Last Modified: Thu, 07 May 2026 16:49:31 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658398bf87f90fcf74a88aae31cec49b54b8cb14691df7b452f323b736e11664`  
		Last Modified: Thu, 07 May 2026 16:49:31 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c49becc054479b976571e06bd36f783cafa4a994af71f81c1e40aea4ab6f99`  
		Last Modified: Thu, 07 May 2026 16:49:31 GMT  
		Size: 23.4 KB (23407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4e874a37410a53fcd8241fd93056232dd0ded909d2a01bbaec711ddd60f6c5`  
		Last Modified: Thu, 07 May 2026 16:49:33 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316da11cb1b8907d8db5b6308f248295c1e870f64ce9a922ab4eb1442d549247`  
		Last Modified: Thu, 21 May 2026 18:17:28 GMT  
		Size: 12.5 MB (12530942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b27ba207ad79f67e04859b26d17d8a3e6a02e6450e90929b4a8cab0349217ef`  
		Last Modified: Thu, 21 May 2026 18:17:28 GMT  
		Size: 1.0 MB (1038150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72ebc5bcdaf26fc361a884f4f452f35aa19f88b499bcc2fbb643cd63e9d2375`  
		Last Modified: Thu, 21 May 2026 18:17:28 GMT  
		Size: 9.7 MB (9731554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efefb101859d6b7c05c4cbc444bea1d77b1b4bf5c9df89f85785c658cc8fbc2`  
		Last Modified: Thu, 21 May 2026 18:17:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42b176fb9b7d7ba4be2c6db59284f058cce81401b8929eedea6d82ca583c13`  
		Last Modified: Thu, 21 May 2026 18:17:29 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96f16eecff0559e006ff5447582b47de9b3b0c4b1b88e8aa2c8222c3655900a`  
		Last Modified: Thu, 21 May 2026 18:17:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db65cb930a99536476a17728629295b3d6822dc71128a602776a384ab6f726b`  
		Last Modified: Thu, 21 May 2026 18:17:31 GMT  
		Size: 58.0 MB (57989588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b3281227cda9469cbce040c1d7d93ddd99a5a3ebfa489b14e1bfa0d8e4dd5`  
		Last Modified: Thu, 21 May 2026 18:17:30 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceb7f316f649433dc7feea603bc939467496bd6dc76b23f1b5b00aa2180d3f7`  
		Last Modified: Thu, 21 May 2026 18:17:30 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:323f03c5c50973ae10da78a0355261bc71023624c37cddd39b1397766415a70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d29d892730331c01b157971297c7e1370a656995591b6fd8cb9d70b907d7f6`

```dockerfile
```

-	Layers:
	-	`sha256:93e2fb4f41201328b1c1dfba17f5ed459eb043341f3834d50a62e7fc0ea36194`  
		Last Modified: Thu, 21 May 2026 18:17:27 GMT  
		Size: 59.4 KB (59448 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:e389699d657c94b47d2848b569ffbf591e59ae63ddf56059cccc507a469e3206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111593334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b03b286c73ffd62470d6e1097c68b11c987fad1d179ddbf5b6740ec83e0adb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:47:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:47:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:47:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:47:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:47:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_VERSION=8.3.31
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 07 May 2026 16:47:17 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 16:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:47:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:50:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:50:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:50:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:50:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:50:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:50:15 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:50:15 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:50:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:50:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:50:15 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 18:16:09 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 18:16:13 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:16:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:18:31 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 18:18:31 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:18:31 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:18:31 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:18:31 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 18:18:31 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:18:31 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:18:31 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:18:31 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:18:31 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:18:31 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:18:42 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 18:18:42 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:18:43 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:18:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc7a47c8fedfb3d805c7c18fe1a7eb6896273078412ce5d277961a53b72022`  
		Last Modified: Thu, 07 May 2026 16:50:21 GMT  
		Size: 3.5 MB (3543619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ad4995cfe3e3b5a8b81cc102048c664a371aab9fa54958142142f3064eb9fe`  
		Last Modified: Thu, 07 May 2026 16:50:20 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c32151de9b49b1cc3814dba4da3b87c8ddeb9426196a285abd2b35e5a7dbc8`  
		Last Modified: Thu, 07 May 2026 16:50:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f53047b29c155794017673ff301e3d7618239179e28636a258883a172a138`  
		Last Modified: Thu, 07 May 2026 16:50:21 GMT  
		Size: 12.6 MB (12627252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d8335e7aa2e2163c07726dd6d6c87d47c02ec5b821f6a90ea0f0a0d27c133`  
		Last Modified: Thu, 07 May 2026 16:50:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02e5f2aece37c05fe1c23ddf07bfd2e1f6f1cfb7ac0d6f9511ed13eafcca9ed`  
		Last Modified: Thu, 07 May 2026 16:50:22 GMT  
		Size: 12.1 MB (12101528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844f14657175f519e2baa6761237add3d132eda98d70ad1108f6177030995df7`  
		Last Modified: Thu, 07 May 2026 16:50:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b48867a116465bb2b56188eb47643b27587c521c16a483bcfa99b15c8c6889b`  
		Last Modified: Thu, 07 May 2026 16:50:22 GMT  
		Size: 23.2 KB (23203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3bd737683658d26628f22f74d384f7736686bcbe66324284574cc6ec253869`  
		Last Modified: Thu, 07 May 2026 16:50:23 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99125882eb2cbe2adcab957dd9d96204e9ca72d942fb9ec53a75d26887bd05b3`  
		Last Modified: Thu, 07 May 2026 16:50:23 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed190700fcef7e6c67282eb4cb1c8b5a4691ab863f9e5b1b43606158ec11f5df`  
		Last Modified: Thu, 21 May 2026 18:18:52 GMT  
		Size: 11.8 MB (11790013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca624489bae972f6aa456850a102a89111ea7e0503baac7454321eb1e33e946`  
		Last Modified: Thu, 21 May 2026 18:18:52 GMT  
		Size: 1.0 MB (1006245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99559aa1b51cfe764ee9aec01566bd0bf520516d55a7103f822cfe6a86c0a0e`  
		Last Modified: Thu, 21 May 2026 18:18:52 GMT  
		Size: 8.9 MB (8898005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce684210044f6bf16b8f16d53e020bdfe59e7b08160dd71ca8fd937ec26c93a1`  
		Last Modified: Thu, 21 May 2026 18:18:52 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ca9d6f31a00f0956ccf19856aadf32b090cfe1069c155ff4d3424b479b1aaf`  
		Last Modified: Thu, 21 May 2026 18:18:53 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cef63f7647ee06349c705deeb6899b863ae9965eea5922d5c2b0861b66d90c`  
		Last Modified: Thu, 21 May 2026 18:18:53 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610f602aad308652cc03a16ebf315bf65e85adc70661ddbd8e45c912adce26e2`  
		Last Modified: Thu, 21 May 2026 18:18:56 GMT  
		Size: 58.0 MB (57989621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c09434b29046cd479ed96446c990d2ef5cb4f0a6e4498f57d224765f3cd3fef`  
		Last Modified: Thu, 21 May 2026 18:18:54 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2661cbfe7a64212ddd0bdc005bc0ea425ee1c0272bc1b89f4371df7c2bdecf`  
		Last Modified: Thu, 21 May 2026 18:18:55 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:57101a729e97de032ce12b4777a2c8e35d3afd5d562636e42cd29518f7b3fcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc28025927dd83386b1c16e1cee46352bdc01ef6b631fe824933045b02b6d4d`

```dockerfile
```

-	Layers:
	-	`sha256:4b17f1ac1a3a6052dd8c39a8f78cece194c0dd9cd273cf66b58357f191f545c3`  
		Last Modified: Thu, 21 May 2026 18:18:52 GMT  
		Size: 59.6 KB (59598 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:7f06a95db884d19c4ed23bc910fcdef35dd8a7824053c3c36ceb9c86a63a305f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109407632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c58ed5ee9ee289e154ea473d123a2e94e233f757d80cadc963a7c359020105e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:00:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 17:00:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 17:00:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 17:00:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 17:00:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_VERSION=8.3.31
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 07 May 2026 17:00:54 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 17:00:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:00:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:03:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:03:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:03:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:03:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:03:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:03:53 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:03:53 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 17:03:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 17:03:53 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 17:03:53 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 18:16:01 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 18:16:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:16:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:18:26 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 18:18:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:18:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:18:26 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:18:26 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 18:18:26 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:18:26 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:18:26 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:18:26 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:18:26 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:18:26 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:18:37 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 18:18:37 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:18:37 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:18:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:18:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56a45895f2553951c0a259d2dd96a11e2fca5b597d2b5ec47ffac77f2ffb26`  
		Last Modified: Thu, 07 May 2026 17:03:59 GMT  
		Size: 3.3 MB (3343515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd3ec8bcd158c2cee012a87ab253a0756e5e2dc8dbb10e4964bec5cde740c81`  
		Last Modified: Thu, 07 May 2026 17:03:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a3ac249a89ee756848706c97693b1a4659300a90718775924b9d15dffc9b93`  
		Last Modified: Thu, 07 May 2026 17:03:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703f3bccd863ccbfab5534f2e216af9d475a3172842d3cbb6dd0ca30a58a167f`  
		Last Modified: Thu, 07 May 2026 17:03:59 GMT  
		Size: 12.6 MB (12627260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f99c7a739732948c6cea18fe4174a54ddcd1d2c1ed9fe4ac0af67d6b29eb106`  
		Last Modified: Thu, 07 May 2026 17:04:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583f464c298281177427b7aa17b14a6874fe4a01fa619082fb1aaa2d360f5cfc`  
		Last Modified: Thu, 07 May 2026 17:04:00 GMT  
		Size: 11.4 MB (11401791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d81531ffb96bb1e3c804d7cc64a93a4cd464b39c1049f9b384238ea32c5863`  
		Last Modified: Thu, 07 May 2026 17:04:01 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241cea0f37aba3e34c06c83186a08e9fabf69e1b61a69a35945d598d78f566a7`  
		Last Modified: Thu, 07 May 2026 17:04:01 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f799be701909215e79d1ea59aea5bddaa51c0d7cf135ae62abb69f8ba15a67`  
		Last Modified: Thu, 07 May 2026 17:04:01 GMT  
		Size: 23.2 KB (23225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a4d1e89cd12b42a83e02026eed990f16101857bade5263e17a0937e859e7b6`  
		Last Modified: Thu, 07 May 2026 17:04:02 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e17d9b7d4b79535f1325b8198f3ba086445f5f63f8ad1c98fe664d69352cb`  
		Last Modified: Thu, 21 May 2026 18:18:47 GMT  
		Size: 10.9 MB (10853538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2959ebc4e60606659f1ec5da4f9240f217275fa0aaac1758716338aebbf887`  
		Last Modified: Thu, 21 May 2026 18:18:47 GMT  
		Size: 1.0 MB (1006213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e90d73144b5d36da4272764afddf3d0ac631003c76cc518773be00eec353df6`  
		Last Modified: Thu, 21 May 2026 18:18:47 GMT  
		Size: 8.8 MB (8837499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361dccf5d466da3fe068ac00d7246b33f10a8fa0277007c6152a5ec0df3b32e1`  
		Last Modified: Thu, 21 May 2026 18:18:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f266e2e4fce4c502ade5b2873f4a565705025600aaf6a2cc2a19ad84af108864`  
		Last Modified: Thu, 21 May 2026 18:18:48 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e2c6f2240fc81e7ff56ab892ab59270e826ccb1cbe09c5b5fca9d747ddd50`  
		Last Modified: Thu, 21 May 2026 18:18:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29160744d2b0e41e12aecfb865f31c2c37b679b2bad069d14ba4c8fd79212aa3`  
		Last Modified: Thu, 21 May 2026 18:18:50 GMT  
		Size: 58.0 MB (57989525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345ffedfc5bb04a1832ca2676927cac7ea1317356be788cb49dff64d573f7fe`  
		Last Modified: Thu, 21 May 2026 18:18:49 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e0c76be6c6d0682ab466038c0ac776f62db8f93531fd35f130339ba889453a`  
		Last Modified: Thu, 21 May 2026 18:18:49 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:5c37eb1e259a9cf1bb5f1830c54203dca0fa1a7889eae214279e9a43559e98fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd87a16421a721c5a0622ed221811142a705ebebd2903eef4659f93cd0079a9`

```dockerfile
```

-	Layers:
	-	`sha256:584fbffd7ff2bf5e95c42f005ea49dbf2271b152ab434fe2cd30136b284bda04`  
		Last Modified: Thu, 21 May 2026 18:18:46 GMT  
		Size: 59.6 KB (59598 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:fbc7b4870587a6682d9bdb3c3aecb90ce23651000800d5b20971ac50bd41826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114776859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b1bcd8e20e312409967c135be70b15684d7a420e4520f1efc9f61cd6884e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:47:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:47:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:47:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:47:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:47:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:47:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:47:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:47:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:47:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 07 May 2026 16:47:30 GMT
ENV PHP_VERSION=8.3.31
# Thu, 07 May 2026 16:47:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 07 May 2026 16:47:30 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 16:47:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:47:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:51:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:51:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:51:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:51:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:51:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:51:47 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:51:47 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:51:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:51:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:51:47 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 19:13:13 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 19:13:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 19:13:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 19:16:13 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 19:16:13 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 19:16:13 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 19:16:13 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 19:16:13 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 19:16:13 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 19:16:13 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 19:16:13 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 19:16:13 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 19:16:13 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 19:16:13 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 19:16:23 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 19:16:23 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 19:16:23 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 19:16:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 19:16:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7696f6a4c5e3c617333c883cdf365b6783ae321831284c57799426be3154f07`  
		Last Modified: Thu, 07 May 2026 16:51:53 GMT  
		Size: 3.6 MB (3596150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bbd65e0f3f1726ab38d44a5ab01a3f1dcc22d1b753bb403f722a0c1b233793`  
		Last Modified: Thu, 07 May 2026 16:51:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053a1da4cd8a0125c20a69581a20c46a6d48b8f60cfdc456cc99244d1c682ea`  
		Last Modified: Thu, 07 May 2026 16:51:53 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2639f0c83865c3e54d17a2604fa669d98f45b3c3d5b86b52babeae4810509fcf`  
		Last Modified: Thu, 07 May 2026 16:51:54 GMT  
		Size: 12.6 MB (12627239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e92f14a78a168f7de85015b8d9e8d0602f01640dd2a130f813a8f5587825e`  
		Last Modified: Thu, 07 May 2026 16:51:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9f3729b0ac95133af9162de22bbe0a399d015c5f411888f8318390d4da7081`  
		Last Modified: Thu, 07 May 2026 16:51:55 GMT  
		Size: 13.3 MB (13263910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01881d30e667bde17da3af9c46f73a71d44d128bbbe761985b95623bd9b81971`  
		Last Modified: Thu, 07 May 2026 16:51:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8291ed6f808d71934f1f0e59b1bdb5d167936b6ca2895d34927da6e6f61f`  
		Last Modified: Thu, 07 May 2026 16:51:55 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892e490aef92e05191adaf1e76461ee68190b99fe518abb21bb56cb0941a1a0c`  
		Last Modified: Thu, 07 May 2026 16:51:55 GMT  
		Size: 23.2 KB (23226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dcb6f9194fdc060602cb29cf420d865d52fcbf79bc4c30cd12d2477a7a751f`  
		Last Modified: Thu, 07 May 2026 16:51:56 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a90b4fc342e06e5c75ac6a9af8ef0cdf5b5ba5b55ea8da22f0eb91d0ecc000c`  
		Last Modified: Thu, 21 May 2026 19:16:33 GMT  
		Size: 12.2 MB (12191142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e917d7fcf6ccd416521254f26a2821222b1c27fadd2fa1d5b89244fcf2e92549`  
		Last Modified: Thu, 21 May 2026 19:16:33 GMT  
		Size: 970.1 KB (970064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b202b966acf5534179ea09cc8fd36cef075cd24e580c3ac9082a99519ed40ac4`  
		Last Modified: Thu, 21 May 2026 19:16:33 GMT  
		Size: 9.9 MB (9873699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b34d269c2602be73228c1e3e941f13f3e655deca633e3d8f33d299704b83c1`  
		Last Modified: Thu, 21 May 2026 19:16:33 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f263c8ba9ff74d5195394b2d94a074c317e2b34817a108b21699921aa9ebf13`  
		Last Modified: Thu, 21 May 2026 19:16:34 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2e3036def39f25b9a4a7799b90b9a9d07aff5b0a4b649325368cca7cb12ec1`  
		Last Modified: Thu, 21 May 2026 19:16:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5fa4f830b6d8268f361983e48960a8183e42b77847c4968584d034d4744388`  
		Last Modified: Thu, 21 May 2026 19:16:37 GMT  
		Size: 58.0 MB (57989589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1d8e3306183ec8ebb781901686d0f51fef69d31742218634913b8fb09a63`  
		Last Modified: Thu, 21 May 2026 19:16:35 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dfa75e2a1129e2fd3540b5a58afa305fcaffdafa79bcad470f1f6e47e25c64`  
		Last Modified: Thu, 21 May 2026 19:16:35 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:2988600dd1d4ab4b3324706f15a7e4546b047d2a23bf32ed279acc8aa5608538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0235d45f11b06b1aad342f863a9bbfc2c764985c68dfecf64acb293b0f6cc78b`

```dockerfile
```

-	Layers:
	-	`sha256:e5fe22ca75274db4e9374eda65417502a9808bb0f69eb71e0006ce37dc670e24`  
		Last Modified: Thu, 21 May 2026 19:16:32 GMT  
		Size: 59.6 KB (59622 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:95dfa4d6ce347444e21551d37614d44a512d0ca86737d1bae0a939e93b9e0060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115342409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28003fc6356034ffbe5b2521d7d9b20dee27afb6d57bd48781dddaf2653de64a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:46:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:46:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:46:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:46:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:46:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_VERSION=8.3.31
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 16:46:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:46:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:49:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:49:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:49:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:49:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:49:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:49:28 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:49:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:49:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:49:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:49:28 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 18:16:28 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 18:16:31 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:16:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:18:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 18:18:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:18:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:18:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:18:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 18:18:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:18:39 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:18:39 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:18:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:18:39 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:18:39 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:18:48 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 18:18:48 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:18:48 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:18:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:18:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d4cfdee78c5c9457650f428bb6e5d5ab018e6fb26ffa2ec66c2676cb3a7a0`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 3.6 MB (3625754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056a9d559723cd4dffbe25d95535c2d92b2f50373a78d8e9a4b93cad5aa14485`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de11264937c4b4c11c636386176f3d3ea2a01e7eb4166d3945e00bbf2e56f023`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4b83ce3931910f3664ee9d405d162be2605be0c5cad1a36fb3a2bd4cb33e4`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 12.6 MB (12627231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9086ad56ab8d3b34d2a98c06b12ccb46551b0d864bdb7eaef6695216b7f150e`  
		Last Modified: Thu, 07 May 2026 16:49:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980f7710a7b9dc8a5e447a361daa2f9e40d0e5d9eb759e2827a84dacb1986e`  
		Last Modified: Thu, 07 May 2026 16:49:36 GMT  
		Size: 13.6 MB (13627339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f850cf1308be3544cac4480add58b7dd1eb0985545b4eccadc3ad5c84177e28d`  
		Last Modified: Thu, 07 May 2026 16:49:37 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03185b775002f31e1c61457ddb183e927ffc0b7f57ab05b91d15177f5df211ac`  
		Last Modified: Thu, 07 May 2026 16:49:37 GMT  
		Size: 23.4 KB (23380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c6ddd905c3508fa85e8f101e42d137b016e94a6a0c5162cbc812080048d130`  
		Last Modified: Thu, 07 May 2026 16:49:37 GMT  
		Size: 23.4 KB (23405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8bdde6d4a064c6551a59477bdd1d3653786f545d922285a1c7c020bb4f126`  
		Last Modified: Thu, 07 May 2026 16:49:38 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c882bc8bb73dd422a660fcdfc8dfc69510abb261bb5359ab494a838eaa7b903`  
		Last Modified: Thu, 21 May 2026 18:18:58 GMT  
		Size: 12.8 MB (12774817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a07befb9ee053bc1c73d765a067685f14050936585634d421ef8852afbcd9c`  
		Last Modified: Thu, 21 May 2026 18:18:57 GMT  
		Size: 1.0 MB (1013732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7808f3355cff6b1fb2c828898f14613fb66d59ef5410d855eb0717ef4e2215dc`  
		Last Modified: Thu, 21 May 2026 18:18:58 GMT  
		Size: 9.9 MB (9927959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96a8d696ce7333ab47bec2b00af69b921cffc40ef7586a693e04b64c8fe1996`  
		Last Modified: Thu, 21 May 2026 18:18:57 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ef2ca2eaec9866bfbbc1d88f3f85f0c285c3223584a351d03f51850f736f5f`  
		Last Modified: Thu, 21 May 2026 18:18:59 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8317ec73e8761d67a5c4c11527a39099215232f40ce1155dd2fb70555811c742`  
		Last Modified: Thu, 21 May 2026 18:18:59 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc33171e8d3c1363c2ade6216b21dee9782866da69d41398805838b47f50bfd`  
		Last Modified: Thu, 21 May 2026 18:19:02 GMT  
		Size: 58.0 MB (57989594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08868d47f7abd0af80134287f4903ed2e5b33bfb674aa15714d1d610bf82f81c`  
		Last Modified: Thu, 21 May 2026 18:19:00 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb8c9c82f92b80344b78072337369e55a54a52584dfd755d68eaf1b3e604569`  
		Last Modified: Thu, 21 May 2026 18:19:00 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:c0ea298caec9f7bf91f75d2a2708e5e31ea29895e27fb58c2cb62c982782907f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144a4c8e56bb09e7e39ec32c72f665d742ade847aa82fb8a7a9fcdcc79446cb`

```dockerfile
```

-	Layers:
	-	`sha256:ab513adba9310e147b41e3d8e2f5927c9c5b2a8d422297ecc48eca6633b0edc1`  
		Last Modified: Thu, 21 May 2026 18:18:57 GMT  
		Size: 59.4 KB (59409 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:025e652f34cc4ef1a015e349c3a2d1d9b966e70951c333eae4e3faeb4be2c81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116597928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca6b9dddd39140cf1810cef686a63fb210dfa25f24a8002729d8d31ee19636e`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.3.31
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 17:28:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:28:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:33:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:33:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:33:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:33:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:33:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:33:42 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:33:43 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 17:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 17:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 17:33:43 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 18:22:37 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 18:22:41 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:22:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:26:28 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 18:26:28 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:26:28 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:26:28 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:26:29 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 18:26:29 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:26:29 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:26:29 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:26:29 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:26:29 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:26:29 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:26:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 18:26:41 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:26:41 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:26:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:26:41 GMT
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
	-	`sha256:10550b23dfafde9e9ca7140cd4f44ed81df25bd43058acec76dc26b1db48065f`  
		Last Modified: Thu, 07 May 2026 17:32:07 GMT  
		Size: 12.6 MB (12627245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737e37e33cf749d1ac30273eb0d697585403e8a518a3cc360635c9c999c0ea59`  
		Last Modified: Thu, 07 May 2026 17:32:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11cc2b81ca630b32856b1982be4476b8ffd233c035ae48c0b7c6d7981895bc`  
		Last Modified: Thu, 07 May 2026 17:33:56 GMT  
		Size: 14.2 MB (14214490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd6eeec7669df81501f5f4f31deb25c89a58b925947ac6689c3c2a314a01564`  
		Last Modified: Thu, 07 May 2026 17:33:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8d26d5a0f1eaa91e62e87c974a951150616f75cfd7fec4c78419aeb19f9f6`  
		Last Modified: Thu, 07 May 2026 17:33:55 GMT  
		Size: 23.3 KB (23280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7004ad95c52b34210aef71979dd36498d114230eb26ddb3ebae211bca2152`  
		Last Modified: Thu, 07 May 2026 17:33:55 GMT  
		Size: 23.3 KB (23301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009e435e02ee8359ce5b2a623e7f151ffe9644be2c85387b16fa6ef0698cb0f4`  
		Last Modified: Thu, 07 May 2026 17:33:57 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ee18a73228ae935f86d47a96545fe4f74b83bcecece901b641b1ea924ba0e`  
		Last Modified: Thu, 21 May 2026 18:27:01 GMT  
		Size: 13.4 MB (13373265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f7678911595042bcdb8edd701a7e0286a9f8e2e93ae5cc2ce7f5fdaef6d4c4`  
		Last Modified: Thu, 21 May 2026 18:27:01 GMT  
		Size: 958.5 KB (958535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15e4bd2497294be00d9ccad712b5fd0ab71e8c85d475b00434d790fecfe732`  
		Last Modified: Thu, 21 May 2026 18:27:01 GMT  
		Size: 9.8 MB (9771335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f260e287c7eacad7dec1a49f1ccb1b25865b8bc544180f87234f38f7a68adc`  
		Last Modified: Thu, 21 May 2026 18:27:01 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9b4f038e20b8e11a127e773de34dc4db779a9783e79dfbc062984742b33cab`  
		Last Modified: Thu, 21 May 2026 18:27:02 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a58c27a21b1fb66db0689d95038d810c007e0a3d6eb111b3344ed7dd8a9c83`  
		Last Modified: Thu, 21 May 2026 18:27:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbc353d6a647efa0c552728379c4df0ec7f125164a3c57064c7ea9b30f51968`  
		Last Modified: Thu, 21 May 2026 18:27:04 GMT  
		Size: 58.0 MB (57989691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849e51765e424bb89ce0da91b93b3b7896e1a425bc5542ab42035b3097b22f00`  
		Last Modified: Thu, 21 May 2026 18:27:03 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a35213967d049abeaa91d384ce03758dc72b8ab2531a1956ee00c7f99edde8`  
		Last Modified: Thu, 21 May 2026 18:27:04 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:5490d5baaf9f0719c9c1cc59ea691860f375c0dba65e5392c837fc85f2f67fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 KB (59489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218753d45b74eeb5769b5e515524825c8bf3ceb01a6c3066ed08f6672fe89d18`

```dockerfile
```

-	Layers:
	-	`sha256:74204fd8744837b90cb1ae1937908dc56b38b72567e6e0abbf0350ffef38ce16`  
		Last Modified: Thu, 21 May 2026 18:27:00 GMT  
		Size: 59.5 KB (59489 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:d180ea532f259f8c48e7efe8ad051c082fd511f27e1bd0a541bb3482fcc865f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113802142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5894d8cc4f48f3bb6903665064100af0ecad346fb39ff18a6ae566db5ca2263`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.3.31
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 06:21:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 06:21:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 08:08:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 08:08:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 08:08:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 08:08:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 08:08:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 08:08:10 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 08:08:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 08:08:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 08:08:10 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 08:08:10 GMT
CMD ["php-fpm"]
# Sat, 09 May 2026 05:44:35 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 09 May 2026 05:44:44 GMT
ENV GOSU_VERSION=1.17
# Sat, 09 May 2026 05:44:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 09 May 2026 06:33:23 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 09 May 2026 06:33:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 09 May 2026 06:33:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 09 May 2026 06:33:23 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 09 May 2026 06:33:24 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 09 May 2026 06:33:24 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 09 May 2026 06:33:24 GMT
VOLUME [/var/www/html]
# Sat, 09 May 2026 06:33:24 GMT
VOLUME [/var/www/data]
# Sat, 09 May 2026 06:33:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 09 May 2026 06:33:24 GMT
ENV FRIENDICA_VERSION=2026.01
# Sat, 09 May 2026 06:33:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d985715f368e106f070519e1e30240b023f31604b3d9e4cc09f23d4d5150147d
# Sat, 09 May 2026 06:33:56 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Sat, 09 May 2026 06:33:57 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 09 May 2026 06:33:57 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 09 May 2026 06:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 09 May 2026 06:33:57 GMT
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
	-	`sha256:ebb178b6ac3918dbee128dd8b8c72a8073f980747b1549635ed35132b9d4c20c`  
		Last Modified: Fri, 08 May 2026 07:15:04 GMT  
		Size: 12.6 MB (12627273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd9dff3913ca16defa259d5824a3d328dc0cb52e25fdc1ecf7a13c53b37038`  
		Last Modified: Fri, 08 May 2026 07:15:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1163ef489237150c5bfa522d9c3d4a522be35afc86b56010aac82885ad1bca`  
		Last Modified: Fri, 08 May 2026 08:09:01 GMT  
		Size: 13.0 MB (13027602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8ebf12b752615f471467dd356ef8704d4d46b39cd12e7cb783a3e1b286f0f`  
		Last Modified: Fri, 08 May 2026 08:08:59 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f74694c0b3fa4c1491f9b6fba01b4deea7f59507a8972d18095009c1b1af7c`  
		Last Modified: Fri, 08 May 2026 08:08:59 GMT  
		Size: 23.3 KB (23289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c63c8a8f71f09c4531f6d12baafc4b1bb24a55758cdbc6ee9879b3415ecb35`  
		Last Modified: Fri, 08 May 2026 08:09:00 GMT  
		Size: 23.3 KB (23302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f4ca5cf1efe5ed8cdb68cfb699bfe3ab7103a575dc6c1303e24d331f098b8d`  
		Last Modified: Fri, 08 May 2026 08:09:01 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c11410554b15700c8c491c92b9dd5a768dcad4ac858c99c664fbe81c7e3d854`  
		Last Modified: Sat, 09 May 2026 06:10:26 GMT  
		Size: 12.3 MB (12272980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc1c4645e70c4fd317c89c87afe7888b2a752c32dd62eee81dafdc5f4948d5b`  
		Last Modified: Sat, 09 May 2026 06:10:23 GMT  
		Size: 1.0 MB (1010236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f19ef390d8560669a09612fe3209d86411d9ef0123ada4913eb4c42c748e9b4`  
		Last Modified: Sat, 09 May 2026 06:35:23 GMT  
		Size: 9.4 MB (9353376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6b8b527471160c55607215f85941a21cfcf1b0b5cf99c8f2bde4932848dba`  
		Last Modified: Sat, 09 May 2026 06:35:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee85c4202d6038f57a689c38e75c5047eed7fe1928dc560a07bac0f88924563`  
		Last Modified: Sat, 09 May 2026 06:35:22 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f43d43112b846fa630004bd7369c7e0d6b60274990f8d4ab6c9a9fc89e2eea`  
		Last Modified: Sat, 09 May 2026 06:35:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf76c1821844a5a60805c73781dc7effa852b723fee6d32e24dffa09de22904`  
		Last Modified: Sat, 09 May 2026 06:35:32 GMT  
		Size: 58.1 MB (58123402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928786e99ef7740bfb7878af0a5c98b72a30ae0e5c2348871cb899201cd6400`  
		Last Modified: Sat, 09 May 2026 06:35:23 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6c223cbabfb7490425f5f926807b7d8aad23d13a724e49046642ffd4a7fa99`  
		Last Modified: Sat, 09 May 2026 06:35:23 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:c8fb50be29e6d5e1ce063389b3102474b43503762f9f965246a43ed4806638bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d918c25b1acc467919ca20b65f8907c0ef23528085e89822cf440e9ec076aa`

```dockerfile
```

-	Layers:
	-	`sha256:7e7a1d47f47ec4497a076611a15f2f26e16ca41ef7c6db79a798559db4348fd4`  
		Last Modified: Sat, 09 May 2026 06:35:21 GMT  
		Size: 59.4 KB (59416 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:5f8e2e7a53b053b335f328bb1a11c535a7550bfaf1bbdcd897b4001b8384b927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114855425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d7482a2c49cac73f14684287585b08872f1b2d06c721e93661a0ffcdc0952`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_VERSION=8.3.31
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 18:21:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 18:21:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 20:23:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 20:23:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 20:23:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 20:23:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 20:23:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 20:23:59 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 20:23:59 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 20:23:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 20:23:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 20:23:59 GMT
CMD ["php-fpm"]
# Thu, 21 May 2026 19:21:33 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 21 May 2026 19:21:35 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 19:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 19:23:52 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev         gettext     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0;     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 21 May 2026 19:23:52 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 19:23:52 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 19:23:52 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 19:23:52 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 21 May 2026 19:23:52 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 19:23:52 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 19:23:52 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 19:23:52 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 19:23:52 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 19:23:52 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 19:24:00 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 21 May 2026 19:24:00 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 19:24:00 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 19:24:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 19:24:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677f4e03a78a2789370c79cc98bf70277df54605d03b98f1ddd8c95295d1f52f`  
		Last Modified: Tue, 05 May 2026 23:48:52 GMT  
		Size: 3.8 MB (3787519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42209df548fd1cd70d82f40e163f4aa9f58445e4a5853781b9c21d3fcfd67c68`  
		Last Modified: Tue, 05 May 2026 23:48:52 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7564dcf40411cee3aeb67bfbec40b4f100e81196fd1c15db9a1bd419fe441d`  
		Last Modified: Tue, 05 May 2026 23:48:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff07b0fe8729647f408050343786a56c01d54f02a25f625bd2fa6aa5a75e4ff`  
		Last Modified: Thu, 07 May 2026 18:29:17 GMT  
		Size: 12.6 MB (12627260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faedbe738809d457da252858711bb37bdc9ae90dd40d948803354bc1b27e2b16`  
		Last Modified: Thu, 07 May 2026 18:29:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40509e28acba1a62178fc3471aee358472864991954a32d293701dbc7540ba4c`  
		Last Modified: Thu, 07 May 2026 20:24:11 GMT  
		Size: 13.2 MB (13239455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180c0db2bf56475954091514c92dbfde1f815853778bddefc89d93b08144f305`  
		Last Modified: Thu, 07 May 2026 20:24:11 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d5c7f96592ea1b9fed3057a1249be3669fd326d3a6b5687bdd30b016a468a`  
		Last Modified: Thu, 07 May 2026 20:24:11 GMT  
		Size: 23.2 KB (23239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4169b2357ffbd1da83afb622d30c9096d29fb8702413f5510b175b52d70faf48`  
		Last Modified: Thu, 07 May 2026 20:24:11 GMT  
		Size: 23.3 KB (23254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f8187f6a56aa321b896351ca463558bc75d2239eae2f27a0b1a84b10f29180`  
		Last Modified: Thu, 07 May 2026 20:24:12 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57afb7cedf4bf112d23667e2fd9039b137ddd69d0a6ca349a8a1d45cec529a3c`  
		Last Modified: Thu, 21 May 2026 19:24:15 GMT  
		Size: 12.8 MB (12771432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026fd9778a71da7ff8c1b09f8db22cdd61e4263d820ad1d9aaf6ca1d61bc5198`  
		Last Modified: Thu, 21 May 2026 19:24:14 GMT  
		Size: 1.0 MB (1004988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6dc2edd0103a34c4723d11129fd4334dce1eccedee906d35b2439f1ad330d7`  
		Last Modified: Thu, 21 May 2026 19:24:15 GMT  
		Size: 9.6 MB (9643376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6ba78cbe78410632a9b9f27639cd0914d54e93e976322da97430defe05b9da`  
		Last Modified: Thu, 21 May 2026 19:24:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5a1e0e45677761798b210f4f94c82ce758a37de8952b541b3c784daf3995c4`  
		Last Modified: Thu, 21 May 2026 19:24:15 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cea2d942aee6f1199dd736c06296f4c81d7b501502433e56232ec7325b3650`  
		Last Modified: Thu, 21 May 2026 19:24:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65767b5bd9d01e47bb475170e33ad57cfa5b9f2176fc568619795bf5f99696f`  
		Last Modified: Thu, 21 May 2026 19:24:18 GMT  
		Size: 58.0 MB (57989610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486785f9c696848c554895de2022e90ca9b035f9afcab56017688c27d61bee8a`  
		Last Modified: Thu, 21 May 2026 19:24:16 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e2cabef53cb616fc752ae8427c888fce66103c891113fdf43c5399e8799f06`  
		Last Modified: Thu, 21 May 2026 19:24:17 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:b6d93f2d3b53725f2f0c0504ec13355dd45f46c5f5277fae68509e91ce82e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7552a15977105cca88dd808040bd65714a4cecb4577f4b989246305ec3fbf026`

```dockerfile
```

-	Layers:
	-	`sha256:79d1658430df9565adbf40a2d6a6c03e2f46cd986cf47af4054f3b01480d2596`  
		Last Modified: Thu, 21 May 2026 19:24:14 GMT  
		Size: 59.4 KB (59447 bytes)  
		MIME: application/vnd.in-toto+json
