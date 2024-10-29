## `phpmyadmin:5-fpm-alpine`

```console
$ docker pull phpmyadmin@sha256:c0a6d052d5642a92bd9dae029519429bfa8547e5b187be18b2fc1cf4f2ec8754
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `phpmyadmin:5-fpm-alpine` - linux; amd64

```console
$ docker pull phpmyadmin@sha256:9f46fad063ffaf22cb40f0ce2478c3e7bd9ed946104ed5c797041ae2d896b7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39107ae887952cea2b7feb188f4bb5ed521481f339e14ebb9d803b8f93f45ced`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96c133c922f31d894927d21653257cd3a5e513104e98d3113e71a7f2c468fb8`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 5.6 MB (5581747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a48dc562ccff6cead7d519237bfdc3c0af9620b096bc49eca49ab8957b1547f`  
		Last Modified: Mon, 28 Oct 2024 22:12:41 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b839206006f2e1fbfd5f5a77e5723c17e2a11d0734b32876ca470c91d85ab`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8dbd39ff5c723a88089fecc98a42a6daa8835a3a4687e11f4de519ac28b02`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.1 MB (12147074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbefb29232519b0a6e5eb4e2ddd28d8c41dbc5e644962bc0f66e8411020cef8`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c975d8003efe68103d60ab404d799e396b4b4b6b432edc40871e78618a76d5`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 12.9 MB (12871627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a153f77c1fbcc4d80c684cec11ac99dbd20757b879a39398e746e8e0964bbcac`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d809165e09ce21422394fe4ecda27388328804c6734f63a8240686b68aa2ca`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 19.7 KB (19655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8ca7d8e061cf75da7c2837903eaf56575ca36dc6143711a67b269047ed0a50`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a1d6105b16c71e1b869ae08da930ce921ac3d99711a73abbf7d546e2543fb`  
		Last Modified: Mon, 28 Oct 2024 23:01:58 GMT  
		Size: 645.5 KB (645461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7002741564882c74921083abc58008932594f1ad6bd054e9c9eb51734d6c5da`  
		Last Modified: Mon, 28 Oct 2024 23:01:58 GMT  
		Size: 3.3 MB (3281552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba309145c74ec5bb8b5a2fbaa1eb946297c26e1e876df9aca1c10c53a8daf7`  
		Last Modified: Mon, 28 Oct 2024 23:01:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f38a328e6ddb8f70a623a50c21eba256039e9f759f3d372c3aee13361770d5`  
		Last Modified: Mon, 28 Oct 2024 23:01:58 GMT  
		Size: 12.7 MB (12718316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d14541b6ce638381a54168a0b0bacc1d96409413d2801601c50e227c7853f8`  
		Last Modified: Mon, 28 Oct 2024 23:01:59 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fece10e971a32616094a9628cf9589ee9190cfd81987af76a68425ec61e254b6`  
		Last Modified: Mon, 28 Oct 2024 23:01:59 GMT  
		Size: 784.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:3bc3f8489610669e4fb3bdbec81593137af03bceed1b8b1211fa0da40bbb9981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08901644d53ee2230b3cf9106b6462729d0f816fbcca5c1ae06dae9f91c198e`

```dockerfile
```

-	Layers:
	-	`sha256:0918652723e9f96c6fc9c05cf6e93f21b46cf281722819d7b33bab0670266a5f`  
		Last Modified: Mon, 28 Oct 2024 23:01:58 GMT  
		Size: 40.9 KB (40906 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull phpmyadmin@sha256:a02d2a84f5e9a00bb05387bd5aabc7c3973030cdec348582ceb6a8a3603711c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48563143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d37042a718820fde17023f385ab7ae293f00b1d69f00df02bc565051d14a357`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077201e66b85be92a47e209273e3a746b6c9fb70abe63fc08fcfdbc9d9725801`  
		Last Modified: Mon, 28 Oct 2024 22:05:27 GMT  
		Size: 5.2 MB (5235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f342726194a9999ab374184edacbc753de40c600fb9b4e9fedc6d530e054ad2`  
		Last Modified: Mon, 28 Oct 2024 22:05:27 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e58cbafd5fc0f6e2372ba8b7dea44a4ee3ddb23dc907076855de93848d047`  
		Last Modified: Mon, 28 Oct 2024 22:05:27 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c20a5dad4f80fb0ace4677169f2947cb5cc21cbeef04e3cad663537c80a90a7`  
		Last Modified: Mon, 28 Oct 2024 23:08:05 GMT  
		Size: 12.1 MB (12147067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0712a76b7e6f7f918b4b1a7d005b928915e8d0903e7f4df292ed65a08b37913e`  
		Last Modified: Mon, 28 Oct 2024 23:08:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34199219341bab36db21bed0e00ed37001d3734917b9efc69c4109f8cfb76639`  
		Last Modified: Mon, 28 Oct 2024 23:12:41 GMT  
		Size: 11.7 MB (11715330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caa71f68c6ef2dddda7fe1327ad950ffd0baa908d1b8727148284d2ebc5334c`  
		Last Modified: Mon, 28 Oct 2024 23:12:40 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4595b0cdcd4175e744216c51f4955e286456fe39af427df360ec74b2bd7f10`  
		Last Modified: Mon, 28 Oct 2024 23:12:40 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25155efc28938d754ad52d82b11365a30a25cd19536a560e26bfd5678fc90ec`  
		Last Modified: Mon, 28 Oct 2024 23:12:41 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dc814150262f0d4763011df2216adf0ee996bf42b784f395849a88729dafd1`  
		Last Modified: Mon, 28 Oct 2024 23:59:13 GMT  
		Size: 645.7 KB (645668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6a92305bb865c21c96ae4f4d02a5d1e5bf4f853c005de2e25741817524da25`  
		Last Modified: Mon, 28 Oct 2024 23:59:13 GMT  
		Size: 2.7 MB (2699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea7ba8dbb60358e8f7d926643c6a8308fa39f18797fd88c5f6af751691035e7`  
		Last Modified: Mon, 28 Oct 2024 23:59:13 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b12cac2e06f4ee260fb038e5eb2d098fb4c4b47a0c3eab82590e4949bfd3a2`  
		Last Modified: Mon, 28 Oct 2024 23:59:14 GMT  
		Size: 12.7 MB (12718140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab29232eb0ad5688b8f6519dda01ab22c89f2cc62cfbafd4fa02d77150d56bbd`  
		Last Modified: Mon, 28 Oct 2024 23:59:14 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c740dbfaf555e65e3cf0f8a9e5f171f6998935f687136e894b641a0441a0ef`  
		Last Modified: Mon, 28 Oct 2024 23:59:14 GMT  
		Size: 783.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:bb35ff7b079441624feb1f2037dd8cf65813810593ea56928ec79012b0ff1a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 KB (41063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f05cf589bc44d5d1db5288aad809ce4359e0287e2d611ddc3754ccc16d6c667`

```dockerfile
```

-	Layers:
	-	`sha256:4c759fb701a03ad4b4ab053d2e6904db26e9b1797cdbac8f822bcea7b37fc983`  
		Last Modified: Mon, 28 Oct 2024 23:59:12 GMT  
		Size: 41.1 KB (41063 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:c2abd14ac5ec3008b5543fdf81a3fddd7ffc3668178afef680e1a4210fbf8724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47001877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8e0941c682d331d13dc6b04c611d5918c0b181e66e6f6958b96f8a80fe5f25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
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
	-	`sha256:b296d94ba43ef9447649c1c80dbaafb2d8e665687caf5b5a173a5e7b676a409c`  
		Last Modified: Tue, 29 Oct 2024 01:55:49 GMT  
		Size: 606.0 KB (605950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396f606d43389c215b888c4c1178966c61274863df1a27049f42c9588595e514`  
		Last Modified: Tue, 29 Oct 2024 01:55:49 GMT  
		Size: 2.5 MB (2525377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8ee90a815004476748b8f12e9b88ed232780cc13e45e8c5b6596dcc20a9bc`  
		Last Modified: Tue, 29 Oct 2024 01:55:49 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd94f732f6dab712d19f5f0ed8e586b09a9dacdf31a67f9328b25c23fccb4e4`  
		Last Modified: Tue, 29 Oct 2024 01:55:49 GMT  
		Size: 12.7 MB (12718165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be8f173f70e9828f4a0c66e95e464004006494276e1a4dd5b483b40f51bb34`  
		Last Modified: Tue, 29 Oct 2024 01:55:49 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f5035063297f6ecbe592af5476ff0e5192a0e0bdc7f4ceb86e88cedf394700`  
		Last Modified: Tue, 29 Oct 2024 01:55:50 GMT  
		Size: 783.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:1cd0b513969bac84133f2c695926177e67ce6985b40125ec7fa31b3d7b616783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 KB (41063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c650dd950f4e9699fc6e1377949e6d04e14f7d6484bc67d843ff53c85e8d7e98`

```dockerfile
```

-	Layers:
	-	`sha256:3d50eca2ab3e90f54b41a987cb7f85bc2949790ec0d53ab82668a73c33568a67`  
		Last Modified: Tue, 29 Oct 2024 01:55:48 GMT  
		Size: 41.1 KB (41063 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:fdc544b34b525c196595d8d92b2c69fbd2971d8cced8ff86559a62eb6719dfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52294203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79010c35f5dfb6334a66ab7c7bb19055d696be48d8773a2b798e4bf6563a0065`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
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
	-	`sha256:e2cc08a4cc4b148054d2e428a48a985493d8c4613e15165a4ceace74a71d0f75`  
		Last Modified: Tue, 29 Oct 2024 01:58:41 GMT  
		Size: 708.0 KB (707979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c345f9669cf786b2f5fc2373e1cadc5f7f0a42bf1b2c59876f9cd25da57f70`  
		Last Modified: Tue, 29 Oct 2024 01:58:42 GMT  
		Size: 3.6 MB (3613695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372d0aa232be085ffea390c02b64b41531a9038c5f3e4473cc9085cb6d6dd91`  
		Last Modified: Tue, 29 Oct 2024 01:58:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4c6dd309d16950541f5a07fef09adccf943e35c9b270ec4a34f4bc886c3c59`  
		Last Modified: Tue, 29 Oct 2024 01:58:42 GMT  
		Size: 12.7 MB (12718180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a8aa5f476c094108f3450598ee0009df81de4e46079051eef14dc16d577bcd`  
		Last Modified: Tue, 29 Oct 2024 01:58:42 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a229136480c64f1e065368bc530c6d1615b638e51224a93df29fdcd8a9230a9f`  
		Last Modified: Tue, 29 Oct 2024 01:58:43 GMT  
		Size: 784.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:5a4c2cae4d17ca351aecc21138966551e049ddd8af07c21b4b5195365e12d7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 KB (41097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a104eb0ac7e4c158dffbe9f1f46c7c42d79fcac233c8f65e838ac955f7406d5c`

```dockerfile
```

-	Layers:
	-	`sha256:312675bf3162e822265c6c5aba7c1a71f6b5c86bca7ecf81f524d5f846e0a08b`  
		Last Modified: Tue, 29 Oct 2024 01:58:41 GMT  
		Size: 41.1 KB (41097 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; 386

```console
$ docker pull phpmyadmin@sha256:9a276e3f50e5e46e63dd4f32795477670e93e1fa9da5f887bc38787c6b3867a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51070533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3114ad92b67c7b588388ec36bd64e54a2d6d7301456545d8e29ec7049477910d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5010c9b606bb9db110c7427a2cfd2620e3bc364ac6b6f3c40af793a0d43de6b`  
		Last Modified: Mon, 28 Oct 2024 22:12:49 GMT  
		Size: 5.5 MB (5465522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d170351fa783a7acacbc3f02a536854413e14ad75fe8230087412cf96fa62d3`  
		Last Modified: Mon, 28 Oct 2024 22:12:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a26f6b065abf5cb6de23f0d808247a6f93a7c608505944f4f0ed99b5ae82e3`  
		Last Modified: Mon, 28 Oct 2024 22:12:48 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22018d92b0452e597a5ce3ab2bbadc2adfd29ecda38ce08e16ca1c96f1a1624a`  
		Last Modified: Mon, 28 Oct 2024 22:12:49 GMT  
		Size: 12.1 MB (12147063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae05d380a3fb3e954e23adafe496e00b0eae294472b09bbd6408f65e903fb7d`  
		Last Modified: Mon, 28 Oct 2024 22:12:49 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a302f8c9e1ab598a36dde4ff174cde78fb277b71cc207349b5a193ef2f3338e`  
		Last Modified: Mon, 28 Oct 2024 22:12:50 GMT  
		Size: 13.2 MB (13222446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b509a41d49c96a34a0d47a7a4c708e8574b2fad731a64b61fdc6d15440dd597`  
		Last Modified: Mon, 28 Oct 2024 22:12:50 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3adc4e9ba20ed3a91c9776983f143a400e0e11992ab23b19dcbe110c38a0d1`  
		Last Modified: Mon, 28 Oct 2024 22:12:50 GMT  
		Size: 19.6 KB (19650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefb63cfb655bc16cd52a4daaa1164173544b30fe66c3a86199a6905352c3834`  
		Last Modified: Mon, 28 Oct 2024 22:12:50 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24a33e6bea522504fd0c3c2ba65ab6deadc81444babe8cdcc1fdae04f8ac0a`  
		Last Modified: Mon, 28 Oct 2024 23:02:07 GMT  
		Size: 653.4 KB (653359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfc26183f85c1534f5d413f75d0688be15fe235de0f6d84ff123560fb24f5e8`  
		Last Modified: Mon, 28 Oct 2024 23:02:08 GMT  
		Size: 3.4 MB (3358799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7dcc15a48b91be8dd4ea4ed34380134c5299cbdaa57a5ace935647672b332f`  
		Last Modified: Mon, 28 Oct 2024 23:02:07 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2e13653c9cee491e2066fa84efe467ea6f41c8960aa0e3fbf8c26f0a903d1b`  
		Last Modified: Mon, 28 Oct 2024 23:02:08 GMT  
		Size: 12.7 MB (12718276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160075c66e0f6fa32c9bada27bc4b1b5d69fb486795dc51fe52d884eac73923a`  
		Last Modified: Mon, 28 Oct 2024 23:02:08 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd3ef39272956898439df27d0f2ffdd05d9f49c2e41ee76b4d54877cc84524d`  
		Last Modified: Mon, 28 Oct 2024 23:02:08 GMT  
		Size: 784.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:42acf3225d7b954ceed63aab57ba05e81c455f49520c3bc60894ed66a6a9fa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47daf02afc73dfe7856da298859301f64c587ad95746dbc7a2f1407b287b9b76`

```dockerfile
```

-	Layers:
	-	`sha256:dc691206f11c025b47f2c56fbfe3ed5e1272920667b72e3ea49bfedfd45fb158`  
		Last Modified: Mon, 28 Oct 2024 23:02:07 GMT  
		Size: 40.9 KB (40867 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:a1d37243dada1d58747e69114b92263fcd0c70b752c6072a8455e742838dab1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51249576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe744474d9d6f369b6a5b87333e15a28d0eff2802b30629c24cbf7b8d88d1224`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba6d71b7953e5a539b29c94897df8abc5c8913c9f8cdd74dbe70ff782c2c41`  
		Last Modified: Mon, 28 Oct 2024 22:19:56 GMT  
		Size: 5.6 MB (5569355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e67a84c448da04979ae1b4f74b62a87996c3c2cf1c1638e98af4254a5cb01a0`  
		Last Modified: Mon, 28 Oct 2024 22:19:56 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6cb5989066db70ae6367501c203d0179801d5021cba5499e956b2f3adf9274`  
		Last Modified: Mon, 28 Oct 2024 22:19:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a295d3d154ccd66fa8a5d29c34ed4749e640184bf0a77e40ae7c40031fcb31`  
		Last Modified: Mon, 28 Oct 2024 23:28:04 GMT  
		Size: 12.1 MB (12147070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6feede72bc57d45c539a8c7a9d2603289e42c7c7e60dbaea3735de7683fb911`  
		Last Modified: Mon, 28 Oct 2024 23:28:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab667e0e41b7d2913cfbc9cf7ef923cc361ceb0d221cd889b9dfd17182e20c2`  
		Last Modified: Mon, 28 Oct 2024 23:31:06 GMT  
		Size: 13.4 MB (13367120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704ca06873e3dcdf12afaa067ecc2e3158ddd1ea1b7f9f5ef1707eb61ddbd2bd`  
		Last Modified: Mon, 28 Oct 2024 23:31:05 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d10e2dcbcd55645a6c4ea578cfc4205eda7454b217dd56ef62a294556207a0b`  
		Last Modified: Mon, 28 Oct 2024 23:31:06 GMT  
		Size: 19.4 KB (19428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ae3702b3b68842f499e80a580c5290d9a68c7442d10026dcf40e24d322402d`  
		Last Modified: Mon, 28 Oct 2024 23:31:06 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32823e59c1756b93dded81393ea5a19c393894f1005110a675f1289e39346ea5`  
		Last Modified: Tue, 29 Oct 2024 00:27:54 GMT  
		Size: 711.8 KB (711778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3021fbdb6c96e1851e1608eb63adcad3ad859c232f3e4b073a2ba6e3a6dfa0ca`  
		Last Modified: Tue, 29 Oct 2024 00:27:54 GMT  
		Size: 3.1 MB (3128001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e35c4021a30b8368d92780967d1e1cec02070901fa3898fa4128d7fdfafce54`  
		Last Modified: Tue, 29 Oct 2024 00:27:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9831e765f1b993de250bdfcfea7a7595a5e108a21450d84fec3b604bc15002`  
		Last Modified: Tue, 29 Oct 2024 00:27:55 GMT  
		Size: 12.7 MB (12718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d711768d12faa92a0358b29f093768c5e3a6b4fbf91b201dee2636ee716ba8`  
		Last Modified: Tue, 29 Oct 2024 00:27:55 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb007073b982d3f14485d1def1cb10f01b263dbc5f867d273923f1d2335916a`  
		Last Modified: Tue, 29 Oct 2024 00:27:55 GMT  
		Size: 783.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:4c8b3740ee06da666d16306590e4b068ccfa086fded9e60b95249d763d3280b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4688b57905cfd62b4a67caa9e4c4c72bdb837003838727fa4de8578feac0f357`

```dockerfile
```

-	Layers:
	-	`sha256:a748c2387115b3b30e74289a1cdc980e07af398d1d573d1985451e2f14cbaa9e`  
		Last Modified: Tue, 29 Oct 2024 00:27:54 GMT  
		Size: 41.0 KB (40998 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:5-fpm-alpine` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:fc2ff0fc324c5dbee70aa3ed53fe08fa6d43061eb8545c0e23ea623eb8039998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50426309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196ab00fedf365df523e0d000576776d001b1181b6556c840771b02b1b9a3a73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 Jun 2023 11:51:41 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["/bin/sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jun 2023 11:51:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_VERSION=8.2.25
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 30 Jun 2023 11:51:41 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jun 2023 11:51:41 GMT
WORKDIR /var/www/html
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jun 2023 11:51:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jun 2023 11:51:41 GMT
CMD ["php-fpm"]
# Fri, 30 Jun 2023 11:51:41 GMT
RUN apk add --no-cache     bash     tzdata # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         bzip2-dev         freetype-dev         libjpeg-turbo-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .phpmyadmin-phpexts-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 30 Jun 2023 11:51:41 GMT
ENV MEMORY_LIMIT=512M
# Fri, 30 Jun 2023 11:51:41 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 30 Jun 2023 11:51:41 GMT
ENV TZ=UTC
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SESSION_SAVE_PATH=/sessions
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENV VERSION=5.2.1
# Fri, 30 Jun 2023 11:51:41 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Fri, 30 Jun 2023 11:51:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Fri, 30 Jun 2023 11:51:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 30 Jun 2023 11:51:41 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         gnupg     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 30 Jun 2023 11:51:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 Jun 2023 11:51:41 GMT
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
	-	`sha256:c199e786d1006a18314af334ad395dd85f7b72e2c287cb879145630a7a45256c`  
		Last Modified: Tue, 29 Oct 2024 02:06:53 GMT  
		Size: 674.9 KB (674925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24d5c143eac191d3b7ccb3a6844a5dbce2c657af4b2d0a09b9425a3fdddc708`  
		Last Modified: Tue, 29 Oct 2024 02:06:53 GMT  
		Size: 3.0 MB (3018991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521c391164c32d48170302dddf142584d0859a270916f2fcd1a8a279503215f4`  
		Last Modified: Tue, 29 Oct 2024 02:06:53 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255088f6bc6cc0a978f010a9b32610db38fd3d61fbbd1185312946602e7ac2e`  
		Last Modified: Tue, 29 Oct 2024 02:06:53 GMT  
		Size: 12.7 MB (12718161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bfc25adaab81872f10f85c04d3b4287e202b2a09e6c3cef45fe2c80e0229e6`  
		Last Modified: Tue, 29 Oct 2024 02:06:54 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f46ec449989376d5860ed51181282d8acf0991389119c7693cbfb5a90e390`  
		Last Modified: Tue, 29 Oct 2024 02:06:54 GMT  
		Size: 784.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:5-fpm-alpine` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:a5a3d0ee2109046906ab766f09c915f92ead20d64b30206b63dfb42a4fb85e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b747164d53ae30b8e99d52bde5e5d0ee7af62781f570732a8b9e12bd943ed2`

```dockerfile
```

-	Layers:
	-	`sha256:b253c70bafe3e7d79a8fcc3b0d9036243ee33b6db53d592521174059bebe443b`  
		Last Modified: Tue, 29 Oct 2024 02:06:52 GMT  
		Size: 40.9 KB (40948 bytes)  
		MIME: application/vnd.in-toto+json
