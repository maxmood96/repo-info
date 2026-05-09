## `phpmyadmin:5-fpm-alpine`

```console
$ docker pull phpmyadmin@sha256:f45165ce4ef4ccc2d653267b5b20074945cfa7ffc4e8605b4de0f2a10e761334
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

### `phpmyadmin:5-fpm-alpine` - linux; amd64

```console
$ docker pull phpmyadmin@sha256:de786129e958730dec4ffd1b6085893e6404216326b964945cd50f42dbc3c312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57148747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feacc8eb69aaafc1800c2f3dc2b69c655b6884ba717a6da2dbe6be5c64ac4410`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 17:13:36 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 17:13:36 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 17:13:36 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 17:14:23 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:14:23 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 17:14:23 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 17:14:23 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 17:14:23 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 17:14:23 GMT
ENV TZ=UTC
# Thu, 07 May 2026 17:14:23 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 17:14:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 17:14:24 GMT
USER www-data:www-data
# Thu, 07 May 2026 17:14:24 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 17:14:24 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 17:14:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 17:14:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 17:14:26 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 17:14:26 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 17:14:26 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 17:14:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 17:14:26 GMT
USER root
# Thu, 07 May 2026 17:14:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 17:14:26 GMT
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
	-	`sha256:7b08540d6b6397319992d1046903c5e658a5de859f67c3a2037e471a64fa94ca`  
		Last Modified: Thu, 07 May 2026 17:14:33 GMT  
		Size: 6.2 MB (6239704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b18db317c9617e85c128fa0b31efc0e41dcd49ac87ac347329f9fdf011368`  
		Last Modified: Thu, 07 May 2026 17:14:33 GMT  
		Size: 3.3 MB (3304184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508eccbb4d89595ba5a268dd4ea868b39a63604e91358ad48c5cc6dbeaee4ca2`  
		Last Modified: Thu, 07 May 2026 17:14:33 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42eae3bd966aa51bde93b902142cf9743ace914ddab5c4a2271118d252b3519`  
		Last Modified: Thu, 07 May 2026 17:14:33 GMT  
		Size: 14.1 MB (14087554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7c9d5edd518425b73eb7ae3c651e1f2f9e005e1b1e463d9b464ab627694746`  
		Last Modified: Thu, 07 May 2026 17:14:34 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033e7ac9d50c52559d572da2cc7ea91794d353bc96bd575be6dc4e25d3747e4`  
		Last Modified: Thu, 07 May 2026 17:14:34 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848308b8a47f61672376c318fa7c5aaddee8d5e35d92bff82c235bac16619c2b`  
		Last Modified: Thu, 07 May 2026 17:14:34 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:42b20337251dbf127cf64591b22170b1ccc1754257fc99f4bae0cdc956619ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e99e327a4c60157eb6839eaabe1eba2de6294bb7d40b73798e94551d6e0c1d`

```dockerfile
```

-	Layers:
	-	`sha256:e50c270fe3811ec15023134d442bc1dd43e350f76bd9c52c127e298485733bb0`  
		Last Modified: Thu, 07 May 2026 17:14:32 GMT  
		Size: 48.9 KB (48886 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull phpmyadmin@sha256:e9311a483b94f92b36166b570077e6118e4d8b7dc6603611a6168b5804a58527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54899022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43155f0ba74c7f6e8fab4e6b49b1ba5ae856956a51e6b26026af354a3ea636ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 17:11:41 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 17:11:41 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 17:11:41 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 17:12:18 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:12:18 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 17:12:18 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 17:12:18 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 17:12:18 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 17:12:18 GMT
ENV TZ=UTC
# Thu, 07 May 2026 17:12:18 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 17:12:18 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 17:12:18 GMT
USER www-data:www-data
# Thu, 07 May 2026 17:12:18 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 17:12:18 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 17:12:18 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 17:12:18 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 17:12:22 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 17:12:22 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 17:12:22 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 17:12:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 17:12:22 GMT
USER root
# Thu, 07 May 2026 17:12:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 17:12:22 GMT
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
	-	`sha256:c764a75e8ee4d09fb0837ba5451b5b1eb4ff7b24d8a4369b43dc16f62dcefd1d`  
		Last Modified: Thu, 07 May 2026 17:12:28 GMT  
		Size: 6.2 MB (6213986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a16f1993d422d54d45440a1c516f3bcd3b12e44eaa1c1a30ec8ccd2018f2859`  
		Last Modified: Thu, 07 May 2026 17:12:28 GMT  
		Size: 2.7 MB (2688971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df80b794ab8549198f6eee4791470fc385ab2d7a2713e0e4ab8b0637b7b861d`  
		Last Modified: Thu, 07 May 2026 17:12:28 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff34137113ba81990e789466268e2b7b5869296e95e3aa86dc3059b7749f5e`  
		Last Modified: Thu, 07 May 2026 17:12:29 GMT  
		Size: 14.1 MB (14087561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4951fd44ad60d423d44628e2522e0bf98f3601ad8f525722ad82f5dda1f0846e`  
		Last Modified: Thu, 07 May 2026 17:12:29 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26ac90a9d39525e641bf8e29fd0a5de553b0f61668179c0245987de37af194`  
		Last Modified: Thu, 07 May 2026 17:12:30 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a193e8416ec22674e849390df8c8d6f82db5cb84c7c56a635a02e11d94a05f9f`  
		Last Modified: Thu, 07 May 2026 17:12:30 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:fbf3eefe6fce4ffe918260a133a10337ff05e1c15a5ead916726d9e7e23fa8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9562715f83c55f5486faf4eb8bf86e250f17b9b4a6ba7ef5ec4807bd930a6bd7`

```dockerfile
```

-	Layers:
	-	`sha256:066cdefe680bb5ee7f73f672ed3b72ac6f29b1d4ab39858a79f9ec17f43c727b`  
		Last Modified: Thu, 07 May 2026 17:12:28 GMT  
		Size: 49.0 KB (49005 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:ac04ffab9582f17ca726ad871a27b39fe6c76e5a623aaa60e399475c838ae2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52886490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89937c330c1c0170a7fd01c366b69caa53627a6df0ebc374d3cf29e0addcabf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 17:31:51 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 17:31:51 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 17:31:51 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 17:32:27 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:32:27 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 17:32:27 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 17:32:27 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 17:32:27 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 17:32:27 GMT
ENV TZ=UTC
# Thu, 07 May 2026 17:32:27 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 17:32:27 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 17:32:27 GMT
USER www-data:www-data
# Thu, 07 May 2026 17:32:27 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 17:32:27 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 17:32:27 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 17:32:27 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 17:32:32 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 17:32:32 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 17:32:32 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 17:32:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 17:32:32 GMT
USER root
# Thu, 07 May 2026 17:32:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 17:32:32 GMT
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
	-	`sha256:d6a46ba9121b5446cac6236564b0b77d54cf6ddca7129049e1475587eaccd33f`  
		Last Modified: Thu, 07 May 2026 17:32:38 GMT  
		Size: 5.6 MB (5564434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7704796607d5f3f0cba2e2eba0a407e148c4a60657bafc78a21165d37874429d`  
		Last Modified: Thu, 07 May 2026 17:32:38 GMT  
		Size: 2.5 MB (2514565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5254959b459ab644c7fe1eadc1476d9955a8fa09a32e54c703c9c243b29c56ed`  
		Last Modified: Thu, 07 May 2026 17:32:38 GMT  
		Size: 647.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c40c0ed1bee09d168c6870cd8857682077ff04912973b211cf3814b0b82be02`  
		Last Modified: Thu, 07 May 2026 17:32:38 GMT  
		Size: 14.1 MB (14087572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b5ab9df4e564a5f61d88a36bcf079803af25f1213d49321887bda32d3eeadb`  
		Last Modified: Thu, 07 May 2026 17:32:39 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f862872348acebb085e7b41ad5477d5a11ed8a6a0befc5ae09096187092865c`  
		Last Modified: Thu, 07 May 2026 17:32:39 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb7ed712b7255f121d9eed31d845d1fac11e9270086a7e3552fd4ade7657e4d`  
		Last Modified: Thu, 07 May 2026 17:32:39 GMT  
		Size: 801.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:1285a5b754da0210faaeec6a319a2048f9044dce233a7069dc3dbe184946e7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd42e0de9752df7bab4726704f1594549c0ec43ac4f6201e5395d591837f96b3`

```dockerfile
```

-	Layers:
	-	`sha256:54215c56d28b851519183039386b0efce133c9bc9feea45291dac9b56558f8f6`  
		Last Modified: Thu, 07 May 2026 17:32:37 GMT  
		Size: 49.0 KB (49005 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:8a28551b7093dedce7ffe7a121146293dd6522f71ee25a1d08d113b3c5902097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57630623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9107233d037f191211a7e189fc5086c02c928679de04f4b528dae03cd2e8be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 17:14:15 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 17:14:15 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 17:14:15 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 17:15:56 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:15:56 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 17:15:56 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 17:15:56 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 17:15:56 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 17:15:56 GMT
ENV TZ=UTC
# Thu, 07 May 2026 17:15:56 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 17:15:57 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 17:15:57 GMT
USER www-data:www-data
# Thu, 07 May 2026 17:15:57 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 17:15:57 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 17:15:57 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 17:15:57 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 17:16:00 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 17:16:00 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 17:16:00 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 17:16:00 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 17:16:00 GMT
USER root
# Thu, 07 May 2026 17:16:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 17:16:00 GMT
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
	-	`sha256:5d93036fe3545a892aec71327f204ba72f2679f5f6cb61beccf2206fb32ef01e`  
		Last Modified: Thu, 07 May 2026 17:16:07 GMT  
		Size: 6.2 MB (6209888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79dc42bafc69bf46e9e9ff02a29e11fefa48a4f077cc36b0f427ed327c033a9`  
		Last Modified: Thu, 07 May 2026 17:16:07 GMT  
		Size: 3.6 MB (3581756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dbc5d7be28cd2b3ee39351ae4c5fe973bd0be7ca66f2bfc6995add2ce0ed02`  
		Last Modified: Thu, 07 May 2026 17:16:07 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068554fdac30c5fa84fa621e93410a2429a0d0bd861e7a240c2ac7dbcf66698a`  
		Last Modified: Thu, 07 May 2026 17:16:08 GMT  
		Size: 14.1 MB (14087554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ce69b74b19a3e521d27d89ae67ff96a2cd42f38252216b27603755c19f5789`  
		Last Modified: Thu, 07 May 2026 17:16:08 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb367ade7cb0196cf6935d30e492a49e9438d7f9e6ee1ae8d60c49c8d1736ba`  
		Last Modified: Thu, 07 May 2026 17:16:09 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526abe5c6d14a651c0799e3c386a974d835bfb57dddbd909fa3c335ac993bd6c`  
		Last Modified: Thu, 07 May 2026 17:16:09 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:e8583229cba8bef2306d2e5de574ec9cda7029d5a9f97778db7623772d37bf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116a00e85ce112282ca0e438f59175d0211ef6f75e78804ec05f3bebf6d4931c`

```dockerfile
```

-	Layers:
	-	`sha256:d3d972428c696c087ce36ba2634fe6c0d4cbe11cbeb626f01094ccb7c3664a2e`  
		Last Modified: Thu, 07 May 2026 17:16:07 GMT  
		Size: 49.0 KB (49035 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; 386

```console
$ docker pull phpmyadmin@sha256:75f93abf4d83ba631a6ada42c14a17ac1f743e420c01222c0b34f0d76fb2cf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57236128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff406895593c933fc704ebd6f4818b9f5492ac400f7df60d48eca0568aac19a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 17:13:40 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 17:13:40 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 17:13:40 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 17:14:32 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:14:32 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 17:14:32 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 17:14:32 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 17:14:32 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 17:14:32 GMT
ENV TZ=UTC
# Thu, 07 May 2026 17:14:32 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 17:14:32 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 17:14:32 GMT
USER www-data:www-data
# Thu, 07 May 2026 17:14:32 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 17:14:32 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 17:14:32 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 17:14:32 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 17:14:35 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 17:14:36 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 17:14:36 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 17:14:36 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 17:14:36 GMT
USER root
# Thu, 07 May 2026 17:14:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 17:14:36 GMT
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
	-	`sha256:4dab8e564841e7f042e65596bc168bd705f71360026dc6dc6d6af71160a99d57`  
		Last Modified: Thu, 07 May 2026 17:14:42 GMT  
		Size: 6.1 MB (6119446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c87a6a28e3b1075d81bac129b885943d11c3d8738d158d6fc4bfc0f5cb86ae`  
		Last Modified: Thu, 07 May 2026 17:14:42 GMT  
		Size: 3.4 MB (3393772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48848df147fdeb1f2c25b125af984b1759c0d0d26a3ab1c4dd23e119ffabc915`  
		Last Modified: Thu, 07 May 2026 17:14:41 GMT  
		Size: 645.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439f66a1437325d2571f02a795832cfdedabbdcbcc5d8fdafd4d69573ccdc7e0`  
		Last Modified: Thu, 07 May 2026 17:14:42 GMT  
		Size: 14.1 MB (14087550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e11007828c26c1f1ac6b8937cf82aa7f178cf6316435e4f4cfc0a5c9dc3c8`  
		Last Modified: Thu, 07 May 2026 17:14:43 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12cab299a2d474195b958fdac27cbea063a2f5e30582ae9c25561d0d88a282d`  
		Last Modified: Thu, 07 May 2026 17:14:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b58c22b86068bf88f2e5ad5607b503317550ad77c1ce11657954adfc5df3f10`  
		Last Modified: Thu, 07 May 2026 17:14:44 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:3e01625082ecf72d2587ddeb831da80361254274f39fd466f54b41c9eb217c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 KB (48848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b8f246028ec595434d99215bbd9db6e71cdf150a8ffc21317b44159bf360d`

```dockerfile
```

-	Layers:
	-	`sha256:0092d0f952e90e8212c127023b33626ddb5c9e53c02a324281b8a5b945656fb6`  
		Last Modified: Thu, 07 May 2026 17:14:41 GMT  
		Size: 48.8 KB (48848 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:7d69b5c5a0ecc53f5cf5c8ba42c55db9d2ed9f6d538cc6e4d198988768d4fc18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58150169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eb5310333266b57bde85fa768977ef8532f8a510481d051a50aa09cc8ae3f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 21:38:16 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 21:38:16 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 21:38:16 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 21:39:18 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 21:39:18 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 21:39:18 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 21:39:18 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 21:39:18 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 21:39:18 GMT
ENV TZ=UTC
# Thu, 07 May 2026 21:39:18 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 21:39:18 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 21:39:18 GMT
USER www-data:www-data
# Thu, 07 May 2026 21:39:18 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 21:39:18 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 21:39:18 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 21:39:18 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 21:39:26 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 21:39:27 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 21:39:27 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 21:39:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 21:39:27 GMT
USER root
# Thu, 07 May 2026 21:39:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 21:39:27 GMT
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
	-	`sha256:58317ea449a47ac4c6b1a44f4409d5f21e7cb5d49ddf37e9cea50fed103f3971`  
		Last Modified: Thu, 07 May 2026 21:39:39 GMT  
		Size: 6.4 MB (6429192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226453da0100afd3af49a7e2273348bdbcf50d5446e1dc57ec2bd20cd3f35427`  
		Last Modified: Thu, 07 May 2026 21:39:39 GMT  
		Size: 3.1 MB (3129259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c1374335d36f03091c422f2729285b43421f1974b62f8e067f2e42ddf3004d`  
		Last Modified: Thu, 07 May 2026 21:39:39 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec5ca1188b00b1a17928ad6eddced0c6b3a1418b2e0eff075dec3c826094155`  
		Last Modified: Thu, 07 May 2026 21:39:40 GMT  
		Size: 14.1 MB (14087564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2df88ed32dcf37757a0f79ffd6f3175d819a22d808ca8ecacfd39610e8841ba`  
		Last Modified: Thu, 07 May 2026 21:39:40 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b979240c5325532bff28aafabccf258294d2e1d8e3823f3412237f6556409327`  
		Last Modified: Thu, 07 May 2026 21:39:40 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0562c113adb50229ac33123d23033de0cc0cd42af7930af21ddd8e5f6cabe44e`  
		Last Modified: Thu, 07 May 2026 21:39:40 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:562d6cbc71ebf533f1a8d1eab30b8af3440f00d33b6095fca7caaf2249b84769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b7e3f41d8b8f9a1565e4f4a7fb6839a425cfdaf643ac28fda4af9ebb7d1f16`

```dockerfile
```

-	Layers:
	-	`sha256:a8478e630d2cb814386cd87cbcda6eb38693abd04980dbca4717454a01c1e2ec`  
		Last Modified: Thu, 07 May 2026 21:39:38 GMT  
		Size: 48.9 KB (48935 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; riscv64

```console
$ docker pull phpmyadmin@sha256:98284213f78a562636577bcf7dbf4ad063d1b19986c699742821fa9ddd82b90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56238375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0d46930c640ed4b1473c8845b12d9a51f50bd0d89d115039dcf8eefc580512`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Sat, 09 May 2026 03:19:48 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Sat, 09 May 2026 03:19:48 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Sat, 09 May 2026 03:19:48 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Sat, 09 May 2026 03:26:20 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sat, 09 May 2026 03:26:20 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 09 May 2026 03:26:20 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 09 May 2026 03:26:20 GMT
ENV MEMORY_LIMIT=512M
# Sat, 09 May 2026 03:26:20 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 09 May 2026 03:26:20 GMT
ENV TZ=UTC
# Sat, 09 May 2026 03:26:20 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 09 May 2026 03:26:21 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 09 May 2026 03:26:21 GMT
USER www-data:www-data
# Sat, 09 May 2026 03:26:21 GMT
ENV VERSION=5.2.3
# Sat, 09 May 2026 03:26:21 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Sat, 09 May 2026 03:26:21 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Sat, 09 May 2026 03:26:21 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 09 May 2026 03:26:43 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 09 May 2026 03:26:43 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 09 May 2026 03:26:44 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 09 May 2026 03:26:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 09 May 2026 03:26:44 GMT
USER root
# Sat, 09 May 2026 03:26:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 09 May 2026 03:26:44 GMT
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
	-	`sha256:22c1f44019bb1741dec1accdfb27cd5ffdd3f69f04024cc3b5b834202a1b32c4`  
		Last Modified: Sat, 09 May 2026 03:27:27 GMT  
		Size: 6.3 MB (6265330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae6f7c34e9c6512e6b7e891ea668aeff450d114c5395bfcf01c88fcb4bdb0f8`  
		Last Modified: Sat, 09 May 2026 03:27:26 GMT  
		Size: 2.8 MB (2844292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690ae01f0aa3f73451e05a5398b388bddc89dd13f689060c3df1d1ccf419a01`  
		Last Modified: Sat, 09 May 2026 03:27:25 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeefbf027d8c106e86fb0acabd0b37da98aba5f10a7c4f6d224b57be4124fc9`  
		Last Modified: Sat, 09 May 2026 03:27:28 GMT  
		Size: 14.1 MB (14087555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eede35bc823ec33d81b0d099ef0e67b2e3dd547306c29a4f17508a188528345f`  
		Last Modified: Sat, 09 May 2026 03:27:27 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289c19eeaf100d6d1e9580f5c137d58a1ab09e361719dce54f1c9395c42ecf8c`  
		Last Modified: Sat, 09 May 2026 03:27:28 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47dd05bcd3661ee7a7f14b5b18153f76269c9e65dabcecb497628d1903d2515`  
		Last Modified: Sat, 09 May 2026 03:27:29 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:2a1af8bcc5891702d81fb65e6727af835e4dd1481a834b62ff04f44861d84186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260c3fe86ada11b9f16802174f93ce240b479e5a8d7072292aa65543e2eb2625`

```dockerfile
```

-	Layers:
	-	`sha256:5b83d221ea70b7880a015b06e82d0aa04d7ac7c408fb35a8477263ad13228d3e`  
		Last Modified: Sat, 09 May 2026 03:27:25 GMT  
		Size: 48.9 KB (48936 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:dcea269623cdb11ecc0c6012623d11f533e3b4de8e462b247b6663e28a11c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56962399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cad6176e608da0f126e618eb3718c380dc60acb8269454eb4832a8c0ca2acc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
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
# Thu, 07 May 2026 21:09:27 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Thu, 07 May 2026 21:09:27 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Thu, 07 May 2026 21:09:27 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Thu, 07 May 2026 21:10:02 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 21:10:02 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Thu, 07 May 2026 21:10:02 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 07 May 2026 21:10:02 GMT
ENV MEMORY_LIMIT=512M
# Thu, 07 May 2026 21:10:02 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 07 May 2026 21:10:02 GMT
ENV TZ=UTC
# Thu, 07 May 2026 21:10:02 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 07 May 2026 21:10:02 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Thu, 07 May 2026 21:10:02 GMT
USER www-data:www-data
# Thu, 07 May 2026 21:10:02 GMT
ENV VERSION=5.2.3
# Thu, 07 May 2026 21:10:02 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Thu, 07 May 2026 21:10:02 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Thu, 07 May 2026 21:10:02 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 07 May 2026 21:10:06 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Thu, 07 May 2026 21:10:06 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Thu, 07 May 2026 21:10:06 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Thu, 07 May 2026 21:10:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 07 May 2026 21:10:06 GMT
USER root
# Thu, 07 May 2026 21:10:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 May 2026 21:10:06 GMT
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
	-	`sha256:15e40c3ab8b53f1f4df03847824bcd7e6f40971d70103c47777e4e786fbf45a4`  
		Last Modified: Thu, 07 May 2026 21:10:15 GMT  
		Size: 6.4 MB (6434356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4defa6651c6e6824d4fa5dce81b069c1c973a86cc23c6d3c6e2830eb8731ba`  
		Last Modified: Thu, 07 May 2026 21:10:16 GMT  
		Size: 3.0 MB (2995417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab5cb0ab3ad8f4ebd6e70d2254f98fc54be2e3acf5dfbac6877fffe9858305`  
		Last Modified: Thu, 07 May 2026 21:10:15 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7445878f267ec4e8d8514de0c3235385b2b8256e0d3f6775cebbf4a783e49435`  
		Last Modified: Thu, 07 May 2026 21:10:16 GMT  
		Size: 14.1 MB (14087547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7709f1973ee2d9d54479d8c7baccc54f30e2febdaf2e4b4a6036696200b20201`  
		Last Modified: Thu, 07 May 2026 21:10:16 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ef66cbe0d77deffa4f7f4fa5dc1a395999b5319f64de859cbf14055cd3236`  
		Last Modified: Thu, 07 May 2026 21:10:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559aaa529fd4dab3ec35bd866176f53bd665fd0babf4ebd1e9a3293a24437894`  
		Last Modified: Thu, 07 May 2026 21:10:17 GMT  
		Size: 801.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:afd97921a1f998a5e8bf04b97686eef4e00e57ada8bab90dbf53638aa093bdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d805999da6ee9ae4f74fc5610900ac116beecf7c5c70da668bc6daae9f4cda90`

```dockerfile
```

-	Layers:
	-	`sha256:7e6887fcaab86389f9f1a57918f93ba8dade25a8fc20fc7c2861348da6d66359`  
		Last Modified: Thu, 07 May 2026 21:10:15 GMT  
		Size: 48.9 KB (48886 bytes)  
		MIME: application/vnd.in-toto+json
