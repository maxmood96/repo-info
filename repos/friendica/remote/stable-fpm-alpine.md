## `friendica:stable-fpm-alpine`

```console
$ docker pull friendica@sha256:73f1b2273d8d5c25956e2e237ca11a01bb6a7cc7ea2b5c24e648b4413bd470a3
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

### `friendica:stable-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:754fc98f8b6be5b20b865ac8c06941955dd6dc7447ee8442f0cce301ed2115b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111053723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be7a221b5d3cfd89696ff804c7b4cbe109155c7ba3b425da7858f51638d876d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b60871cc70d3f357621a185df45989d2cafade8364e0e96ec460ac59718792`  
		Last Modified: Tue, 07 Jan 2025 03:32:16 GMT  
		Size: 3.3 MB (3319674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b81aeea0a9c8a7ab306f8f093cb4af1c1ab880895e603733f08759255bd857`  
		Last Modified: Tue, 07 Jan 2025 03:32:16 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1a6cb63ba87bbe9c27500aca23ce71ae1088176e5bfeacebbd55e91e032059`  
		Last Modified: Tue, 07 Jan 2025 03:32:16 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881c1b297f6c59977997d988ae36ac3e39a64b278fe1fe338df3c76b13a8497c`  
		Last Modified: Wed, 08 Jan 2025 08:11:14 GMT  
		Size: 12.2 MB (12172292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26f2cfca565084eae420639fa01c375c125daa7eca546ac0d997c48a32bf3c7`  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc71264eca7c498dc75a132473c44300fbf1b0e141a68163d9b9f2c35ea92cbe`  
		Last Modified: Tue, 07 Jan 2025 03:32:17 GMT  
		Size: 13.0 MB (12970797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb0a08d0ac3f400c417758fe93a3d7276068bc4e8c19f5c57da9ce9c82ebb18`  
		Last Modified: Tue, 07 Jan 2025 03:32:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94747dcf6a7233c4b5ffd0df784edd30fc116d13b6a249cf373828a8dce00df6`  
		Size: 19.8 KB (19755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42300a12e79bb49a4388dcc6f7520fe4a5746a2fad1fe15474d5edf2c384c3`  
		Last Modified: Wed, 08 Jan 2025 08:11:19 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0414f40e909f5b481a4584f713a85b3ce927e40fc674abb162d540463681f7b`  
		Last Modified: Tue, 07 Jan 2025 04:20:55 GMT  
		Size: 8.7 MB (8729339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad4d3f18b2608a1f3adea0a84ed89da2c631745d91fc66a7453693ed2319911`  
		Last Modified: Tue, 07 Jan 2025 04:20:55 GMT  
		Size: 1.0 MB (1031227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086131563c30e4af3c1af988708f98debfc9a444f31c80958832ae4f26e417ca`  
		Last Modified: Tue, 07 Jan 2025 04:21:11 GMT  
		Size: 9.7 MB (9699161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798ef9977d2a47aa167c48bebc8dacc3cd252810e9bc4a0669b6d2f8005ba172`  
		Size: 640.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe8d57ad04b14e0a0e5fa288a3d34d9e9f114d33e2fcc0a034e27c8da4546be`  
		Size: 59.5 MB (59457209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5da2021cddd64619268cb94b6f06ce7800213efca52ea0693063cdd27dd92`  
		Size: 3.2 KB (3181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeaeb97d28d90c3b1ced3b85f16a38b4e0945f4dfd2a498083fe1cf6fa869ad`  
		Last Modified: Tue, 07 Jan 2025 04:21:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:7703932974b4529fe6848feb7939b7e92609b09518d63c759aec75807bec30c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 KB (51179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b6561c631dedba861ac43dbae770e2032632b225be5d251635c119b7e1f6e0`

```dockerfile
```

-	Layers:
	-	`sha256:c14f1075f96f32f3e430d42c22f437e5d28c50357d3c03f76aa89bb19b272204`  
		Last Modified: Tue, 07 Jan 2025 04:21:10 GMT  
		Size: 51.2 KB (51179 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:356f2247ce87d5df3b963f17371c1c3f7ba14da321cc9d1f991c8e3763120e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108154922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d92c45c0b6df236469cd5ca196e37cb2442d2f5258db5b4eb79ed6e1418761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bef010c611114840926e80cb28932ac752a42db1830688c08b53e3b0479b57`  
		Last Modified: Tue, 07 Jan 2025 04:04:46 GMT  
		Size: 3.3 MB (3288904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6270f8fc8d436fea30c28e682f01c03d0fc9e3ad4d478dd522e49204e509af1`  
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d76c367f31c843767d908ec20d1f4689fd733c923fd9605738b522084ac5a`  
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f9a2e38e2c1090dcdf5c7bd6249297c361e7671706a3a14015a7505b6c770`  
		Last Modified: Tue, 07 Jan 2025 05:41:09 GMT  
		Size: 12.2 MB (12172293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9363939b03c53a2a52a5e674e76b2657c5895ca142d7f66d96c71c83b3d97c9d`  
		Last Modified: Tue, 07 Jan 2025 05:41:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8807085035fb9d4d86a5bc5cd737924a17abe3d26167abcb420eb350e43bbe`  
		Last Modified: Tue, 07 Jan 2025 05:45:03 GMT  
		Size: 11.7 MB (11716803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c112d944edacfe6413b8ab1e99c3f70de2a9d7309a877ac120b4c8f227391481`  
		Last Modified: Tue, 07 Jan 2025 05:45:02 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064828b33a2393e26196eea204635fb3a4139075563a6d9433b1c71346d06b9e`  
		Last Modified: Tue, 07 Jan 2025 05:45:02 GMT  
		Size: 19.6 KB (19555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c179db893b2c3047ba613c3a30961cf62fec0311c2b6beb9b34ad446726cba`  
		Last Modified: Tue, 07 Jan 2025 05:45:03 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ece72cf80c22719f64bb17c7c3159853c9554577a8bfd64c5e2e0e822d6ab7d`  
		Last Modified: Tue, 07 Jan 2025 18:40:12 GMT  
		Size: 8.2 MB (8222105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e9598a5716a20ce915f370da0b89c39269aac669a37d25aadeed8838424a9c`  
		Last Modified: Tue, 07 Jan 2025 18:40:11 GMT  
		Size: 997.6 KB (997594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fbdd635ee91eb556d40552cddfae177b38d078df876dc7b775d87d848f868a`  
		Last Modified: Tue, 07 Jan 2025 18:40:12 GMT  
		Size: 8.9 MB (8901425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b526709808530adc2b8a16d0207d17ad64359fe1e1ba9432ab565d0ca8829e2b`  
		Last Modified: Tue, 07 Jan 2025 18:40:11 GMT  
		Size: 649.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a6deec1a88bf6e839072fbe8e3c777284103fd45a69fbd8d3972db495a7020`  
		Last Modified: Tue, 07 Jan 2025 18:40:56 GMT  
		Size: 59.5 MB (59457141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ada342ad09899d0dd63cf1cdcbccf688220fad87e75cc3595e790c9ffc90`  
		Last Modified: Thu, 02 Jan 2025 19:29:27 GMT  
		Size: 3.2 KB (3181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f4e160237cf63e8101df316fe5606c9ae5dc74274a066c77ab95c9da13e75`  
		Last Modified: Tue, 07 Jan 2025 18:40:54 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:f56c2f71686d47dbf808d2b641380b89707745f27c86f61cb4eb8ee5e8d2d482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 KB (51293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6731cff452d506f3a7e058e8270f48e1d446bf40f1cdf7731836d9fd1b12d91b`

```dockerfile
```

-	Layers:
	-	`sha256:790dc0e498cac3b95026e605343d3c591c192a8681c18128c2097895c31f781d`  
		Size: 51.3 KB (51293 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:3959f9aec2d3d52c1084c9b543c02ba1f6dccd7601b3efa134fd18e9802d6382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106280822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3d2fd1ed12351c1141ccd6459c9959203bdb6d32722afeca46a27c53c3337c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a46a05ef2f8f5dc8f91bb48ccb26f8769e182e5d38d1a1d557e82d060b4ec5`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 3.1 MB (3097878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0ae4122e18dac51504a788ad60f49ca9ac0b06ecc7c0df42385e05efeb7e30`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90539fb79bdae2b2ecda3212490766029854e00ebfa8dd5d8618634d5b8b789b`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9be2c19d7b9b03e540cfdf2667b283bb1af014d9e13624f42c8a82ae073fac`  
		Last Modified: Tue, 07 Jan 2025 05:24:07 GMT  
		Size: 12.2 MB (12172295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39ecc00ec4deedb989fcd93c0ed30c35bce2b4a1ff298959ccb32e36de91be3`  
		Last Modified: Tue, 07 Jan 2025 05:24:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390093a6b47833931e5a7d49eaf14c5a2d084277e66433ddaefede70ecbee41e`  
		Last Modified: Tue, 07 Jan 2025 05:28:02 GMT  
		Size: 11.0 MB (11036508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117eba0144d9ff31c2b3de4854851aea64e708d53b4b683dbbec9b9a42b2923`  
		Last Modified: Tue, 07 Jan 2025 05:28:02 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1dcf38482698e3267318cca48e6830184ca91d680ce35adc74319adafc829`  
		Last Modified: Tue, 07 Jan 2025 05:28:02 GMT  
		Size: 19.6 KB (19561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73991fa3b4c16127677122e51ad65a8e251726ee2f190736c81e81c7388ecbfc`  
		Last Modified: Tue, 07 Jan 2025 05:28:02 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601a4d37a30d56887fe139b58e19e4f2086bf4dd780090c0be7a815f9598533d`  
		Last Modified: Tue, 07 Jan 2025 18:50:40 GMT  
		Size: 7.6 MB (7604453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29da5a2cbcad2302a13b404f4dcb3b1ea090d93e9814cc3439c7f87292f64d8`  
		Last Modified: Tue, 07 Jan 2025 18:50:40 GMT  
		Size: 997.6 KB (997576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ad05b633c3c75efd4655ad1645519e2a22e3a89084bc058b9e14d0c622c98d`  
		Last Modified: Tue, 07 Jan 2025 18:50:40 GMT  
		Size: 8.8 MB (8784136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c380da3f0690ec8597bfb5981dccb5e215db841126f00b85b63b7c5d6685452`  
		Last Modified: Tue, 07 Jan 2025 18:50:39 GMT  
		Size: 647.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7264f4b533497b24cbe28a8272fa1254c22da577fc8b16bc2eb19c694dcf84d4`  
		Last Modified: Tue, 07 Jan 2025 18:50:43 GMT  
		Size: 59.5 MB (59457116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caefb61cf64b11a72701a56d5ba8b4bfd054e92844edcd59bbe912c2e4e17cc7`  
		Last Modified: Tue, 07 Jan 2025 18:50:41 GMT  
		Size: 3.2 KB (3181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7de1a55817a630870573281ec8bb0088d81f9f2d3161ac27a66558d69464cb`  
		Last Modified: Tue, 07 Jan 2025 18:50:41 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:50b2aeb85a8080e8bbac0a5bce48aa240f809186b5e6a653e6958b37a8664f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 KB (51292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f47e6bafb1583b66b0a2c1e416b30179b517cb04816878e861124646c7bec43`

```dockerfile
```

-	Layers:
	-	`sha256:1c74cc4f6fbfa6b5d03b26e8ab374f61597237c19c3e0cb500037457ee5eaffa`  
		Size: 51.3 KB (51292 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:474118b6a364f4879e7ef9e5bc6b9998b67ec7a1d89871c2db31716fb4dfa4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111398823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7542a0f3efa0c1c98d0e372704d929254d4e421c5d254c8755ffe31183f61844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Wed, 08 Jan 2025 08:00:48 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d40162970ab5d274af508499ec972de793b17d5f14ffee01a11a8e5a5256724`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 3.3 MB (3315021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8949964140eb86d4055cf8d682a19190f4519a76a0135d9c0635b8e590a12`  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc0ab84d61c5b652f4966a78d4064b20a3ee74b683b2fff8a31bfa6695fd46`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dde7237037e4226b0e0a8b4183f319b778e656bc6caf433b716cd8b9392243c`  
		Last Modified: Tue, 07 Jan 2025 06:07:40 GMT  
		Size: 12.2 MB (12172295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d8182f8835afb934750223cf6ef2ee5e57845bf41d77c1a1a389c46dcc86d`  
		Last Modified: Tue, 07 Jan 2025 06:07:40 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459197a9d1e1e37700bd402f6fa0e256dca1da79ac7c852b041bd6b054373692`  
		Last Modified: Tue, 07 Jan 2025 06:12:22 GMT  
		Size: 13.0 MB (12972662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b14f18caf272b0d78fc0fa838cb8e5a5d3dba03d65c87465239491112545d8`  
		Last Modified: Tue, 07 Jan 2025 06:12:21 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263358638c9c19aef0af5ccc2bc76b4c970ad89a30e04e72d4ba2ce05f351b85`  
		Last Modified: Tue, 07 Jan 2025 06:12:21 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eb321374265895ca3c40e8804cfc50a2fdb17127f8970663bd00f30725a57`  
		Last Modified: Tue, 07 Jan 2025 06:12:21 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8683edc75c1ad4124496718acbe69f59cc8d436cd8297aec6e890488b7b0913e`  
		Last Modified: Tue, 07 Jan 2025 16:24:24 GMT  
		Size: 8.6 MB (8594410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a7858b90931740dd17572869253d10b045fddcb9758da6cb14eb858c17fe55`  
		Last Modified: Tue, 07 Jan 2025 16:24:24 GMT  
		Size: 960.3 KB (960346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c6d57d4d51f836c785cb6b789f20a2b61fd5542cd0e1a7f2398734f556d48b`  
		Last Modified: Tue, 07 Jan 2025 16:24:24 GMT  
		Size: 9.9 MB (9906338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8967d90613a771e1fe27e6a3800247dfcde0f390b83c1ba946feb7e71ff33`  
		Last Modified: Tue, 07 Jan 2025 16:24:23 GMT  
		Size: 647.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792cfe164f90457f2e43d797ec835fd9a83d9b87b4f6b20c8e8939598d7f326b`  
		Last Modified: Tue, 07 Jan 2025 16:24:26 GMT  
		Size: 59.5 MB (59457133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a6040c90c2cb7fce1bea76a12ffa689097e6fd0ed6607e2335560aa7d92f1a`  
		Last Modified: Tue, 07 Jan 2025 16:24:25 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cadc018bf62fba51e79f5664fdf3daba8b5a669b40ebb31f79b8dd6ff8d3eec`  
		Last Modified: Tue, 07 Jan 2025 16:24:25 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:0424d94a4c246e60ef05107e52c591d112103f4e74876c3d96fd72e4e41d31c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 KB (51325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c917ce81265bfda0aa4a6350f3aa97fd3351259ffcc4c4f45cabcddcbe93017`

```dockerfile
```

-	Layers:
	-	`sha256:385ed2041e79015ebd129201d21cc5fa9e07dfb6d8ce13e63131f3f7513de469`  
		Last Modified: Tue, 07 Jan 2025 16:24:23 GMT  
		Size: 51.3 KB (51325 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:941e987cea1c8b6eb47b9b18b19e62c3419c77106401e3918106d783a76185ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111462776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da58c44c3f79b00c1ecdabc76e2fcad6d9d1d930fe633aa9b7458dc2bde6879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afde2bd859446a62abcd7e61d85f5789c1ed6f2e15d30d970dd859fa023f8b58`  
		Size: 3.4 MB (3357011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39653cbfb60f695f44f35fab47b137e2442abb3cfcd1fc44ae5030a3428b7c1e`  
		Last Modified: Tue, 07 Jan 2025 03:29:38 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5fe88d2b2f8cbda518ba0ffee49397b9eeec815c5916be7813a70463940651`  
		Last Modified: Tue, 07 Jan 2025 03:29:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bd3996b69dc8733fd7098af70f2244cf05357fc8bdd9ccc4fcab7fe11e773b`  
		Last Modified: Tue, 07 Jan 2025 03:29:38 GMT  
		Size: 12.2 MB (12172284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83173881d41bf6170f4f0efb491db1ad8e766ddf6719ffc9a4c0f20b66e8b26a`  
		Last Modified: Tue, 07 Jan 2025 03:29:39 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09892fa976253cb337cf3b8dda2b166963076e257ecd40e669048841769ac8ec`  
		Last Modified: Tue, 07 Jan 2025 03:29:39 GMT  
		Size: 13.3 MB (13292347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcaa3aed20640e711033247029b1ec3bfba181748e04974afa91ade0624fa55`  
		Last Modified: Tue, 07 Jan 2025 03:29:39 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9abb490980ee6b687bb4e38bdf32f490333815bf03f5345878e746682bcb648`  
		Last Modified: Tue, 07 Jan 2025 03:29:39 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1669e7237f3c436ddd18dd1e06b3869c9807d3772a4980b3ce8f807755e8ed78`  
		Last Modified: Tue, 07 Jan 2025 03:29:39 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13b4d0d62ef0fde656a9a31e03f6821d6630c808675587f2ae4fb6a84b1a2de`  
		Last Modified: Tue, 07 Jan 2025 04:21:10 GMT  
		Size: 8.8 MB (8823252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951abfe66c96e09cc2367a6988c5a9689a72cd9c040bd8b443992a9ece87cd79`  
		Last Modified: Tue, 07 Jan 2025 04:21:10 GMT  
		Size: 1.0 MB (1006388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf4edda2c00612a3f8e99d561521974adeb955b3f8aa9815d29325b12e7070`  
		Last Modified: Wed, 08 Jan 2025 07:33:18 GMT  
		Size: 9.9 MB (9858433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409494579b56700e3691368c45ae2c9412556ddd771b8dc973eb2eb5818168b9`  
		Last Modified: Tue, 07 Jan 2025 04:21:10 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51ef85a0f8a115a9bdc5e1fc19073bc89fa61a26eae1bb463670061e4dcdf66`  
		Last Modified: Tue, 07 Jan 2025 04:21:14 GMT  
		Size: 59.5 MB (59457010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacea8fa0a747fd89461caa8fcf301ffafde318d2c156e975392d0c4bec9892`  
		Last Modified: Tue, 07 Jan 2025 04:21:06 GMT  
		Size: 3.2 KB (3181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a95060fb1c0fb7013dfdef2bb1fc6fd753726a968485b804a8e74014cb2b553`  
		Last Modified: Tue, 07 Jan 2025 04:21:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:25916fa8adb272edac35534544eaaf26d125be8455fb7fa8edc7f3861f9b1208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 KB (51144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8394eb40f774ed6171264f0088b4b4a0075438621c88674751b53454045b78`

```dockerfile
```

-	Layers:
	-	`sha256:477474e8a395968b2430346a02b8e4457efad232033c2b45d45e93acc36925a1`  
		Last Modified: Tue, 07 Jan 2025 04:21:10 GMT  
		Size: 51.1 KB (51144 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:5bda071a51a7a0930681464432bee02541611386c6a7dc05679245347f7e8855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111952046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b0098f3c3aa0f6a66d108585fa7f2895d8793739c46cc037c8aa951230a8a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770cb477b1c68317bfb2860d023b4972e2abdce0461a24b5e3c5d2ff8eadff58`  
		Last Modified: Tue, 07 Jan 2025 03:57:04 GMT  
		Size: 3.5 MB (3462737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8249e7b9c0ca9f3f0f47f0fd9d16c7a924f96930522c42609a86570d36e0ce7`  
		Last Modified: Tue, 07 Jan 2025 03:57:03 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e91a0f9929fb530faadf31b21d97adcb1eb6d139b4a4d3b93c2e76f0c02b000`  
		Last Modified: Tue, 07 Jan 2025 03:57:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b3973ee275154c85849469b1712283c1ccbc0cd3ca0de499553d6b21dd515`  
		Last Modified: Tue, 07 Jan 2025 05:18:29 GMT  
		Size: 12.2 MB (12172285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5972657873b532f084bd235207b72c3298e5d27032319e061e045075fba90b`  
		Last Modified: Tue, 07 Jan 2025 05:18:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b3b2bd4fcf7a0f7aae4af3e2d55ed53be4dc4d825af98e5696b47a5bf119eb`  
		Last Modified: Tue, 07 Jan 2025 05:21:56 GMT  
		Size: 13.4 MB (13439011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a326c648486a087cb18945b7d9b729ef3572b3ca408832d829ec9cec157258bc`  
		Last Modified: Tue, 07 Jan 2025 05:21:56 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d7494296a3dcfbc65e2543e8ef984c3304432aa768245580e20ea92db2e33`  
		Last Modified: Tue, 07 Jan 2025 05:21:56 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2aeb1b5f2dfae3d72f72744bfadc91a2a4727e562e14e8a83b70aac08cb07`  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c46cf04f44415a714b15a08127318b7fe8eaac3fffc8841bf8652c22584f533`  
		Last Modified: Wed, 08 Jan 2025 07:33:19 GMT  
		Size: 9.2 MB (9169353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd4fba8461f2695d64761aa635409586542232cd03086344d85260ab59e1e46`  
		Last Modified: Tue, 07 Jan 2025 10:28:09 GMT  
		Size: 950.7 KB (950667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61a743a3af824fc21e0c5f822cc62d87306a52a0f30e29295d2d46dd3bc25c4`  
		Last Modified: Tue, 07 Jan 2025 10:28:10 GMT  
		Size: 9.7 MB (9695502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dbc73f6c937f68c2ca2e9e5fc44f20f942d040f1019872a1b9e6ee9c14e216`  
		Last Modified: Tue, 07 Jan 2025 10:28:09 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1462641d4f173f92351e0fcb479bb41778965c7b70e3b0e489dead8fd1b7cf4`  
		Last Modified: Tue, 07 Jan 2025 10:28:12 GMT  
		Size: 59.5 MB (59457120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50978c226109596ca9c04622ffc3a3044f0cde0ea0ddd3a660da9fb0e369025`  
		Last Modified: Tue, 07 Jan 2025 10:28:10 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7df360741a7232a6b54f13bd35a40847003257b3bad6e2c363123ae1fe6922`  
		Last Modified: Tue, 07 Jan 2025 10:28:11 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:89dc4cf721bdfe294ab7533863dfcebfa85a549fa340b07747677ae9fafad93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 KB (51217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba241a41fc3af936b3cc9540c6a69a88cef10a2e48594795f90a69849e48b202`

```dockerfile
```

-	Layers:
	-	`sha256:27e2dc0ab4e942b874865598df5b00cafd564aed2b058086c4487f59c8457717`  
		Last Modified: Tue, 07 Jan 2025 10:28:09 GMT  
		Size: 51.2 KB (51217 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:2e41095e5ee81bb2584f53ad761090e5be4fa6dd69ddaec8b20119a1c39371d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109831863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e937a1a85e074975a96156aec1c9f4663076928ed12b4724e983b0144abc57ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c725d2b7cda04131943f46fbc9ab5daedc4d0bdf3c30a0e37da7d34d14947341`  
		Last Modified: Sat, 21 Dec 2024 09:20:51 GMT  
		Size: 12.2 MB (12172525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711edafacbefbcdf2dac55ada0d1a7a162cbf509eaf229c0a3fb50b55dba5dea`  
		Last Modified: Sat, 21 Dec 2024 09:20:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb772f0f4be3ba733f071837b62477b2daf71e1d9c183ab61f98645687f20b`  
		Last Modified: Sat, 21 Dec 2024 10:09:23 GMT  
		Size: 12.7 MB (12741335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd122e552aba01f4120ea99b2d763b434fa0e72279ee26d80dac1412c4d22e`  
		Last Modified: Sat, 21 Dec 2024 10:09:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bf562dab2e4e07f18a80907746097a85fa9f24e42d2fb241494260e4370bd8`  
		Last Modified: Wed, 08 Jan 2025 06:33:00 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb0f64acd62efcb6fd3bb51cec1762fcda8690fd8004e4fefccb881d4bc4eb0`  
		Last Modified: Sat, 21 Dec 2024 10:09:21 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb9fd80640c37d1e2825172c94c240365332cc6181a8b788fad1cb97419f5a`  
		Last Modified: Sat, 21 Dec 2024 15:26:00 GMT  
		Size: 8.5 MB (8513946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83ded020727cc877ce777b46a739b23fda8c1e5fabce44f38af29ee5ccd53e9`  
		Last Modified: Sat, 21 Dec 2024 15:25:59 GMT  
		Size: 1000.6 KB (1000581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2938a2a1344167d9f57d7514fe61a7062e3678352b4ec479814d074f84e120a3`  
		Last Modified: Sat, 21 Dec 2024 15:26:00 GMT  
		Size: 9.1 MB (9107863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc99b19ab0c7beab710758b5fe38238058a0f0872d7ad6b0ac98f05fac0e715`  
		Last Modified: Sat, 21 Dec 2024 15:25:58 GMT  
		Size: 645.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f66385196c7efb19b91cbc2a16bf6c30db8a42c278252eaa69301a7623ebeac`  
		Last Modified: Thu, 02 Jan 2025 19:30:55 GMT  
		Size: 59.5 MB (59457866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d2d176127fec5c7fe46ea6ebe7351461b3c9ea95ca2990148a682716ab88a`  
		Last Modified: Thu, 02 Jan 2025 19:30:46 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f19c99b0a865111a17a3079114e75d50b5b3acfac02482b8f4bb666d7da73`  
		Last Modified: Wed, 08 Jan 2025 06:33:37 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:cf94de822ab7f3c66cc965c94a4b2a36519a9a5cf0d3121fe13d5d4325ea649a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 KB (51225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8623f3348fe96b41571d03b308aded8ca0ab4805c3165af450a699dda4d8ccfe`

```dockerfile
```

-	Layers:
	-	`sha256:431ee2b8807675e01ef79e97e03fb64e82bafba214a077f6951110972aa6c9f9`  
		Size: 51.2 KB (51225 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:6945946d60fd67a4005093281520fd448005060008ba411522add7d4daeb7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111121749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35179e755fc8be1e9aaf30be857002f719c7dce40ef0a21f5002ca0abe6892ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;             export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81298346f7998688090749dc4a0c5695063618d53944be66940589a7c4cec0f0`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 3.5 MB (3546676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ae0e9cd63cfedbc820ff5cce925cad38492ddd41b8ef4a7dafcfb8c8699fc`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19010506c88f12a8f1bd5ca006528412ce5ffcb1745e840ef9578eb779ec3a4d`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb27512c316c7ad720aaab818c919c83290166bb1961c12a19180df3a8179cb2`  
		Last Modified: Tue, 07 Jan 2025 05:22:11 GMT  
		Size: 12.2 MB (12172294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a9096893d0fbeeff8e0e9b1328db92aef855111359913890dbb2b3b7dd650`  
		Last Modified: Tue, 07 Jan 2025 05:22:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12eed59818e492a9c6bb71faf0d2e8236c3d987578859f109cef052a7aa8164`  
		Last Modified: Tue, 07 Jan 2025 05:25:47 GMT  
		Size: 12.9 MB (12931967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebad769245db981cccadd566f74477c739aab2a3dd0f325328f952a1e1cf7`  
		Last Modified: Tue, 07 Jan 2025 05:25:47 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d95c7bb73344d8ce20e229be73835a580e5515a8b21c311a49a56dc8b8e15b`  
		Last Modified: Tue, 07 Jan 2025 05:25:47 GMT  
		Size: 19.6 KB (19555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4495e526087badb927ad6529b4f0aaf10c21b163fa580f0ba6e13d33466e4b`  
		Last Modified: Tue, 07 Jan 2025 05:25:47 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d715d2d289a2c7978a9c8cfe0fc053d1e970d27574a157044bed81b1380df9f2`  
		Size: 8.9 MB (8883026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f9f7c7ace46396d093cbca3faf0dd06b05c15b38609090351d6450c519cc07`  
		Last Modified: Tue, 07 Jan 2025 16:00:51 GMT  
		Size: 994.8 KB (994820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5251697187bef5ea5c0d38a1f293612c145c80d80bec563699a195b67fee20`  
		Last Modified: Tue, 07 Jan 2025 16:00:52 GMT  
		Size: 9.6 MB (9638723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd080d24a02743154ec84112cf0c93589a98bf0bd01c23f6bd78573670a5975`  
		Last Modified: Tue, 07 Jan 2025 16:00:51 GMT  
		Size: 645.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2125ed7df97484f19c876d8f2b3c8cfd697a1ba8cab63017de0d9d7efa84e045`  
		Last Modified: Tue, 07 Jan 2025 16:01:52 GMT  
		Size: 59.5 MB (59457181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836233abc9cd38787effe734e57354e0985ca8a84c369ecf58e32f7d49d10546`  
		Last Modified: Wed, 08 Jan 2025 07:33:22 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1a13a7bacfbab89885aa06fdbb96bd963a23fbaabd4fda5f9a81be43d47c74`  
		Last Modified: Tue, 07 Jan 2025 16:01:51 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:e9636056581b761a51e42a9e99b63c31b277c93646022994b2d27a0553c4369c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 KB (51173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a784e137412c1747fea6a60367111a3297f9e10a59d63ccf91e0a66d618f1655`

```dockerfile
```

-	Layers:
	-	`sha256:a8927412291adcc53b3cc64eef9289926d5df242ac1e9c46964ea40cae922b4b`  
		Last Modified: Tue, 07 Jan 2025 16:01:51 GMT  
		Size: 51.2 KB (51173 bytes)  
		MIME: application/vnd.in-toto+json
