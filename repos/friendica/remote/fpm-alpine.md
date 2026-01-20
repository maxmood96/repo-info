## `friendica:fpm-alpine`

```console
$ docker pull friendica@sha256:ca412b6e6fceec1b0914ef3a705be7a80b95c02bd4f981aeabeebb87274e3676
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
$ docker pull friendica@sha256:cced811d402a74109822dacad961ba4020458382428be9f3519ea242aff59653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116402978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1265c589dfc4122b15b6e9b82f2a684630825752af553816f562794cc882f2b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:17:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:17:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:17:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:17:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:17:34 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:17:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:17:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:20:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:20:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:20:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:20:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:20:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:20:17 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:20:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:20:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:20:17 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:20:17 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:32:17 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Fri, 16 Jan 2026 23:32:19 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Jan 2026 23:32:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:34:20 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Fri, 16 Jan 2026 23:34:20 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jan 2026 23:34:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 23:34:20 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 16 Jan 2026 23:34:20 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 16 Jan 2026 23:34:20 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 16 Jan 2026 23:34:20 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:34:20 GMT
VOLUME [/var/www/data]
# Fri, 16 Jan 2026 23:34:20 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 16 Jan 2026 23:34:20 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 16 Jan 2026 23:34:20 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 16 Jan 2026 23:34:20 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 16 Jan 2026 23:34:20 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 16 Jan 2026 23:34:32 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:34:32 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 Jan 2026 23:34:32 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 16 Jan 2026 23:34:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jan 2026 23:34:32 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf0001b87faad678e492fbe52c4d0956642b480ca270446b682498ab48043bf`  
		Last Modified: Fri, 16 Jan 2026 23:31:10 GMT  
		Size: 3.6 MB (3591623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e367217606eb89df7bf806077fc961f5778d9261aae64c0dc855156dcc5b5c`  
		Last Modified: Fri, 16 Jan 2026 23:31:09 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee69afcd153bd2b7016bc456f768d14f1de8660db516475250b7b96b478f891d`  
		Last Modified: Fri, 16 Jan 2026 23:20:30 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f50a1e8903458c74dacd28b98f53ee014c0d9fd4f85704fdec80b719c39d59`  
		Last Modified: Fri, 16 Jan 2026 23:31:11 GMT  
		Size: 12.6 MB (12632647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea05c597be3eff6ca6f409a193b01a2719ac4aaf0034ef823de0433f5030ea6b`  
		Last Modified: Fri, 16 Jan 2026 23:20:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aa0ebb2b4f1fb36c8b2aa6f56d3eeea8ff92a47267e5554bf5a1d2298a2fd0`  
		Last Modified: Fri, 16 Jan 2026 23:31:09 GMT  
		Size: 13.4 MB (13371516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ffe10f4ba972b0815e860439c769c00d698e3fefcc82c993d6ee74589ab896`  
		Last Modified: Fri, 16 Jan 2026 23:31:07 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef12e1cd0631ac46aa90363cc1108f1d024c405a2291a20ed119f42c71c3f1b`  
		Last Modified: Fri, 16 Jan 2026 23:20:25 GMT  
		Size: 23.5 KB (23498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf3f8a08e0c3139cb0f29ef4b0d65972d1b4db5394279e2258cb6b12574cd7`  
		Last Modified: Fri, 16 Jan 2026 23:20:26 GMT  
		Size: 23.5 KB (23510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe71a8153d220dae5740275aa0ee9fdb31aedc6d68e10fd5ecb9b5000783226`  
		Last Modified: Fri, 16 Jan 2026 23:20:26 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc281e3434197dc433815dec6609029855eb22606d5a6a440d42ed5da54c0e`  
		Last Modified: Fri, 16 Jan 2026 23:34:41 GMT  
		Size: 12.5 MB (12504561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6592cd899e098b4ccd21fbcc4ca5059f816011ad7b94304736cfdd3f40ada`  
		Last Modified: Fri, 16 Jan 2026 23:34:49 GMT  
		Size: 1.0 MB (1038207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759fcb756457c3adbd39c96c9d15cfd1ea281fa15845c3bdd4b9c6fdddb199e6`  
		Last Modified: Fri, 16 Jan 2026 23:34:41 GMT  
		Size: 9.9 MB (9864711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840e0622ec7413d86529cf5e8aa1b647a986cf3714c295c82a34762c9f8cee2a`  
		Last Modified: Fri, 16 Jan 2026 23:34:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6349ba23a1e618ab7abe54d616d796a30d71f8332d14472267a675dc090e94ce`  
		Last Modified: Fri, 16 Jan 2026 23:34:49 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04add02667416ee14beed096cc8cb3fdbeed66086321b2fa9f93b807fd0baaae`  
		Last Modified: Fri, 16 Jan 2026 23:34:49 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e04487cb928ee1a55244c2b2decab39f96580111f8c25f72c2e5d36069b0d9b`  
		Last Modified: Fri, 16 Jan 2026 23:34:56 GMT  
		Size: 59.5 MB (59473848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2043587d878d20e332f43cdde2cd54fb9a86deef5f11e1c703af2520d8127adb`  
		Last Modified: Fri, 16 Jan 2026 23:34:49 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7215bc098068ae6aaf99f0f6790bee4bad2741aa52ad883176afc978daefb0`  
		Last Modified: Fri, 16 Jan 2026 23:34:42 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:1b24fdc359e668298f5de35cf49a81a614bcd7f00ecde99d586bde8a0e398973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 KB (61898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7de5055449d8181369c999f66321ca2478026f89f1fadba291b6e3a45268a2f`

```dockerfile
```

-	Layers:
	-	`sha256:3b9efb3127b58c3306a2d22e3af1c467fceeff5244912240e31d68090ee1431a`  
		Last Modified: Sat, 17 Jan 2026 00:29:03 GMT  
		Size: 61.9 KB (61898 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:6b0b19df4efade725522d642e17468ac2c907e64944bb8aaee789ef42a6944b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaaa268e09e92aa97322a500e598192aa00229803095346602ab154b663d25e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:20:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:20:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:20:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:20:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:20:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:20:33 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:28:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:30:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:30:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:30:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:30:57 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:30:57 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:30:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:30:57 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:30:57 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:55:21 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Fri, 16 Jan 2026 23:55:24 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Jan 2026 23:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:57:55 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Fri, 16 Jan 2026 23:57:55 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jan 2026 23:57:55 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 23:57:55 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 16 Jan 2026 23:57:55 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 16 Jan 2026 23:57:55 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 16 Jan 2026 23:57:55 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:57:55 GMT
VOLUME [/var/www/data]
# Fri, 16 Jan 2026 23:57:55 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 16 Jan 2026 23:57:55 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 16 Jan 2026 23:57:55 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 16 Jan 2026 23:57:55 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 16 Jan 2026 23:57:55 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 16 Jan 2026 23:58:08 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:58:08 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 Jan 2026 23:58:08 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 16 Jan 2026 23:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jan 2026 23:58:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24515353473db2a33c0353413941692c6338187eb28b87ee347c791ba816dc5`  
		Last Modified: Fri, 16 Jan 2026 23:38:32 GMT  
		Size: 3.5 MB (3548333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5b4d63191c669228925296e943ffe7e78ea7be3afc2899edaa01eb71c9a5a`  
		Last Modified: Fri, 16 Jan 2026 23:23:52 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a347714cf68ac4b3fa8d80486474dca19851389a3654354d9354edde506c7d0`  
		Last Modified: Fri, 16 Jan 2026 23:24:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba4565fef26bfa3a483a0d785a6f534ab6fd8e9d84e14946de2cf2582ec88f`  
		Last Modified: Fri, 16 Jan 2026 23:31:11 GMT  
		Size: 12.6 MB (12632657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83fe1af8938a162c92ecb67e81a9ea7cbbdfdbed955d516fe7f14185e658712`  
		Last Modified: Fri, 16 Jan 2026 23:31:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e409a49e87f68333041e5ce1fb21395e507452d93faf61518c9372f6298a2e3d`  
		Last Modified: Fri, 16 Jan 2026 23:31:12 GMT  
		Size: 12.1 MB (12099040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce31f145246671a42428e5c273110aff56e4d25c2e2fdc198f2054901573c1`  
		Last Modified: Fri, 16 Jan 2026 23:31:02 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f00ef517a0d2f9aacd37e69f26628b7bc89ff373ab6e09a0d134224e190a47`  
		Last Modified: Fri, 16 Jan 2026 23:31:04 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8978b383d2dff2e025367e53841851b872536603a506cbe984418a44c094710`  
		Last Modified: Fri, 16 Jan 2026 23:31:09 GMT  
		Size: 23.4 KB (23350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a93c26c5a00d2dd2e46670207f1388c6011474aae3307a31b538a018292ded6`  
		Last Modified: Fri, 16 Jan 2026 23:31:10 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ec46cd8c066801befc10050de804d03654fe97407b9859ae93ca6f979a8ab`  
		Last Modified: Fri, 16 Jan 2026 23:58:26 GMT  
		Size: 11.8 MB (11771973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cffcd7fd7a44633a4c2b5cbe547429d5c2ec8a4b5a63a47f34cd4759d5eb98`  
		Last Modified: Fri, 16 Jan 2026 23:58:25 GMT  
		Size: 1.0 MB (1006381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be7113636b98ca13f980df2616f29f6bd4887e498fff3a79db980b33a1d8f8d`  
		Last Modified: Fri, 16 Jan 2026 23:58:27 GMT  
		Size: 9.0 MB (9034745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04f2eda3c9967989fcd905df7e7490bdbbff211634176f0f6080858281fd2e8`  
		Last Modified: Fri, 16 Jan 2026 23:58:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91b688b11e1b4e9fd2085b9cf191f7abe0db18d5e01f61026c7da1ea9dd98e`  
		Last Modified: Fri, 16 Jan 2026 23:58:25 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1f227db707aebcb39c2d73d9f42786c1c43774bd040831262708fa25c5a700`  
		Last Modified: Fri, 16 Jan 2026 23:58:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250f7a458db230682d97ac3adaf579a394047b1b8cb65b0b2dbbd5dbf408aaba`  
		Last Modified: Fri, 16 Jan 2026 23:58:36 GMT  
		Size: 59.5 MB (59473874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77fd705cc31b4d3fffec9bec8fc5ade9b7c42c5c076a7775a79612202c80a0a`  
		Last Modified: Fri, 16 Jan 2026 23:58:25 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac0ca77d3e7377c6cd9cd2791f077473af6b66d4b2c578a6b8fe4abcf9f815f`  
		Last Modified: Fri, 16 Jan 2026 23:58:25 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:1f32584be83eca7975f295ce421d95ba6adc351c826a577c60871ba9b1cdd193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 KB (62048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7aa66859a538e0c762af4070c371787190a303af451eb6f998237bf125bc94`

```dockerfile
```

-	Layers:
	-	`sha256:32e26e58fe122acd8fad898e74f61ccac8a43474f5135723f5044b7ded4f62e2`  
		Last Modified: Fri, 16 Jan 2026 23:58:17 GMT  
		Size: 62.0 KB (62048 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:e3685a4e7d4a7f34e15394c92ec2d1fb4c0217b07c0cf9541f26aabb6790501e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110996834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc37e4c2c2dc85500bd89af20f6bee181be406c63c6e0af211fa586ad5cc3b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:16:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:16:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:16:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:16:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:16:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:16:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:16:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:16:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:16:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:16:40 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:16:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:16:40 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:16:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:16:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:19:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:19:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:19:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:19:30 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:19:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:19:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:19:30 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:19:30 GMT
CMD ["php-fpm"]
# Sat, 17 Jan 2026 00:01:40 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 17 Jan 2026 00:01:43 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 00:01:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 00:04:12 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 17 Jan 2026 00:04:12 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 00:04:12 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 00:04:12 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 00:04:12 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 17 Jan 2026 00:04:12 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 00:04:12 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:04:12 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 00:04:12 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 00:04:12 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 00:04:12 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 00:04:12 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 00:04:12 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 00:04:25 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Sat, 17 Jan 2026 00:04:25 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 00:04:25 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 00:04:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 00:04:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d191236481e1fb715d189c28720b080c1f36207b48750759f68d3c364e1209f6`  
		Last Modified: Fri, 16 Jan 2026 23:19:37 GMT  
		Size: 3.3 MB (3347129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d741f80a2e1550fa544757826fe76924ecc18197367638d5998ed61d717cf4b5`  
		Last Modified: Fri, 16 Jan 2026 23:47:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910f66adcc72eecfde4047f27f6df08381084e53eddf0bb00252ba7082c622b2`  
		Last Modified: Fri, 16 Jan 2026 23:19:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e2053377b50552fcdb47af9056d7e589f5aff2e6a2b1614bc91c78477c172`  
		Last Modified: Fri, 16 Jan 2026 23:47:03 GMT  
		Size: 12.6 MB (12632650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe970b75acb26677ad68f0c4165b6857ad37823d266ab523baa57865a403b2c`  
		Last Modified: Fri, 16 Jan 2026 23:19:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b601a105894715e7014fbd75f1892757981e411c092179ab59a951ab2aa1bfb`  
		Last Modified: Fri, 16 Jan 2026 23:19:38 GMT  
		Size: 11.4 MB (11399648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115795093c1ab6234e2dac9e87c3963a0abb6a27cea1588bf37ccf2fdb113ff9`  
		Last Modified: Fri, 16 Jan 2026 23:19:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225c7f1f836295c942d389328b6ecc0cad96666f92f0d765b8fd882fd49765d3`  
		Last Modified: Fri, 16 Jan 2026 23:19:39 GMT  
		Size: 23.3 KB (23326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240daf9bcfe6347bb12cf04f3b5f06200e85c659d98f2026dadb915dc28bbd2d`  
		Last Modified: Fri, 16 Jan 2026 23:47:01 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bb7c5e173d090663c930cd6146b8b206f774ad9705228c0dad67ace4a0cc6a`  
		Last Modified: Fri, 16 Jan 2026 23:19:45 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24badbcbfdfdda2739b103d009b586a5339f1fc27958a505d25d674d31712db0`  
		Last Modified: Sat, 17 Jan 2026 00:04:34 GMT  
		Size: 10.8 MB (10837275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e6a34544c9f09a3c8e94f871264bed016c744075c2aedf260373985705ec3`  
		Last Modified: Sat, 17 Jan 2026 00:04:42 GMT  
		Size: 1.0 MB (1006330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb37d0c22d1348cf61aa8d5e96118fa054b6c8a5d9e31d975eb3be6ad80fd27`  
		Last Modified: Sat, 17 Jan 2026 00:04:33 GMT  
		Size: 9.0 MB (8955045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671965227d00cab575b2c935eee410925166a824229711c0852457f956e13b3`  
		Last Modified: Sat, 17 Jan 2026 00:04:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3926a4bb586616e4e7fb0b5c832106acf2194e9b9182efa8f86ae9a606509fcb`  
		Last Modified: Sat, 17 Jan 2026 00:04:41 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b921285df909a75e484c99df6546a40537d355c44662e42c6ad9ab012fbd7377`  
		Last Modified: Sat, 17 Jan 2026 00:04:42 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85621eb91de5593cd03786c4b19f9935a8bed625ee98994ac3d849194fe4b0`  
		Last Modified: Sat, 17 Jan 2026 00:04:37 GMT  
		Size: 59.5 MB (59473947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0163bb0754e6d38ad0cc88d36d77c96b13846d2475f0fc150d40d34efb01be1`  
		Last Modified: Sat, 17 Jan 2026 00:04:42 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1820cf8689902cfe531e92dc1ffa2432f818031ee98999b78d83faf4768abf4c`  
		Last Modified: Sat, 17 Jan 2026 00:04:35 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:e711991f1a7027166a25450410accfbd1fc4d14908c2eeb7c968bc69973815d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 KB (62048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ea6bc5239d870396a4686ed4ab515b150e2014b40a1508454f6c4cd9052d4`

```dockerfile
```

-	Layers:
	-	`sha256:718610684e2778de26b7fc3d51fd24cd55ea8a92cdbdd00a22e9f983dc75d9ae`  
		Last Modified: Sat, 17 Jan 2026 00:32:38 GMT  
		Size: 62.0 KB (62048 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:eb6284a14857b64137d82e986efa15d86399f428af4713a3e8950729f4941e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116366936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f448c985aef1de9e7776a6cbb451f462184329fe609ba3df01f2773fe6df08d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:18:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:18:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:18:03 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:26:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:30:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:30:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:30:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:30:45 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:30:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:30:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:30:45 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:30:45 GMT
CMD ["php-fpm"]
# Sat, 17 Jan 2026 00:00:34 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 17 Jan 2026 00:00:37 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 00:00:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 00:03:49 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 17 Jan 2026 00:03:49 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 00:03:49 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 00:03:49 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 00:03:50 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 17 Jan 2026 00:03:50 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 00:03:50 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:03:50 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 00:03:50 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 00:03:50 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 00:03:50 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 00:03:50 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 00:03:50 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 00:04:02 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Sat, 17 Jan 2026 00:04:02 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 00:04:02 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 00:04:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 00:04:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e57ef49273509bd2cae945ec2ed47fd7e262bc7a6fb3a5cb0880c2bbfe13c7`  
		Last Modified: Fri, 16 Jan 2026 23:21:42 GMT  
		Size: 3.6 MB (3601419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ee18e8df132fa626cb19973c2fdd84473cd677304fe6da3f87911c2d4c1e0d`  
		Last Modified: Fri, 16 Jan 2026 23:21:42 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d70156c099ba7d27cb8ef9aca78e146b7ea146cedab51e648df4c62670ae7`  
		Last Modified: Fri, 16 Jan 2026 23:27:59 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c71bb137bc09ea779e9d37dc743983c903d68c87786b515820ceb30b66c9b`  
		Last Modified: Fri, 16 Jan 2026 23:30:59 GMT  
		Size: 12.6 MB (12632643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fef165a76604b7bf1305dbcfa0d55bbc896feb79849eee6a4a0b72d03e54b`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49660a09addce683f6e6d10e228001e3334a49ee3a7a586a79a69e77e28ade6`  
		Last Modified: Fri, 16 Jan 2026 23:31:01 GMT  
		Size: 13.3 MB (13262038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55944b17138f60294e904d4cf6379a6b12f4a86783eef578c4a382f24a39f562`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd7b0441f9c73f7db13bd1f912209ce31f6a48257c58c58aec516cfdbdb1a8`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 23.4 KB (23355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbc4a5675e34e6a09d8270bb8eed3262e5318cdf732bdb4468c686fc0b2080`  
		Last Modified: Fri, 16 Jan 2026 23:30:59 GMT  
		Size: 23.4 KB (23367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965ece9c0854d564010f4b17712d67711ef8f9a19f0b0f46343d4f412b6cbed`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc26543c12967745f0dc4cdb9f313c0f7bbe7d17adec79a8a85da66d0a7a67d9`  
		Last Modified: Sat, 17 Jan 2026 00:04:11 GMT  
		Size: 12.2 MB (12168346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd05a3565b9441076c60c4174251f710328d848d60341ccdbd6915ecdd1115`  
		Last Modified: Sat, 17 Jan 2026 00:04:19 GMT  
		Size: 970.1 KB (970114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c52e00c65e2e093a5347547419577fc0d3eb7c8fc2ab0241bfcb18ea0e72f1b`  
		Last Modified: Sat, 17 Jan 2026 00:04:11 GMT  
		Size: 10.0 MB (9997311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54a6cd73d93f325ab1dbed21886aa976e98dc094ceac55ef538671da56cbfa1`  
		Last Modified: Sat, 17 Jan 2026 00:04:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3b3f3cd56faa02e6621b5594912af1185c4f8435bfe59472a279ffb704ac0`  
		Last Modified: Sat, 17 Jan 2026 00:04:11 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7ee515445389d065bd7f288994e2d3df61f337a7dd931b2ae67a9b1e252a2b`  
		Last Modified: Sat, 17 Jan 2026 00:04:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80509f9b5f2f23e4aac5829cb8d5120ebda934b57accfc9042017506c8dd3c4`  
		Last Modified: Sat, 17 Jan 2026 00:04:25 GMT  
		Size: 59.5 MB (59473845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d957d73f0102a4ac32545778def246cc2ea534fea5add8fdbdfe17799807d6b`  
		Last Modified: Sat, 17 Jan 2026 00:04:12 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde2eddb2101778240b1bc6f13e867d47f3a781d598ce7f277c6974b0a7bfb22`  
		Last Modified: Sat, 17 Jan 2026 00:04:13 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:f77dd935af7edd74055fb0e1b22e8e91a715f42e352787ef80f2ddffb4d2dbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 KB (62072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a63f11f60ffc36a654c1c559ac62cadeeda69d3a22a4137cfb1b5901ce28f00`

```dockerfile
```

-	Layers:
	-	`sha256:132c52436cf8907676844ad4acbd05d7c09e430a379713e7b981c9d76dc55950`  
		Last Modified: Sat, 17 Jan 2026 00:33:13 GMT  
		Size: 62.1 KB (62072 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:2dd83039f9d06bbf11960ac3095a8c9a827007cbfd25f3fb3bf52b09d810539e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116940289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b31ef561d9ea29484b22e3f592f49a8b819e64982c7761f3003180e846607b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:18:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:18:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:18:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:18:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:18:42 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:22:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:22:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:26:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:26:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:26:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:26:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:26:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:26:07 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:26:07 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:26:07 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:26:07 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:26:07 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:57:35 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Fri, 16 Jan 2026 23:57:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Jan 2026 23:57:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 23:59:51 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Fri, 16 Jan 2026 23:59:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jan 2026 23:59:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 23:59:51 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 16 Jan 2026 23:59:51 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 16 Jan 2026 23:59:51 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 16 Jan 2026 23:59:51 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:59:51 GMT
VOLUME [/var/www/data]
# Fri, 16 Jan 2026 23:59:51 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 16 Jan 2026 23:59:51 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 16 Jan 2026 23:59:51 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 16 Jan 2026 23:59:51 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 16 Jan 2026 23:59:51 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 00:00:03 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Sat, 17 Jan 2026 00:00:03 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 00:00:03 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 00:00:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 00:00:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449bb8977563b040e95c798072cc3f87bf9d15ececab308bc5098543a203ef8`  
		Last Modified: Fri, 16 Jan 2026 23:30:18 GMT  
		Size: 3.6 MB (3629147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9117759c26104880adfd7ce2dfe84505828ec310c4b8b6fec517edd8e7179d2`  
		Last Modified: Fri, 16 Jan 2026 23:22:43 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acecb1a6db8a318afce9e5ab2ea7be76c34b9931fff6e773fc2dfb0380a10e62`  
		Last Modified: Fri, 16 Jan 2026 23:22:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142b0a41b7be4fe121712e812e6097f4477e7b6e52547348a934b3d6b41fe1d`  
		Last Modified: Fri, 16 Jan 2026 23:26:14 GMT  
		Size: 12.6 MB (12632631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9762d106960e9c954d7d7dade6f103974c7df7b1dee0bd8d242b0d75448f0064`  
		Last Modified: Fri, 16 Jan 2026 23:26:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ee0285377471359fd30cba708533abc74e51355ec1aa138a866e721c9e32d`  
		Last Modified: Fri, 16 Jan 2026 23:26:21 GMT  
		Size: 13.6 MB (13625392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090bd00eed27358845e2fd72fa2d0a3cbef1a9ff959c0fadcddc418b1717379`  
		Last Modified: Fri, 16 Jan 2026 23:26:20 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3baa30095f14c496a007ab2a4672915f4e63b9a37d645ecbb9f959c3eb9c4c8`  
		Last Modified: Fri, 16 Jan 2026 23:26:14 GMT  
		Size: 23.5 KB (23520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e4330326db564ff90f3150236155f9c0edda26ca40c41cb549c111faedd62b`  
		Last Modified: Fri, 16 Jan 2026 23:26:14 GMT  
		Size: 23.5 KB (23541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b26437b8c20ba7691c0b6c18f5d96c4886b60ba81c9cae03ff1e83a471b00cd`  
		Last Modified: Fri, 16 Jan 2026 23:46:58 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6641ec27d2f723f9adf23ea3e254212e1d37dd9628262830a5ec569b137ed294`  
		Last Modified: Sat, 17 Jan 2026 00:00:13 GMT  
		Size: 12.8 MB (12751658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61952243348b51324098d614a2651f48f6d8d4bf4be97caa435c05bbc2fd4d4`  
		Last Modified: Sat, 17 Jan 2026 00:00:26 GMT  
		Size: 1.0 MB (1013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4556464d638ff8d4f08717426b093e149c01e6cfeed44e644dd301ab68277834`  
		Last Modified: Sat, 17 Jan 2026 00:00:28 GMT  
		Size: 10.1 MB (10061714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82db187913c4cf2f762722dcaf4b573002c7c83df5e364d1572b4aa61b1e8ac6`  
		Last Modified: Sat, 17 Jan 2026 00:00:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0075faaf96448cd066cce053b3a2ca477cfda07f47b0ce1afe75b9ff958c693f`  
		Last Modified: Sat, 17 Jan 2026 00:00:26 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51baeba370b4782bd74bd743c98c4b04838cf0a41dcb6962f349206262e684c`  
		Last Modified: Sat, 17 Jan 2026 00:00:16 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd9b75e677f9c21ec643662836322f1bc5cd1c24ee2d795282e9d8f6b5dba05`  
		Last Modified: Sat, 17 Jan 2026 00:00:41 GMT  
		Size: 59.5 MB (59473889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73aadae99a8a1403117a2d0eb00d83eb6a6e3afa535fc7afe60a3fc4473c3e6a`  
		Last Modified: Sat, 17 Jan 2026 00:00:27 GMT  
		Size: 3.2 KB (3158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f48c81a9565f591a2e88e734285042d736be593cc008ea9ca023e847887a9ac`  
		Last Modified: Sat, 17 Jan 2026 00:00:27 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:cdd97cfcbee34dfd5702d46fe56773839584d10a2859471ab054b1c4b283679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 KB (61865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3756a9c53b896737b769c7d12b6d5099399a7516c1e207fad382d1f9810eb6f3`

```dockerfile
```

-	Layers:
	-	`sha256:42e69d1b21e4e37b341bcf8a6b83174792297de5e809783dbd632564f16fa673`  
		Last Modified: Sat, 17 Jan 2026 00:00:11 GMT  
		Size: 61.9 KB (61865 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:d1dfcb734547299ed8a5e26f7876ac6d8ee9ec21d29873d515028e497c6faf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118113000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb293cdf497bb73a3ad371db8a62fae4a4d4eef14753ba339d25a447d10355e`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_VERSION=8.3.30
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sat, 17 Jan 2026 00:46:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 Jan 2026 00:46:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:53:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 00:53:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:53:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 Jan 2026 00:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 00:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 00:53:25 GMT
WORKDIR /var/www/html
# Sat, 17 Jan 2026 00:53:26 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 Jan 2026 00:53:26 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 Jan 2026 00:53:26 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 Jan 2026 00:53:26 GMT
CMD ["php-fpm"]
# Sat, 17 Jan 2026 03:18:16 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 17 Jan 2026 03:18:21 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 03:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 03:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 17 Jan 2026 03:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 03:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 03:21:48 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 03:21:49 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 17 Jan 2026 03:21:50 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 03:21:50 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 03:21:50 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 03:21:50 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 03:21:50 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 03:21:50 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 03:21:50 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 03:21:50 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 03:22:09 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Sat, 17 Jan 2026 03:22:11 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 03:22:12 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 03:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 03:22:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772e0a90d4aa4f209aab27b75a49043c6df83f144ec29ba8e6c8e964a8a165a`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 3.8 MB (3768859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb9c8b89ecca8688bdf852690f34dbf7da2dc90d2e06d7221c85ff1070c08b`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce8460d16487c23dd44b0afef57a49c4aeca53309e968b330dc8c9044d5e51`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557c1a23c76873bd4e8613ecac9c79740d96fa8eb9a3f8796dd6db74d173f6b4`  
		Last Modified: Sat, 17 Jan 2026 00:50:22 GMT  
		Size: 12.6 MB (12632671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3508d1b60b4dfd1975551db78e87cd6f68f6a60e4260b72d5e38fe35b6c01ae`  
		Last Modified: Sat, 17 Jan 2026 00:50:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7acbc630e63f14877d1afdcce9b7513f50c0fc213641552ea1b62af63e9541b`  
		Last Modified: Sat, 17 Jan 2026 00:54:04 GMT  
		Size: 14.1 MB (14142042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb83aabc56c0767804dde31d40d822f7bc6cfaecc6b5dde9384577f467e9213`  
		Last Modified: Sat, 17 Jan 2026 00:53:56 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbce42e3f6eae51a98c21e9330838db49dae44db7609d6f61f77abbf4d83870`  
		Last Modified: Sat, 17 Jan 2026 00:53:56 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b331672fe99e75d1d77aec3096dc981919d31e0001b89ad49df323a18fb877`  
		Last Modified: Sat, 17 Jan 2026 00:53:56 GMT  
		Size: 23.4 KB (23401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9006e4ea6a7ff1b0ab4f67f721af61fac6dcf1c8512cda24d0018960613e0d`  
		Last Modified: Sat, 17 Jan 2026 00:53:56 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafc43b77a1ead377561cfa062237899ec671b8204c7336b69f5790e17cd0abb`  
		Last Modified: Sat, 17 Jan 2026 03:22:47 GMT  
		Size: 13.3 MB (13348132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dc56e0c45686c3345641308d3b023d3115c65b5bd9050934920c1c7e7805d5`  
		Last Modified: Sat, 17 Jan 2026 03:22:35 GMT  
		Size: 958.6 KB (958561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aefddf8e3819c0d20ed9de8509c434d3c031d23b61cbf057a50befa4fe1f26`  
		Last Modified: Sat, 17 Jan 2026 03:22:48 GMT  
		Size: 9.9 MB (9895607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5290b695762ba9ef71d1688c94e49d5e294e12a4550639470aff7449ae2ab9f2`  
		Last Modified: Sat, 17 Jan 2026 03:22:45 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610b71d67399e2175d1429d4939be04157951eefed933334cb6745a8f18db0cb`  
		Last Modified: Sat, 17 Jan 2026 03:22:45 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f93e585aeee142f166b022ac68e3e1afca69af0dd5e9ceb64209c35b06a8b9a`  
		Last Modified: Sat, 17 Jan 2026 03:22:46 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af565e3d65a7f540d56e2d242de230f133be91ef5ab217fcc45e391228be4740`  
		Last Modified: Sat, 17 Jan 2026 03:22:53 GMT  
		Size: 59.5 MB (59473815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e337ae78434410dd84b0525be171adb1ad3ca96c428662e4d5e46beebdb7cb4`  
		Last Modified: Sat, 17 Jan 2026 03:22:46 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2e9ddea2e6e0d8b44bcf12a5bfba69ee241b1867afc82791d7ad2d7c274d92`  
		Last Modified: Sat, 17 Jan 2026 03:22:46 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:27e8567eab4d00a8a67a3dfb23d07df3a55c890f6c1dfec3aec2187b79395325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 KB (61940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f1804aadf3c32809bd2dc9b8cd979f82cff3f11472b8b8890b7c07a094a769`

```dockerfile
```

-	Layers:
	-	`sha256:fa151630d292e356959a33487dd1e84c969e4fc39b256a5e4fc6290d22bad1f8`  
		Last Modified: Sat, 17 Jan 2026 06:27:44 GMT  
		Size: 61.9 KB (61940 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:d9ca6ac6b8aa3486dab246b3327c96220a7f2719671ceb86fc2bb543dddaea98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115207588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eefa5cbe652f6dee759efb508d1e008d085d6c610a939f028dea63e674967ce`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.3.30
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sun, 18 Jan 2026 16:10:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sun, 18 Jan 2026 16:10:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 17:56:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 18 Jan 2026 17:56:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 17:56:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 18 Jan 2026 17:56:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 18 Jan 2026 17:56:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 18 Jan 2026 17:56:34 GMT
WORKDIR /var/www/html
# Sun, 18 Jan 2026 17:56:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sun, 18 Jan 2026 17:56:35 GMT
STOPSIGNAL SIGQUIT
# Sun, 18 Jan 2026 17:56:35 GMT
EXPOSE map[9000/tcp:{}]
# Sun, 18 Jan 2026 17:56:35 GMT
CMD ["php-fpm"]
# Mon, 19 Jan 2026 18:43:18 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Mon, 19 Jan 2026 18:43:28 GMT
ENV GOSU_VERSION=1.17
# Mon, 19 Jan 2026 18:43:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Jan 2026 19:07:06 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Mon, 19 Jan 2026 19:07:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 19 Jan 2026 19:07:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 19 Jan 2026 19:07:07 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Mon, 19 Jan 2026 19:07:07 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Mon, 19 Jan 2026 19:07:08 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Mon, 19 Jan 2026 19:07:08 GMT
VOLUME [/var/www/html]
# Mon, 19 Jan 2026 19:07:08 GMT
VOLUME [/var/www/data]
# Mon, 19 Jan 2026 19:07:08 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 19 Jan 2026 19:07:08 GMT
ENV FRIENDICA_VERSION=2024.12
# Mon, 19 Jan 2026 19:07:08 GMT
ENV FRIENDICA_ADDONS=2024.12
# Mon, 19 Jan 2026 19:07:08 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Mon, 19 Jan 2026 19:07:08 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Mon, 19 Jan 2026 19:07:46 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Mon, 19 Jan 2026 19:07:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Mon, 19 Jan 2026 19:07:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Mon, 19 Jan 2026 19:07:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Jan 2026 19:07:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:09:59 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5ca77aaa3d4c3436dacc22cd35e93ba60a69c375f2612b83ca60e8cce337`  
		Last Modified: Sun, 18 Jan 2026 17:04:01 GMT  
		Size: 12.6 MB (12632650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c18c87dabc45078f4ee30ba247ef150e2d7cc4fb627ac605af0b221fc950483`  
		Last Modified: Sun, 18 Jan 2026 17:04:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49fc4f21fbd510842aad9d50717cde1800cfdb72aebd6c5607f1aaa1b564bd`  
		Last Modified: Sun, 18 Jan 2026 17:57:25 GMT  
		Size: 13.0 MB (12960367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a71a5f8c7b96bf32a53657ce88a9708d5da73aae331be3e21143b10476c773`  
		Last Modified: Sun, 18 Jan 2026 17:57:30 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b3f5aadedd5f74487b47b6ca1844684c049a28324262007036343803a`  
		Last Modified: Sun, 18 Jan 2026 17:57:30 GMT  
		Size: 23.4 KB (23368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d21fc3fe5a8cb429630195c9e672fb191c593b58439864f4689ea80393295`  
		Last Modified: Sun, 18 Jan 2026 17:57:30 GMT  
		Size: 23.4 KB (23391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab03688f392c7a731b68db58845a839c965c8121fd9d5c0ca32f72a52a4ea0e2`  
		Last Modified: Sun, 18 Jan 2026 17:57:30 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7c4eae9cd96bda56f16564686d0060f9eb7ae7334daf83fb49685dbac5158`  
		Last Modified: Mon, 19 Jan 2026 19:09:16 GMT  
		Size: 12.3 MB (12260061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c37f19cb7b03707062af7eb308ca5b52a5550557218f6bed3b78cb72c874f7`  
		Last Modified: Mon, 19 Jan 2026 19:09:41 GMT  
		Size: 1.0 MB (1010376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97054fa67b693b1593dfec2925a53ccef54ca728bb92ad51a423199f0ad6c40f`  
		Last Modified: Mon, 19 Jan 2026 19:09:42 GMT  
		Size: 9.5 MB (9480632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb93aa4ba4f9619c47608bee6d37653531eaccb1e10cb8b56f6bc5d75d9135`  
		Last Modified: Mon, 19 Jan 2026 19:09:13 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c557c553bea3df1c8930bb19acbd651a3656f52e540fdd6b7c38022780fdd`  
		Last Modified: Mon, 19 Jan 2026 19:09:41 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59ef4601c78df7bde61917154d6f7b525663225b1cf70cc990a232d23d40cf4`  
		Last Modified: Mon, 19 Jan 2026 21:07:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4731319cdc5c78ac168d019075a728dd49c2435bbd57a78b46b41b39bc76b2`  
		Last Modified: Mon, 19 Jan 2026 19:09:25 GMT  
		Size: 59.5 MB (59473818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cada3cc7f4302bbfa117a2db6438afc89a4824379ff4851903dbcc95f2e2d30`  
		Last Modified: Mon, 19 Jan 2026 19:09:41 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a89c3dfbfae930e899396028e929a974b5c8801cdb8b03a057938461e22dcd`  
		Last Modified: Mon, 19 Jan 2026 19:09:41 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:18706e671a00999242c8b55f9e6fb4fa6bdd9422486f68f06d5d0e187d26470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 KB (61948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384bdc2edef7dc7a87b5a75502fa92bd90d386f582633fa6a98dd3f86c732cc5`

```dockerfile
```

-	Layers:
	-	`sha256:e65f320b834da3cfb05634d2efa38fa19f7fe4c661b89da41a8464be59dbc569`  
		Last Modified: Mon, 19 Jan 2026 21:27:40 GMT  
		Size: 61.9 KB (61948 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:2392436611119e8d5789d82bbf17408fbb6a99e1fa61af125c7bacf04493766b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116650653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0492f6a75fe03d75d99f4162c5509735fd7c0e908afd3d93fecc3550209879a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:31:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:31:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:31:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_VERSION=8.3.30
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Thu, 18 Dec 2025 00:31:41 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:43:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:43:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:48:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:48:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:48:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:49:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:49:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:49:00 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:49:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:49:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:49:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:49:00 GMT
CMD ["php-fpm"]
# Sat, 17 Jan 2026 00:36:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Sat, 17 Jan 2026 00:36:50 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 00:36:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 00:38:44 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Sat, 17 Jan 2026 00:38:44 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 00:38:44 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 00:38:44 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 00:38:44 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Sat, 17 Jan 2026 00:38:44 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 00:38:44 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:38:44 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 00:38:44 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 00:38:44 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 00:38:44 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 00:38:44 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 00:38:44 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 00:38:53 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Sat, 17 Jan 2026 00:38:53 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 00:38:53 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 00:38:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 00:38:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344fa339e55ae2ef62eaee8d37110609d0d656213b8274a8e7a7ab18327247ac`  
		Last Modified: Thu, 18 Dec 2025 00:38:18 GMT  
		Size: 3.8 MB (3794501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327290246b6eefafee2ed67e84a73a399acad16f47f0ad2d3f400fcf15ef1b3f`  
		Last Modified: Thu, 18 Dec 2025 00:38:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083737e4ce9faf5aa6c038cf664c25a769c6a5aac182a45e34a89d948c87732`  
		Last Modified: Thu, 18 Dec 2025 00:38:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2b279c4f9fb3b6841b5a35845e3d1cc0c1de469a052c641448b4d3423ceb7e`  
		Last Modified: Fri, 16 Jan 2026 23:49:01 GMT  
		Size: 12.6 MB (12632654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61ac558a1507c4076943ce39384fd4b65d36b93b8b280d216718da4707e4fe1`  
		Last Modified: Fri, 16 Jan 2026 23:49:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7117b737c9c695bdade4f43920fbfeacbfbf0b33e1c36a83277101fa6dce646`  
		Last Modified: Fri, 16 Jan 2026 23:49:10 GMT  
		Size: 13.4 MB (13436229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcc010a25c81bcab33e34fd63feda68f8b7a6e3f2662bc34c74882260a8553`  
		Last Modified: Fri, 16 Jan 2026 23:49:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f57122c68bab9bad204b6bccadb675cd77ab0d89194549ed7e0ec6c465c30`  
		Last Modified: Fri, 16 Jan 2026 23:49:10 GMT  
		Size: 23.4 KB (23383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd927d99ce0e4e1e9fe2cc07a3f6bb26bbb0bc2b575c719242a0bdf53f6ac2b4`  
		Last Modified: Fri, 16 Jan 2026 23:49:23 GMT  
		Size: 23.4 KB (23408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafffb395df8c750f2040f4e69974f9a6d0fc1fa0b4f17986920b648edd6265f`  
		Last Modified: Fri, 16 Jan 2026 23:49:11 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04ddac3cb561a15363c9dc47be6180dcc00c0a2e5ce8698a1e3d052a3adac2f`  
		Last Modified: Sat, 17 Jan 2026 00:39:14 GMT  
		Size: 12.7 MB (12749560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef4a2288261b58a66aa4465ba6ae190fc4a75676bee877f6a2214194d9de705`  
		Last Modified: Sat, 17 Jan 2026 00:39:14 GMT  
		Size: 1.0 MB (1005149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9b7858f1ed000417fda7b2b8365beabb4391ed604b2b95b77660cadbf1ab8b`  
		Last Modified: Sat, 17 Jan 2026 00:39:14 GMT  
		Size: 9.8 MB (9768768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5415b6ea412ec64a0437365e49a1819da401e280e93cec707af032d692c35cf3`  
		Last Modified: Sat, 17 Jan 2026 00:39:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c9b21bd66e980ec9d6a814dbe28cb7f246beb93519f1f224e7c6698141800c`  
		Last Modified: Sat, 17 Jan 2026 00:39:14 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b937bea195fb54c3de88e0125c6118f768939cc41dba835681994175713e386d`  
		Last Modified: Sat, 17 Jan 2026 00:39:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e20e097b75fe4571f3ed1bd6edb637b7b5041d4f2355b9f050adf17abbae2`  
		Last Modified: Sat, 17 Jan 2026 00:39:08 GMT  
		Size: 59.5 MB (59473934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b7590aeec28aa43313249ea240843328c2d851eab764883c3ee0769fe50abe`  
		Last Modified: Sat, 17 Jan 2026 00:39:07 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5257a5d63e6fc44fe749dc971b78041fb85d4ee85211443f0f362e9ca22bf`  
		Last Modified: Sat, 17 Jan 2026 00:39:15 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:3a1c8053ce4d4e035e331d71e6a36c09bae124452c8fcf032e8401cf325f3d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 KB (61898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cddc916a905cb0b9e397c11d629bba4ff3aa6b05207876bb3abb2a743cb0474`

```dockerfile
```

-	Layers:
	-	`sha256:147880505ec173524738eb5d895f6afc5a3aa1e727537bc6dbbeed92b4729afd`  
		Last Modified: Sat, 17 Jan 2026 03:28:19 GMT  
		Size: 61.9 KB (61898 bytes)  
		MIME: application/vnd.in-toto+json
