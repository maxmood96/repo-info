## `phpmyadmin:5-fpm-alpine`

```console
$ docker pull phpmyadmin@sha256:5b451026d658559b30b267f0225e77119b83086303361ad0324f79c3f8539036
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
$ docker pull phpmyadmin@sha256:c0f4109c8c5a1aa536c2615dd9b742942532b6744017a3b15ce1c901d1a1b446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57076398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460a58cd9cacdb38cdd1e0088388a8721efae21cacbf5322e9a2d3a77a339519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:16:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:16:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:19:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:19:05 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:19:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:19:05 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:19:05 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:12:39 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:12:39 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:12:39 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:13:25 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:13:25 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:13:25 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:13:25 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:13:25 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:13:25 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:13:25 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:13:26 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:13:26 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:13:26 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:13:26 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:13:26 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:13:26 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:13:29 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:13:29 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:13:29 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:13:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:13:29 GMT
USER root
# Tue, 16 Jun 2026 01:13:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:13:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dd4732e2b99153a6d793672259fe16511026394361d9a4546a505fc892ec26`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 3.5 MB (3466800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564766333e2350c3f785f44564469ebc099dcb0871eb5ff8d9f1174ae9416f39`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7470fb2f68ecb33e0cc428289222713040bc6a0fb07a219ec29b9be9f39985bf`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c64268d00ab62c4f8906301775f10530956c2d93f9614fc8043f56a19fd3ed`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 12.6 MB (12626290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8667346ced391e67f639e71ec1fdd3e4f2d5f92304b705cf7502c9aefad6b2aa`  
		Last Modified: Tue, 16 Jun 2026 00:19:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9015c0b720110c5cb9b008ee9ca2a43a0522c253d5bb3eaa78678d300b17f1`  
		Last Modified: Tue, 16 Jun 2026 00:19:13 GMT  
		Size: 13.4 MB (13416525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64f2f99cedc2c8912f0a823a27dcca2cac8ebd8b3fb87bccde22b87b17710c9`  
		Last Modified: Tue, 16 Jun 2026 00:19:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915ffc2502405f650a72b28a68df9f73fe86533e60bb70a5dec1ca9a824d3c12`  
		Last Modified: Tue, 16 Jun 2026 00:19:14 GMT  
		Size: 22.4 KB (22352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ae65494ca8528d38cf4c896b8b4810ea8c9a4a469f902e965bf38edf18ca5e`  
		Last Modified: Tue, 16 Jun 2026 00:19:15 GMT  
		Size: 22.4 KB (22358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ec4a172ae0f050e31e9dcc58b400328245442fd96bba8903ce25ba2e765aa0`  
		Last Modified: Tue, 16 Jun 2026 00:19:15 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307a7ab4c8b5aa7b302232c96e210ed4b84aaf1b7c87b07b1b4c61c3a7500ce`  
		Last Modified: Tue, 16 Jun 2026 01:13:35 GMT  
		Size: 6.3 MB (6262506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048704d76d2b13bc38e80afa78ad12c6fdb3038a2925ab4c935673c0d16b063`  
		Last Modified: Tue, 16 Jun 2026 01:13:35 GMT  
		Size: 3.3 MB (3307809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc2019172b11d2d35403e96b3b55f0529a7e23bb96a0b2b8c0828315d245d9`  
		Last Modified: Tue, 16 Jun 2026 01:13:35 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e17ec7bfcb46da709cc1a49ff31788e34b62bc658fa2e9512e8b610113331e4`  
		Last Modified: Tue, 16 Jun 2026 01:13:36 GMT  
		Size: 14.1 MB (14087549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c488f80d1152d5bc9cd3de792cc8d3586dcfef5f7cbdbb0f824bf1c14f6e725`  
		Last Modified: Tue, 16 Jun 2026 01:13:36 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbdaed204d7bf25d28cc047fa64db736b37ca03b372ba7a0dad49ecff46c573`  
		Last Modified: Tue, 16 Jun 2026 01:13:37 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c5c14e61389099ed642b99fa644969646499572f47bd51f3bfa8dc7c9de6a`  
		Last Modified: Tue, 16 Jun 2026 01:13:37 GMT  
		Size: 801.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:04746150f34a584d16451302d8aa295ef146532599edad80450ba783302884f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33f256b63cb5a9ac45acdd8cf93436238bbd7ce8b62eef775cb80c0e84740f0`

```dockerfile
```

-	Layers:
	-	`sha256:4c7730e4c2666230b76d6eee86f9fd62dc83e52d3118a95b303aa34d5a9735e3`  
		Last Modified: Tue, 16 Jun 2026 01:13:35 GMT  
		Size: 48.9 KB (48886 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull phpmyadmin@sha256:92370320a1fe13cae5ccb6d7aceeabd35aa74080c2fa02f17ae345d0a3c8b251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54825605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f7ee28d0eff7a2a7c5e259a11e6eab09fa9fc8c2018f17c684f87f57f839a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:19:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:19:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:22:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:22:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:22:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:22:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:22:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:22:31 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:22:31 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:22:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:22:31 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:22:31 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:11:31 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:11:31 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:11:31 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:12:07 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:12:07 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:12:07 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:12:07 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:12:07 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:12:07 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:12:07 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:12:07 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:12:07 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:12:07 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:12:11 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:12:11 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:12:11 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:12:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:12:11 GMT
USER root
# Tue, 16 Jun 2026 01:12:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:12:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5230d03921a527b9f279c604c71dc4db15ab131e00ad4ac831317aed9b8592`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 3.4 MB (3416654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b528158f29bd5ca9983f791571ec7eac252b82c365b58879ae3bd2ff2e48c2f4`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8af6fa12a7122bd4001e6224682f17ade9530bc74e05c2722c1ed4a37478318`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668f255cd4d090b89df03b29a76d5c4a5a7acc200f994a634add4c4a079f0851`  
		Last Modified: Tue, 16 Jun 2026 00:22:37 GMT  
		Size: 12.6 MB (12626294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bd5987c0d80157b12468800d25035c39c7826b125856e5ded0d1094e531d96`  
		Last Modified: Tue, 16 Jun 2026 00:22:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b533baab338501d966ffc88ae6c9bf5d223475a1004e418a5b0c11a219245f9`  
		Last Modified: Tue, 16 Jun 2026 00:22:36 GMT  
		Size: 12.2 MB (12159505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe05818d056f3a4c55f207d013300f36d54389bd56430b34a135293b312ace8`  
		Last Modified: Tue, 16 Jun 2026 00:22:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe9b3ff027b1cb06a1748f0d17f739f6d7c848986665e2050299981e13a21f`  
		Last Modified: Tue, 16 Jun 2026 00:22:37 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24d9c21c2e0d79d7af2bb090baf0a2552eca490c70f22c4b6da72d749f9e79`  
		Last Modified: Tue, 16 Jun 2026 00:22:37 GMT  
		Size: 22.2 KB (22155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b967eb9014ecd390e52a6fae91486bdef2eb91ac554af8c4a70b1df24ee1a0`  
		Last Modified: Tue, 16 Jun 2026 00:22:38 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bc15f737dfe00d7db9c7a226e752125a44b66a6926b9d64ddb62219cb58574`  
		Last Modified: Tue, 16 Jun 2026 01:12:17 GMT  
		Size: 6.2 MB (6227338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb36c016e2a39c831e613e77572b1c605a6dffaa372ac220f1df41345acc13a7`  
		Last Modified: Tue, 16 Jun 2026 01:12:17 GMT  
		Size: 2.7 MB (2692697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e11ab4397b7677021a1d82f93ded696100af63a5caab5291f46f902cb4a1f`  
		Last Modified: Tue, 16 Jun 2026 01:12:17 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563f7476b1c5813754d46a7b6b6b418b17934aaeb61861d4af89b738c889bcb0`  
		Last Modified: Tue, 16 Jun 2026 01:12:18 GMT  
		Size: 14.1 MB (14087555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519da442c4016e706e23c32b6405df5a461d5d6a7357ffab1e53f1d016891d6`  
		Last Modified: Tue, 16 Jun 2026 01:12:19 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b942cd1db680ef69f878069e0d38a9b045dd32affa74d1364dbaddc3c6235725`  
		Last Modified: Tue, 16 Jun 2026 01:12:19 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b7903f5e3165555b6ed861c6bf6fd931e42f3aff81f9897f8d6b3f5cf4ef4b`  
		Last Modified: Tue, 16 Jun 2026 01:12:19 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:81ac599f39dd2545a02ca5845651d4a31011a47cab5b9156d83c412293e19b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5467db54c5f4c1f6560d365383c397ecfa4b415e83126754c1f6a35313771d56`

```dockerfile
```

-	Layers:
	-	`sha256:cfab34b9b391403075b8b3eedadcd5153e3acac763e8dcda0751d1a35e72c55c`  
		Last Modified: Tue, 16 Jun 2026 01:12:17 GMT  
		Size: 49.0 KB (49005 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:b42523e523aba4e79c2ca23d73fbec62cc3bcef9992290cdc4e4b6c994ef6caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52814500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd7216bcbb9a383dd500cb2249af393f5f61df3bb098bc7b67743731968011`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:22:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:22:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:22:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:22:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:22:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:22:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:24:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:24:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:25:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:25:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:25:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:25:01 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:25:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:25:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:25:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:25:01 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:11:26 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:11:26 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:11:26 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:12:02 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:12:02 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:12:02 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:12:02 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:12:02 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:12:02 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:12:02 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:12:02 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:12:02 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:12:02 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:12:02 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:12:02 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:12:02 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:12:07 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:12:07 GMT
USER root
# Tue, 16 Jun 2026 01:12:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:12:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d1d207c87ecb8483478cebba55e69d647f6ecedfc0da267d886cd8a000606`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 3.2 MB (3233760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1c123bfd6be24a667b3ccaccd14f406e2226ce5ab8c9346189dd55da240b2e`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e30dfd0f3a4543dd39f5a397924c79e7a82f96e265c437df4723245e323c12d`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4864a0c79d98806c1f9bbe2d7e6a9918ddf041c1d4045e7783b0a7c336b04a1`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 12.6 MB (12626306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e8df0c609282ee3a8107f5ad60ddd209b59614155ef0d3cc54ea86e17383ba`  
		Last Modified: Tue, 16 Jun 2026 00:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4689b77e96c6d5c2efc0bf61e8ead5fc85ceca449788503b307b6af2163680`  
		Last Modified: Tue, 16 Jun 2026 00:25:09 GMT  
		Size: 11.4 MB (11444360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c20a9f88ff092918443f6388d2a059e84be9fe5966c61570ab9fdb0e2d2802`  
		Last Modified: Tue, 16 Jun 2026 00:25:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d4624fa9ed346cf31dd73da2c70202d854ddfb30f63b4c3f464e9677e08de`  
		Last Modified: Tue, 16 Jun 2026 00:25:09 GMT  
		Size: 22.1 KB (22141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f618452ebb0124c504dd117a4b317514bcb0bc9e2ee8b43564ebb76cb45234e3`  
		Last Modified: Tue, 16 Jun 2026 00:25:10 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c285222c8cb5e18671f79f7007ae11796c2e2832df93a20ff5dde9f04bd54852`  
		Last Modified: Tue, 16 Jun 2026 00:25:10 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff751eb06b95d6b8f0c1d7f12c886e60b3ca8872c99128c7313b1a2d087c0676`  
		Last Modified: Tue, 16 Jun 2026 01:12:13 GMT  
		Size: 5.6 MB (5578269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa379d1503edb4831a84458cfc68cb5fcb5f12c5b9808cc8267f4516dc6f3b5`  
		Last Modified: Tue, 16 Jun 2026 01:12:13 GMT  
		Size: 2.5 MB (2521541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bba3d01634742b253f7470a1cd7964db4b0257c9d2892cccbf77b6156a6bc`  
		Last Modified: Tue, 16 Jun 2026 01:12:13 GMT  
		Size: 645.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96de7fdecc65cc72cfd7a9a477498679bedd5c8330d3f49b01877dbf98880a79`  
		Last Modified: Tue, 16 Jun 2026 01:12:13 GMT  
		Size: 14.1 MB (14087544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d581048e4fad96b734771d1eadb2469d86e7142064b93b88d2952f94f99ab3f8`  
		Last Modified: Tue, 16 Jun 2026 01:12:14 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a02cabc6d2ae8b0f38173ce7c59fa6e973a89be2f36641b4629f81ea0aa94e`  
		Last Modified: Tue, 16 Jun 2026 01:12:14 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe775d9b36f9ad73a511571541bfa6eaa2bcc93287e6fcee54ff1a0915a612b`  
		Last Modified: Tue, 16 Jun 2026 01:12:15 GMT  
		Size: 798.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:45f9d2af0f1e371d167d698927187b2b9f891da8b34e1b01a7bdf0e62073bb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf49a09064a2c374cd00b3e121deb6a031a37ac83453e4c7b7b9fce6988d0efc`

```dockerfile
```

-	Layers:
	-	`sha256:320a8af663e0b1b30fd3cb5f4a9aa3277fcc3eed312b09402313d00ad4c4eab1`  
		Last Modified: Tue, 16 Jun 2026 01:12:12 GMT  
		Size: 49.0 KB (49005 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:2fd7bc520738d7e01b696861b832c50fda7deab354ff5129539542e35a3f2b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57568152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1678afc6bff192db18d5a91346cd04e3926e35052099e6f5d333ec65e8f6682f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:13:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:13:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:26 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:18:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:27 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:18:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:18:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:18:27 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:18:27 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:13:46 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:13:46 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:13:46 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:15:22 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:15:22 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:15:22 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:15:22 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:15:22 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:15:22 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:15:22 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:15:22 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:15:22 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:15:22 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:15:22 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:15:22 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:15:22 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:15:26 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:15:26 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:15:26 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:15:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:15:26 GMT
USER root
# Tue, 16 Jun 2026 01:15:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:15:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20927fc874f68b1dfb3247c97d1e06a8d2fd122901377db2698427184e8b3740`  
		Last Modified: Tue, 16 Jun 2026 00:18:34 GMT  
		Size: 3.5 MB (3475810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293370315a62e3dcf82832aa1d28a17337a85a0b63cd5ed39705638e6ad97cab`  
		Last Modified: Tue, 16 Jun 2026 00:18:34 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b508e52c244a07c7e9d094ee31366105e64fc09fd6b131c52c05a7553b3c09`  
		Last Modified: Tue, 16 Jun 2026 00:18:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4c038ac2c897f69ac595a02197e5686e28c2a8d12f85998f1e2b17bbf9a4e`  
		Last Modified: Tue, 16 Jun 2026 00:18:35 GMT  
		Size: 12.6 MB (12626290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0387296813e0cc18bdbc9d044bfc24bdbb69c3336a1efc47c2bca2e2f2fab8`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d548ea984a73d437bfb41fed9ed29f55a7a3ef04990d7f1e924dadbf48216efe`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 13.3 MB (13319719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f72b5cf36b8130c8cef1124ee9f04692ffebc22c09aab85a5cef7179360dc50`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6d72804eec9407842761d3de63890c73006e23a639c2bb88f26669e3886537`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 22.2 KB (22155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8783d73bb465c7c28b5cb490d326631de541ad1b8a5acb17cefc380250af989a`  
		Last Modified: Tue, 16 Jun 2026 00:18:37 GMT  
		Size: 22.2 KB (22178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723df7026a14767594d3fa1282af584dce55902e0e31ac25c97347545487ad5`  
		Last Modified: Tue, 16 Jun 2026 00:18:37 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7283a502ccaf5f3998b152eefaca3e8e54a996989ccfdb2bd4eff8757f7890`  
		Last Modified: Tue, 16 Jun 2026 01:15:32 GMT  
		Size: 6.2 MB (6228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6415acbcce140eb788dfab72854466a91b668f3ca9b50923441ff9cb53749afd`  
		Last Modified: Tue, 16 Jun 2026 01:15:32 GMT  
		Size: 3.6 MB (3585132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9df0b8c93fcfb42f97319ee230daa59d1b1998f39dedad57f7567118142f04a`  
		Last Modified: Tue, 16 Jun 2026 01:15:32 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431f43c630d831a29301a3cacf98b127bf39c9f5c8e53e773a2cc7595bcfde8b`  
		Last Modified: Tue, 16 Jun 2026 01:15:33 GMT  
		Size: 14.1 MB (14087547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a25aabdbdb69f28996a0f5f42bfe73459aa15fcef5d944d7c9190655d61b601`  
		Last Modified: Tue, 16 Jun 2026 01:15:33 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd78ecf2abbb9b68ffa022f966eddaafce94f0c64b372bec65acc199b84f358`  
		Last Modified: Tue, 16 Jun 2026 01:15:33 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6237e0f494a035b9267e49e41a521ff0c92f20680cb21536370c4f626da0d6d8`  
		Last Modified: Tue, 16 Jun 2026 01:15:34 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:3f622d2726dd225bf115e6d9f756dea0d72233f164a139df0e79c6ba6987935c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a4fac0f70e03ba57f9f02d868f54abb75bef917a96391a93ae55a605623565`

```dockerfile
```

-	Layers:
	-	`sha256:c0228e1eaba3636863f1b14481882b8e68cdc5442d6485bec4245454743acc73`  
		Last Modified: Tue, 16 Jun 2026 01:15:32 GMT  
		Size: 49.0 KB (49035 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; 386

```console
$ docker pull phpmyadmin@sha256:74a2c8367b00ceffbe2db468b61612f02e246b832e9d56377c3fb63ad35d7b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57173978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ee07b6532f866bd444e090534bbccda8b2cf443584462649599e58e851c108`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:15:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:15:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:15:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:15:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:15:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:15:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:23 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:18:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:18:23 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:18:23 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:12:00 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:12:00 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:12:00 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:12:48 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:12:48 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:12:48 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:12:48 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:12:48 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:12:48 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:12:48 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:12:48 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:12:48 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:12:48 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:12:48 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:12:48 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:12:48 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:12:52 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:12:52 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:12:52 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:12:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:12:52 GMT
USER root
# Tue, 16 Jun 2026 01:12:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:12:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a1f87309f760a910a5f3b278d7e02cc9e41747bd6c7da50de79c37774b6ce`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 3.5 MB (3497309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c13d3f542289e7019282f796435ff5feb38ef94d23d9b02eee2f64fbf0ba597`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c86cc39b7afbf4033178653190199e70655723b408046cd102cb5b26e6654e`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193d558fad92af7cfba37bbb4d56f2b571ac60036f2046a008dcd58af1429bbb`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 12.6 MB (12626282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9deff40ff2ca9d43487cbbee0f4790fb1f54039f2f02b11c40bebdb9bf10a9`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b896f0235e2baf509bd727289de262d42e04c3ae687e43d227ad06ed065b4c`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 13.7 MB (13690201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55251fb34d4af4e5cb217d212ff8bbe79383d88299bbbd9d1fb704123ee2b627`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f82ae9a228fc1947483e8ea0561e89fd09612aa6d5430e7c46c6a0ea885e57`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 22.4 KB (22359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b7adc858c09e3ea06c23f6ffcae3eb1d73b8e22d73e517968a0f13a36dd972`  
		Last Modified: Tue, 16 Jun 2026 00:18:33 GMT  
		Size: 22.4 KB (22369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da74e87d8deff5e4a2df18810d36366b2ad620852aeac3b6e1d98ca55b8d2f97`  
		Last Modified: Tue, 16 Jun 2026 00:18:33 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3bd9acdc5a0904487b39df62596e1e5e27ad231ffd79593dd0e6fa5baa8b`  
		Last Modified: Tue, 16 Jun 2026 01:12:58 GMT  
		Size: 6.1 MB (6137972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a204a409a5008162c121f36180a9e7628bab47a456b28a4ceb07774359d499dd`  
		Last Modified: Tue, 16 Jun 2026 01:12:58 GMT  
		Size: 3.4 MB (3401971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e855cca029792e0dce59a640603de14a65ab00161c66f3913fe61d2edcb13c`  
		Last Modified: Tue, 16 Jun 2026 01:12:58 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad898a77857ecb77f9e04827b5c3098b70c7e36b41a3dbaf4673dc50cb95116`  
		Last Modified: Tue, 16 Jun 2026 01:12:58 GMT  
		Size: 14.1 MB (14087574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6ac597a2c61f39b8c545667016d134e1be9dd0d270fa3b3f711e5dac3e6d05`  
		Last Modified: Tue, 16 Jun 2026 01:12:59 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91022bf932e6c96b008d352677679e4667a4b045633058087c1f8a0f9d599ee6`  
		Last Modified: Tue, 16 Jun 2026 01:13:00 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b394fee9da101e41e108aafcd53865de86af3351eb7b463abc0a8b22df26802`  
		Last Modified: Tue, 16 Jun 2026 01:13:00 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:28c56dce549fc8dc4bf8f61e28f23eb2fd812957be789b3b40dc4b1b0f37391f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 KB (48848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de98957e8be04ad9a1d98529a19ade91cf16d7435f2dd943e4e5a7859bf54dfc`

```dockerfile
```

-	Layers:
	-	`sha256:ffc9567cb9809221b4facbce5d0ae62b3bfd0ca2ef7a35309046b22c6654cb9c`  
		Last Modified: Tue, 16 Jun 2026 01:12:58 GMT  
		Size: 48.8 KB (48848 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:ee22e516c4739fea64352a90046eb2f13cfed77337fb73e8303cb3c06320b6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57791099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bbf53459237fe67a15beba40d281db45143758957194f3042d54ac78f9d0e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:30:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:30:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:36:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:36:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:36:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:36:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:36:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:36:17 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:36:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:36:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:36:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:36:17 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:16:11 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:16:11 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:16:11 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:17:09 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:17:09 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:17:09 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:17:09 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:17:09 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:17:09 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:17:09 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:17:11 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:17:11 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:17:11 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:17:11 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:17:11 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:17:11 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:17:19 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:17:19 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:17:20 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:17:20 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:17:20 GMT
USER root
# Tue, 16 Jun 2026 01:17:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:17:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b9da4fa7a0b9d4db76eaa5e7475a9b26aebc92ecdbad7795d33e8c5862bfa`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 3.6 MB (3637828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72717bce2b969f044f4c03b530bca77062f0b0d4dfc1eb2f53b9a1459bcf77c`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecffaea7a9240f30a6d71b76e5cba5e41c27f6ab0409cce52536feeb7b55db`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82494c5f949127e6a8557f5449493de7a71bbcce098a218e56de562eb44fef3`  
		Last Modified: Tue, 16 Jun 2026 00:34:57 GMT  
		Size: 12.6 MB (12626311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d8eaaa90bb3f69b2f7b270337e96d5458cc1e911b9caf5f02575e1b9a3857a`  
		Last Modified: Tue, 16 Jun 2026 00:34:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626f1a2a1bcf9a7c85feab8a8e31f87e3f9727e526569b5b5459edf4a66236b5`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 14.0 MB (13984035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e2a9d220e12aa7b0cf3acf96ea52befedd7eb4fb76b5137fd6d60f0a240013`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3618b26084f12d36e6f16cf8d234e77d7dd155a6722c85875d5691d92a4d069f`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 22.2 KB (22191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa0599b7f093ac0f6eadd12b17a300095f127c1c9f101cde156f85eb562fd1`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 22.2 KB (22201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cd8d939820864a24757a485595c0ae431e462a8641d34cadb20cc6aa15b050`  
		Last Modified: Tue, 16 Jun 2026 00:36:31 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f563f23adb1ca2d0740050f537019654cbea466df6d3fce4c41047b4242a8d50`  
		Last Modified: Tue, 16 Jun 2026 01:17:31 GMT  
		Size: 6.4 MB (6446985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa5d34deb8fbd3d31ce94534594755337677d6d1d88f6c020560da1d54d0e4`  
		Last Modified: Tue, 16 Jun 2026 01:17:30 GMT  
		Size: 3.1 MB (3132780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c1735f9ec526fafe5fd8ea5393a1dc7589e08e8bd97eb341029f1309987b7c`  
		Last Modified: Tue, 16 Jun 2026 01:17:30 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8438cbb1dbe5d3ebbb0ee627edda8f6e9795718d035ebad9d17b70b6ba6d7f5`  
		Last Modified: Tue, 16 Jun 2026 01:17:31 GMT  
		Size: 14.1 MB (14087540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6acbfd25704f880f8d64d7b84698c0b0bcb8d4797e3e380e928b807fa1c710`  
		Last Modified: Tue, 16 Jun 2026 01:17:31 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc341d205a05c06cfade62165768d21699f52e270c5e3b3b79d79c1217e3f34`  
		Last Modified: Tue, 16 Jun 2026 01:17:32 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d7d74f0e2466150874131fe6762e7551e2d5112f5d343b45ff5bb76849a6e9`  
		Last Modified: Tue, 16 Jun 2026 01:17:32 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:00a3c925e8eeefc78a58dc582ec4f8ea0080d54d2fd3f43ed7a47078825b27cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a878ffd3464c73c1c52ae0082c1b8f66c930e675fa18de609e874452aad2ce`

```dockerfile
```

-	Layers:
	-	`sha256:c0754a455261f6d2d7d4cfcc1526a5ce4240889d1a3ee647f85f4212b7b40ac5`  
		Last Modified: Tue, 16 Jun 2026 01:17:30 GMT  
		Size: 48.9 KB (48936 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; riscv64

```console
$ docker pull phpmyadmin@sha256:5740b20ae83e1d9dc8dc699799f5d97c93a9c14b483a35b0998385e074b948d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58128977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b36662bde6bfee6784f8cf3e96bd1c061e3de16eb234a427f9d9502f047ef7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 04:52:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2026 04:52:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 04:52:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Sun, 14 Jun 2026 11:02:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sun, 14 Jun 2026 11:02:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 14 Jun 2026 12:49:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 14 Jun 2026 12:49:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 14 Jun 2026 12:49:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 14 Jun 2026 12:49:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 14 Jun 2026 12:49:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 14 Jun 2026 12:49:12 GMT
WORKDIR /var/www/html
# Sun, 14 Jun 2026 12:49:13 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sun, 14 Jun 2026 12:49:13 GMT
STOPSIGNAL SIGQUIT
# Sun, 14 Jun 2026 12:49:13 GMT
EXPOSE map[9000/tcp:{}]
# Sun, 14 Jun 2026 12:49:13 GMT
CMD ["php-fpm"]
# Sun, 14 Jun 2026 14:21:24 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Sun, 14 Jun 2026 14:21:24 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Sun, 14 Jun 2026 14:21:24 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Sun, 14 Jun 2026 14:27:54 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Sun, 14 Jun 2026 14:27:54 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sun, 14 Jun 2026 14:27:54 GMT
ENV MAX_EXECUTION_TIME=600
# Sun, 14 Jun 2026 14:27:54 GMT
ENV MEMORY_LIMIT=512M
# Sun, 14 Jun 2026 14:27:54 GMT
ENV UPLOAD_LIMIT=2048K
# Sun, 14 Jun 2026 14:27:54 GMT
ENV TZ=UTC
# Sun, 14 Jun 2026 14:27:54 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sun, 14 Jun 2026 14:27:54 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sun, 14 Jun 2026 14:27:54 GMT
USER www-data:www-data
# Sun, 14 Jun 2026 14:27:54 GMT
ENV VERSION=5.2.3
# Sun, 14 Jun 2026 14:27:54 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Sun, 14 Jun 2026 14:27:54 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Sun, 14 Jun 2026 14:27:54 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sun, 14 Jun 2026 14:28:15 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sun, 14 Jun 2026 14:28:16 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sun, 14 Jun 2026 14:28:16 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sun, 14 Jun 2026 14:28:16 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sun, 14 Jun 2026 14:28:16 GMT
USER root
# Sun, 14 Jun 2026 14:28:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 14 Jun 2026 14:28:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1dc2b0247d9ffb9aa950846edb9cd66b4f53852a8a9879e3b90eab1e6b59a`  
		Last Modified: Thu, 11 Jun 2026 06:26:26 GMT  
		Size: 5.8 MB (5791702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6ded20d49de2d129bbc9f97fb6b326363a5b54d9bd6c73e47dee306b314693`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f977f288e84989a2379a82f5f4195784dcdf513d90a9d1c0069a2c531162f0d`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb72ded20015bbf425de81640879dc35e30985449852003a63bbb49d68937ab8`  
		Last Modified: Sun, 14 Jun 2026 11:56:08 GMT  
		Size: 12.6 MB (12627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b61b90be991058d2579c52c0d888e6f5943171aa51e2999b5dd56ac53b3ed10`  
		Last Modified: Sun, 14 Jun 2026 11:56:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1991f503c9693c1bb647c85c8de930350356b7c11a4e98f59dcc9c04bbc74cb`  
		Last Modified: Sun, 14 Jun 2026 12:50:03 GMT  
		Size: 12.8 MB (12828411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab88bf6134cfbc374e2434116a714f4f1fcd3ad378ce24440f74d5006dc074c9`  
		Last Modified: Sun, 14 Jun 2026 12:50:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e8eec18ec4ae32e634a4b6112cd208dfc83dd2a254552572ef154bb2745ec`  
		Last Modified: Sun, 14 Jun 2026 12:50:01 GMT  
		Size: 23.1 KB (23050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb86f88f3436dd6cbdb0c874d53eb3b472ca36501e977aba29df270f72a7025`  
		Last Modified: Sun, 14 Jun 2026 12:50:01 GMT  
		Size: 23.1 KB (23070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81cc5f7f69b7f168c967f5afc69829f52f44f908699a03e8e0ea32312fb4fbc`  
		Last Modified: Sun, 14 Jun 2026 12:50:02 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b745ffe973ba44467a44138228923b3bee0a3742967a0cdad2c956e660839fb`  
		Last Modified: Sun, 14 Jun 2026 14:29:00 GMT  
		Size: 6.3 MB (6291037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f074ec9acfe3977a5d51b6181e4c2eef17d283251e42d5be00775c648db45fad`  
		Last Modified: Sun, 14 Jun 2026 14:29:00 GMT  
		Size: 2.8 MB (2847358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ea7b19a9124d688a92d67b2c6500797403d42ed890e4b5f4a17c650e4a3682`  
		Last Modified: Sun, 14 Jun 2026 14:28:58 GMT  
		Size: 647.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880487a9f0b47a4e7f7ebbce37c2cd010ed17db372f290de112e644cef670359`  
		Last Modified: Sun, 14 Jun 2026 14:29:02 GMT  
		Size: 14.1 MB (14087544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3cd849e9c701d5d4cd6046beffb3830c15a6c297ad5583008e2c8844dbeee`  
		Last Modified: Sun, 14 Jun 2026 14:29:00 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b996719eb96e004e427a86ed3d67c6802c51e0638f5265fe1384e4360d15b`  
		Last Modified: Sun, 14 Jun 2026 14:29:01 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72ca5d60c92f341b08b3a1bd35895fca1ab70d826c18a21d766d405c6d63814`  
		Last Modified: Sun, 14 Jun 2026 14:29:02 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:285c8e5c8e892d352125e70b19e6e582f39c7ce64e031238491a1fa34fb26388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c70ffb6e29eeaab3214e786bfc9b0cd42f52ff6f254317162f2e35c8ba070d`

```dockerfile
```

-	Layers:
	-	`sha256:d73222918c8d5ec3980264304422de9c44016306302efe24c41e59d91956bab8`  
		Last Modified: Sun, 14 Jun 2026 14:28:58 GMT  
		Size: 48.9 KB (48936 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:838ee0fc7d671e5f14aa871f1e43c0fbe3f511d10a333dfe018361bacbe41f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56867859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74985e64267fb965fd2fe9584026f5c95fce753b0720f3128699fab66b06ed73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:23:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:23:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:27:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:27:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:27:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:27:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:27:59 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:27:59 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:27:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:27:59 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:27:59 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:36:35 GMT
ENV UPLOAD_PROGRESS_EXT_URL=https://github.com/php/pecl-php-uploadprogress/archive/refs/tags/uploadprogress-2.0.2.tar.gz
# Tue, 16 Jun 2026 01:36:35 GMT
ENV UPLOAD_PROGRESS_SHA256=fe3f6cdfcedad563c970c4fd1cda31e422cfc0df5cc9a217d8c80ed3c8d137f5
# Tue, 16 Jun 2026 01:36:35 GMT
RUN apk add --no-cache     bash     tzdata     gnupg # buildkit
# Tue, 16 Jun 2026 01:37:12 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         mkdir -p /tmp/uploadprogress;     curl -fsSL -o /tmp/uploadprogress/uploadprogress.tar.gz "$UPLOAD_PROGRESS_EXT_URL";     echo "$UPLOAD_PROGRESS_SHA256 /tmp/uploadprogress/uploadprogress.tar.gz" | sha256sum -c -;     tar -xf /tmp/uploadprogress/uploadprogress.tar.gz -C /tmp/uploadprogress --strip-components=1;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath         /tmp/uploadprogress     ;         rm -r /tmp/uploadprogress;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:37:12 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Tue, 16 Jun 2026 01:37:12 GMT
ENV MAX_EXECUTION_TIME=600
# Tue, 16 Jun 2026 01:37:12 GMT
ENV MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:37:12 GMT
ENV UPLOAD_LIMIT=2048K
# Tue, 16 Jun 2026 01:37:12 GMT
ENV TZ=UTC
# Tue, 16 Jun 2026 01:37:12 GMT
ENV SESSION_SAVE_PATH=/sessions
# Tue, 16 Jun 2026 01:37:12 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Tue, 16 Jun 2026 01:37:12 GMT
USER www-data:www-data
# Tue, 16 Jun 2026 01:37:12 GMT
ENV VERSION=5.2.3
# Tue, 16 Jun 2026 01:37:12 GMT
ENV SHA256=57881348297c4412f86c410547cf76b4d8a236574dd2c6b7d6a2beebe7fc44e3
# Tue, 16 Jun 2026 01:37:12 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.3/phpMyAdmin-5.2.3-all-languages.tar.xz
# Tue, 16 Jun 2026 01:37:12 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.3 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Tue, 16 Jun 2026 01:37:16 GMT
RUN set -ex;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Tue, 16 Jun 2026 01:37:16 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Tue, 16 Jun 2026 01:37:16 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Tue, 16 Jun 2026 01:37:16 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:37:16 GMT
USER root
# Tue, 16 Jun 2026 01:37:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:37:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1478be2c88d13000249832224bb580b87a524c10ccf140e1f65943cb33f59eb`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 3.7 MB (3651068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4532b14d23ad0cd16945b31df22f9a393cc7b3b64f7aa7fa62ade4877c52fad9`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d62373606e3c4c1b6fef638aa78a6674eda0089fb632b2f1eaa05c504adeec8`  
		Last Modified: Tue, 16 Jun 2026 00:17:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb960454a3a050789ebff09c3493b411132f19ccb0fad82bdc05f469cc39b14`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 12.6 MB (12626287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba72edc733fc0cf03ed9d8998ab076026ebaead0f7aa5ae3c4c13d4692c261c`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb211e10020f5ebe101b302143029b923096e937408f968683a38637229ebb8c`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 13.3 MB (13280099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d543d076e4dee58b3803c228720fc1c76d849a906875d8396e78a34caf72871`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843bf5fbcb8266a4d5d7e7668e571950c294d8dd56704d1a14e671fe1f2a8a5f`  
		Last Modified: Tue, 16 Jun 2026 00:28:12 GMT  
		Size: 22.1 KB (22134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f205ffc785403ee30b26f6ec7ee5795b1ef9ed4ee89d67f4871d1b4dd8c4cd`  
		Last Modified: Tue, 16 Jun 2026 00:28:12 GMT  
		Size: 22.2 KB (22158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9d045787fa842d15e34a5d5736ed9027130ae88c2e6f47c13487fa54adf99`  
		Last Modified: Tue, 16 Jun 2026 00:28:12 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412feb2c54ca299dd96f438c574dc999d6ab971be1d3cdaf8d9cd505c4918fa4`  
		Last Modified: Tue, 16 Jun 2026 01:37:26 GMT  
		Size: 6.5 MB (6452112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7ea4cec534b17a4f293a716c55be64aaf2ab1484de60914b75feaa9077d55`  
		Last Modified: Tue, 16 Jun 2026 01:37:26 GMT  
		Size: 3.0 MB (2999319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eadf28976cb2c743ab3bdfea58eb784ebb85842b7b58e2a04a0115c57d158d7`  
		Last Modified: Tue, 16 Jun 2026 01:37:26 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba58e0922af6e10a5fef047ff8be16cba917641c276d60808b6e1c94a7ef441c`  
		Last Modified: Tue, 16 Jun 2026 01:37:26 GMT  
		Size: 14.1 MB (14087552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe819f8aa66f31d3b0ce6dc9ce4d6cf846e0b5478fc7a987af326e55c65de53`  
		Last Modified: Tue, 16 Jun 2026 01:37:27 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cdcfada11248a37d01facc0cd1747f7e9565408edbc808ed8999cccb572bc`  
		Last Modified: Tue, 16 Jun 2026 01:37:27 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadcf77a9418ef036db1c3250e551f83be4303f6c6c049aaecc34d15b3d15e9e`  
		Last Modified: Tue, 16 Jun 2026 01:37:27 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:95871142a2c489cfff16ef00775e379e4b828384ed4fe24d5dbe1fca6d92a05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 KB (48885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bde903141cecc260c9a9142e98c84a36f1c6b03f7605915ee5887ae980f046`

```dockerfile
```

-	Layers:
	-	`sha256:14ab7152316a597ffc40f87001d0c765e7a1775adbf4770a931086c09d8364db`  
		Last Modified: Tue, 16 Jun 2026 01:37:25 GMT  
		Size: 48.9 KB (48885 bytes)  
		MIME: application/vnd.in-toto+json
