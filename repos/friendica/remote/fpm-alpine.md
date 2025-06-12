## `friendica:fpm-alpine`

```console
$ docker pull friendica@sha256:5a83662aca11e0067ddbdd0f7d2f2735cb35d081ac36660d35ac5a363da2e792
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
$ docker pull friendica@sha256:6ddebb0e7fe68afbe48c9930c391472b28c6c2273f6c3a4a8c68612b9aa4d0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6a63ecb5d867ac05f394ee6a92233210a8ae89c746ff6db6dcab3f69d5b9b`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94070b1555eb9d39ed22e649983becf2bb72fb22585bec7a49df36fe4190e13d`  
		Last Modified: Wed, 11 Jun 2025 00:03:27 GMT  
		Size: 12.6 MB (12576238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82f137985dae9d6f442dae7a80f57cbc8e5053df43b00bbbd9c15302ce781fa`  
		Last Modified: Wed, 11 Jun 2025 00:03:27 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb82a003d3c63378e7b84743d024507052e3b2e1996a8e94c844c881b05261b`  
		Last Modified: Wed, 11 Jun 2025 00:03:28 GMT  
		Size: 13.3 MB (13261198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03c593a7b00608ea5c8534062562e946bc0a3d159cf20ea6cc8c7dfe01e57e0`  
		Last Modified: Wed, 11 Jun 2025 00:03:27 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97896200a5c564e7c88a17f3acd070645c4775fd2e146a8e3bf7e792bf0a3d94`  
		Last Modified: Wed, 11 Jun 2025 00:03:28 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c93710be8c8a941cb7c19437dc1eef7f885ec0979268aeaf706f3b24f3f415`  
		Last Modified: Wed, 11 Jun 2025 00:03:28 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db96fe7af466b21033597e4637266f57e15b0b6941995c5f3c45c9a4c696b720`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 8.8 MB (8750971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008df670fcc76ce333b794578e6acf40229b0e69cffece457a3ea380bc758bde`  
		Last Modified: Thu, 12 Jun 2025 11:14:18 GMT  
		Size: 1.0 MB (1031315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37cde83bfea35c21d990441fa09d517d8fbc0123a7b351b558f4329c84cd100`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 9.8 MB (9822831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be2bb0952720b85c59f0e051f8870a697de4d60d9207b07bf9cee126a18c59`  
		Last Modified: Thu, 12 Jun 2025 11:14:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ad5ad81462fcaf227815391e653fdd568b8b30d2cd5109f2efaeda746c12ff`  
		Last Modified: Thu, 12 Jun 2025 11:14:30 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fea91a4c566c5d3564de78f565a60240fc28806e9634e32bd58055d3f7c56ac`  
		Last Modified: Thu, 12 Jun 2025 11:14:33 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f47aea633a68dddeb5da73d2efa12102244738de244ca46be10141c05154b8`  
		Last Modified: Thu, 12 Jun 2025 11:29:32 GMT  
		Size: 59.5 MB (59458992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66df916de4da8f2d1ffc31536e3fa4749d11e79b41f84f1987cd29a34b129ff4`  
		Last Modified: Thu, 12 Jun 2025 11:14:36 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58f0b720147b158d61b914bfd3dc1b9aaf86638e5cbe62cc7846a730d48ff25`  
		Last Modified: Thu, 12 Jun 2025 11:14:39 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:d807c4b7861583495fa994b744eccd054c488ea31e170e50532f513af8474a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 KB (60370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b5c6bbf8b00bd8e723ac41907ad5710af73bb9637fb2067d4ded64dde14f99`

```dockerfile
```

-	Layers:
	-	`sha256:f99137702b332a99b9a807ffcfe8f0c652345ddb0a9d2456f0dc68fa4f332d6b`  
		Last Modified: Thu, 12 Jun 2025 11:28:52 GMT  
		Size: 60.4 KB (60370 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:9b3c9c5d2837c1ca1bc08c5381ebedc4ad200ee654bc6f4711a5c57308f84cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109558339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1c6240dc0e9dfaf3796d2b5cc62e632e1ede3ecfafb81bf4fc6cc10b87a5af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e3e8fed6eecaa5f4e5fda14677241e20bfad2ac9033a025d69590236c98a9d`  
		Last Modified: Fri, 06 Jun 2025 18:13:08 GMT  
		Size: 12.6 MB (12576056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f007accc5583b56c774f899c6390d0bec566288561cf5f90e528cd13eac732c`  
		Last Modified: Fri, 06 Jun 2025 18:13:06 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4ac2f9ab8be15310abc7fb7a3a85f3d6b1f3dd83271dca52ba65eab56425f7`  
		Last Modified: Fri, 06 Jun 2025 18:18:05 GMT  
		Size: 12.7 MB (12724080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8adc1f9a5ccba7c16aa4abfeb6a8486f5c14903b3237b5e4e6d88703d4cf6b`  
		Last Modified: Fri, 06 Jun 2025 18:18:01 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19a8d72793a184da4f8d53d6aae8f2441ae18360fc68f9896ed4ce5aa2289d`  
		Last Modified: Fri, 06 Jun 2025 18:18:02 GMT  
		Size: 19.9 KB (19869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e119264e541d14a22aca91b6d530988fd3a8d5480a335bc3adaf8b7bdc66eb`  
		Last Modified: Fri, 06 Jun 2025 18:18:03 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ba1fce83f20514d95d2ddb2835f7b826a1d5e07d68032e3d6d2465022a47ee`  
		Last Modified: Fri, 06 Jun 2025 19:31:52 GMT  
		Size: 8.2 MB (8221438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe479e8ad70e7dbdc903a4dfb78095d5ea5e6450a58656dd6d19faffa4cbddb`  
		Last Modified: Fri, 06 Jun 2025 19:31:49 GMT  
		Size: 997.6 KB (997570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27145deddcabf16edb0633a61b42ed1cd7f9a67b3c8e48049a3548c7d4b804b9`  
		Last Modified: Fri, 06 Jun 2025 19:31:59 GMT  
		Size: 8.9 MB (8868940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e863613ccd11913d1d3a38977eda9e62d67fa38bddcc733174d8d2c4f0635268`  
		Last Modified: Fri, 06 Jun 2025 19:31:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4b71db6ac397b666106a856b36477de68ded66c3d0c75e184adb37bfc09e93`  
		Last Modified: Fri, 06 Jun 2025 19:31:49 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491ee09cfb8d2bb53adf2bbe3b5e299617fb38f1c3678bbf8623660a5eee158`  
		Last Modified: Fri, 06 Jun 2025 19:31:51 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d50cef8751d2ed65141659168463362d5ffb2e2838601d8571b2d37ad2a6a88`  
		Last Modified: Fri, 06 Jun 2025 19:31:59 GMT  
		Size: 59.5 MB (59457957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ff0f4f37c837d252384d4c2251150306c13e17fc0ea7d0fc6289c30c82a7a`  
		Last Modified: Fri, 06 Jun 2025 19:31:50 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a4c56c9556053fbf077787c1a3584aab1c88359ae2e1a66b35d9a838307aa`  
		Last Modified: Fri, 06 Jun 2025 20:20:08 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:4017d80619b9095954c34e2379f16ad73ee66663ceadbbae9acdd3692319aeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 KB (60510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf5a4ec910e46b661ebb52d7e31329c535682951983430e952534b5a1521ec5`

```dockerfile
```

-	Layers:
	-	`sha256:76ec82ac4ebd01dbee2d37343181056b59f18f048a9c7838ca3bc990c9e66f21`  
		Last Modified: Fri, 06 Jun 2025 20:28:41 GMT  
		Size: 60.5 KB (60510 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:6b53938e83796af8dd9954bcd7962d178537cadf501a1276a71bc3fbf827ea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107350845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f467370f9570ce8afce7a5d0b5acf1f33f38de6107e743213130f9bf939d48`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
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
	-	`sha256:0e4283ac42685038a3ed46bf05fa54ab4bfdaa975c17e26e357143c8c0323ea7`  
		Last Modified: Wed, 11 Jun 2025 11:58:48 GMT  
		Size: 12.6 MB (12576225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741687b0c9e57be621e022c7972e29e049714b0076fb944fa8713a06d0bb1bab`  
		Last Modified: Wed, 11 Jun 2025 11:58:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08a3c676bee3ca3ea309b1b4da6db64f4e2308209926dbbd58055cba3c9cbcc`  
		Last Modified: Wed, 11 Jun 2025 14:30:57 GMT  
		Size: 11.3 MB (11284618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4416e852da4c41efcdd6c391639f54029fbcc58339233d239ee6ba226fcf4`  
		Last Modified: Wed, 11 Jun 2025 14:30:56 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1888b69799ae098e199ecdf068e825e5470de6c91593dad7209ca7ce43afdc65`  
		Last Modified: Wed, 11 Jun 2025 14:30:53 GMT  
		Size: 20.0 KB (19985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8604ddc2d70d5a8cac9a2deb8a8953d575f9d49c24f2b6623140c6a9681d966`  
		Last Modified: Wed, 11 Jun 2025 14:30:55 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27d8489d0bd6542036dc7552267428062e20aee64e4dc05d1d758c38b12fa9f`  
		Last Modified: Thu, 12 Jun 2025 09:13:47 GMT  
		Size: 7.6 MB (7620690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c755f0c36f5b89357fd62f927f8c36e7280d1c734677f435f5f3fc61eb0cd2`  
		Last Modified: Thu, 12 Jun 2025 09:13:47 GMT  
		Size: 997.6 KB (997601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af63f48cf6c86d20a53a6eb59d58f6a359c301dbf936d348a7b3f0e818987935`  
		Last Modified: Thu, 12 Jun 2025 09:13:49 GMT  
		Size: 8.9 MB (8907578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e15bedb3ff86c973054a97e7d4d07a96100840e98cba2e8e1c214360b66acd`  
		Last Modified: Thu, 12 Jun 2025 09:13:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6908b2fd5a100278339abde5308cfed9e61bdd530e63a311953e495778d9d045`  
		Last Modified: Thu, 12 Jun 2025 09:13:49 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497d1de7ad88dff0a301339e9b5d09b87995de7e2fe9f4923f89b4b6ce7ef43e`  
		Last Modified: Thu, 12 Jun 2025 09:13:48 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79320efa11c4ace8fa6a84a61220158cb6afc052fc46dc008d01b7adaa3d2262`  
		Last Modified: Thu, 12 Jun 2025 09:14:00 GMT  
		Size: 59.5 MB (59458875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3a5bb5946dfc2fcc257a7247df2d6438d48b33536739737a88e9c1614ab3f4`  
		Last Modified: Thu, 12 Jun 2025 09:13:48 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8694fb3f1333bd1e6b4acd807d1115b0956faa3313baa6b3fe6203b89019c0`  
		Last Modified: Thu, 12 Jun 2025 09:13:50 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:a3129c28fd91e6020fdc313967336884ef47e7bd087b40ef485bd23f7d7c4bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 KB (60510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63003383a60c7a7320f8561292144ff4cc09230cdf2122905c23ddf4552bb732`

```dockerfile
```

-	Layers:
	-	`sha256:89c35dafff66ea6ec7edf92760c0c083ca5d4814cc1dd2df679c70af5e116593`  
		Last Modified: Thu, 12 Jun 2025 11:29:00 GMT  
		Size: 60.5 KB (60510 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:6815dd55195b44c459ffcfc4a17001ea8b2e6f02d618e9d0cc6ab8afa817ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112534565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbd208db87569a2745940add35d28f7cb6d63559a7ac2a1009a014bdafb81f7`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05602459d95eaaad97b5b9b000a31ad26f0eb610cd660e6c00286ab14e83d6`  
		Last Modified: Wed, 11 Jun 2025 09:24:40 GMT  
		Size: 12.6 MB (12576220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6009a2fef25c68c3e1fe283a09950eaaebf7b5f614e8bb226e39e53cf92d1`  
		Last Modified: Wed, 11 Jun 2025 09:24:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f115d6f00f4bbc4cc814ae5670851a1f02750a06b80561a1ee2185625f162d1`  
		Last Modified: Wed, 11 Jun 2025 09:30:44 GMT  
		Size: 13.2 MB (13247738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc702833cec2a0a6825bca526fd38028f3799551063bd1048096ba9ad7ed67cf`  
		Last Modified: Wed, 11 Jun 2025 09:30:42 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6580f3bc4f6b18f970b0c9b596701e82571b2c6d73d9aa40230f66dd8d5d4d`  
		Last Modified: Wed, 11 Jun 2025 09:30:42 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e2521d26864b360fc0ab74e2f1eee99d2266ab700a7983d2fef138d11d4b3`  
		Last Modified: Wed, 11 Jun 2025 09:30:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878f9fe3188b761678ead089f40f54f3082abe4a1c9718eae0024bd50ecfd111`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 8.6 MB (8619956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039fc723e7b9a6ac1b377da36df7b45acc1d778b5bf6003cbc39fae2c067e7b4`  
		Last Modified: Thu, 12 Jun 2025 10:14:55 GMT  
		Size: 961.1 KB (961058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16eccd937545ea3ddc3e2c98b506287f639bfb638e0c4a3510819f714c2721`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 10.0 MB (10025333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d54bc4d9dd4d0ce1e51154d14e87bd86d426f1d03bf87c101017a36f45a2c4`  
		Last Modified: Thu, 12 Jun 2025 10:15:00 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8824602691e72cac48478ed8a8b553fc308a315eb911b0b6ddbeeb394c9f567e`  
		Last Modified: Thu, 12 Jun 2025 10:15:04 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec82e0e61ef13d61c63b3e6cf62bdad3bd07974ce1c9406119fb85981298384`  
		Last Modified: Thu, 12 Jun 2025 10:15:07 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58280a4ad606b1ccba7271b93ad1566066879555ae48ba5cb25b479548616feb`  
		Last Modified: Thu, 12 Jun 2025 11:29:33 GMT  
		Size: 59.5 MB (59459011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a349b4861d9b4b1e760bf034574d3caae5fc461f3cbb9d12d7ff7ee96d52924d`  
		Last Modified: Thu, 12 Jun 2025 09:35:09 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0637ab161735ee0f7a3005096bd0e2ad900a7bff820a176a0aa34b8823d9ea3`  
		Last Modified: Thu, 12 Jun 2025 09:35:15 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:91910e44f2d214cc16a5f8d15cd081188d660b4df2ee4fa9f08b64d49acceccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 KB (60553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbb78423cb403df6c086c6e9caabeff117f9a064e9b81149d20e3c585dde7d6`

```dockerfile
```

-	Layers:
	-	`sha256:359369b1cde9c046464161b7914a31fce499cdbb24f4e20572b1cb9b91a2501c`  
		Last Modified: Thu, 12 Jun 2025 11:29:03 GMT  
		Size: 60.6 KB (60553 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:426c097cb6944018aa9f7e1706a30681e720421e53778526977d5347b595d53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112640642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a693bcfa87db4705440d528320075514a1aff7d67ce0a13ab075f420898b5c54`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad911242465f6c0cde3d5c906eab3d46a4a5ef9c7959a31a3d1fa6e2c6310b1`  
		Last Modified: Wed, 11 Jun 2025 00:03:49 GMT  
		Size: 3.5 MB (3527771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a9a58e768c9776636ca4a31bfe145f187a1aa794aba4343c2a36d409fbcbf`  
		Last Modified: Wed, 11 Jun 2025 00:03:48 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d40d469b1d335f5f75a3ca1e9009ea157e2d54d9f8f61e936caed41062bfa21`  
		Last Modified: Wed, 11 Jun 2025 01:12:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247f555e5a9a340d6f13b22e0edccaca28f84b48a0731579c4ef1e178998fa81`  
		Last Modified: Wed, 11 Jun 2025 01:12:58 GMT  
		Size: 12.6 MB (12576205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba38f0252f574dd5ecbe60077dfd2d4bb6b4d891de9666188cfc453d01b4f9e5`  
		Last Modified: Wed, 11 Jun 2025 01:12:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8dcd7c62a9397ebd3cdb5f345e9a780ee480007c66f294144644a649cca201`  
		Last Modified: Wed, 11 Jun 2025 01:12:55 GMT  
		Size: 13.6 MB (13568984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9804203e712fd340caffff86c88e0159c4b29e9da61cbead1d4e61bd1c4344`  
		Last Modified: Wed, 11 Jun 2025 01:12:53 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d14795a33b66d09a16300a068ab99ef988e380bd1b6ca61c3804e9cda5c40`  
		Last Modified: Wed, 11 Jun 2025 01:12:53 GMT  
		Size: 20.2 KB (20183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0709fa6924910761a3c3cfa28ac96d5b7c288b1a728826a48c01351ea1f75c`  
		Last Modified: Wed, 11 Jun 2025 01:12:53 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265b04fc19f382df5c6b5b6c5a42628b6c1d5cfeebc1f3bf8f38ba7e81f2edd4`  
		Last Modified: Thu, 12 Jun 2025 10:28:43 GMT  
		Size: 8.8 MB (8845865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be81d501dee5c21e22fc7c5bc4d81e7cda4b16bba860b7e4b8aaac1e20f07c5`  
		Last Modified: Thu, 12 Jun 2025 10:28:41 GMT  
		Size: 1.0 MB (1006240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9e63b117a1e774b8e3e55415301fa9f0b1c732a653fff46a23560d52413d9`  
		Last Modified: Thu, 12 Jun 2025 10:28:36 GMT  
		Size: 10.0 MB (10001681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21b55c96300fcb42c24aaeb04006addac1c357eb4cb2aed9c8339601baebb03`  
		Last Modified: Thu, 12 Jun 2025 10:28:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060b85204b4a9f9d011c6f9448b209f093ee29c44d1529d00a8b2ac30e02e33`  
		Last Modified: Thu, 12 Jun 2025 10:28:35 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f846382db06936758b83f0f5df6ac2c1a7f96e7bfc128c4b864b4f496e0e601`  
		Last Modified: Thu, 12 Jun 2025 10:28:35 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11cc990a8e0fdc365c02a789c854b32d2d4544b05352507c140030eddce2454`  
		Last Modified: Thu, 12 Jun 2025 10:28:39 GMT  
		Size: 59.5 MB (59459066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318404c0b77a7af2c81d01870d1790626c776d973c7d88a75174a921937bcb31`  
		Last Modified: Thu, 12 Jun 2025 10:28:36 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3df9370c64afe710d60b1abce685b49680f80e4b8be379a208bd7e96d62e04`  
		Last Modified: Thu, 12 Jun 2025 10:28:36 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:9bdd8b22044e0111a62a7c05bafb872425b56f689c9c0062ece8ae916f7d64dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da8533ec4f40b222455514499240a6de40bf995d57a9b14564ce59c06794df3`

```dockerfile
```

-	Layers:
	-	`sha256:da692494d1e63968cb29091208fc117f1fdaadd3ee93e005e28961eb76cfb8aa`  
		Last Modified: Thu, 12 Jun 2025 11:29:06 GMT  
		Size: 60.3 KB (60340 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:0a68682ec78c14ab2e0f17dad88dd1b1129f831c4256c6699e5467f811100992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113123923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf560520a1370590abbb429d2c7550ed71198aadbfd134258f30ce40f14a013`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e98527d27dfe373bb05fe4a32feae4e983c3ea61c6e75a47cd18dbaa9f06e4c`  
		Last Modified: Wed, 11 Jun 2025 09:28:04 GMT  
		Size: 12.6 MB (12576214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb3390ac49f9efbf6d20912051491cbccf67620aecd18d32594e6dd87b74ba`  
		Last Modified: Wed, 11 Jun 2025 09:28:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e6a25b6101b313fa34875b028b172cad9c9680cee80e292f115adba7417cee`  
		Last Modified: Wed, 11 Jun 2025 09:33:22 GMT  
		Size: 13.7 MB (13731670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fe4afc2b18dee11686be563ce289d666303ac2ef846948fecd695bafb4e813`  
		Last Modified: Wed, 11 Jun 2025 09:33:18 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b543d2869a32f83c6fb938daf392dfd4df558264decfb7bf19f32c754301f3`  
		Last Modified: Wed, 11 Jun 2025 09:33:18 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2cb99f9caafa35970bee68bb6e56af35e3687bf7d9e6a59a802258a0d7675`  
		Last Modified: Wed, 11 Jun 2025 09:33:19 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb273172bbbac8098bc0dc97824323277bdefc12f5f6b4ca00ca0771007507d9`  
		Last Modified: Thu, 12 Jun 2025 11:29:30 GMT  
		Size: 9.2 MB (9195012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862a2e48eaf1b1e8ab6a538988ef442fc04927fc0c122ebaf865c17b95e023c3`  
		Last Modified: Thu, 12 Jun 2025 09:08:38 GMT  
		Size: 951.4 KB (951351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecff4f2014cc78f75849d9f7001e2aaa0105ce9cfb7a3e81c1a19ec33e5a2d7`  
		Last Modified: Thu, 12 Jun 2025 11:29:30 GMT  
		Size: 9.8 MB (9822665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05302e99fd3462f2a6da0071ad0f6bcc6fa1a69c7fa9cd35426d43f1ff591d0b`  
		Last Modified: Thu, 12 Jun 2025 09:08:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4a70ce8c770f5a92dd31a2e0286305f7f56654148b1e43ac2bec5c5644abe`  
		Last Modified: Thu, 12 Jun 2025 09:08:45 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c776d04b9e9f6ed9f0ee066c974835895f0466aef4effe9e2bec40f76cf1527c`  
		Last Modified: Thu, 12 Jun 2025 09:08:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4a733f0800d13273aadab93a0b093d57d890fddf610808a994bc8f532e7885`  
		Last Modified: Thu, 12 Jun 2025 11:29:33 GMT  
		Size: 59.5 MB (59459030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f7a86feef576d03fc5311e11cba6108cff6671ab7feb17612b0ab69f650d1e`  
		Last Modified: Thu, 12 Jun 2025 09:02:24 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae9830f34ddff91926db18bfa690d72192ad1bfe03c6f56e1b52f4d11fba0df`  
		Last Modified: Thu, 12 Jun 2025 09:02:28 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:7706db81fcadce6ac98c098075763344e620888bb1911b1e3751b3ab1246a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 KB (60414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aa80b6b1b41507bbcb8598376e7fa2ac25cabcc06e98549c4bf44a41a9d9d9`

```dockerfile
```

-	Layers:
	-	`sha256:5d06cae7813b98cd7842bda83ca618b4b75545e4fb3d58a2c094d8669957b95b`  
		Last Modified: Thu, 12 Jun 2025 11:29:10 GMT  
		Size: 60.4 KB (60414 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:73f332c905270a2e7094e50e61e6fa88e604810c8e013e1bfd6bcc679d6db72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110743929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37639dfd9fe534662e11a0d36f897fb697acb9995b889ea42f4df3777d846a2`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
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
	-	`sha256:bba1091c9bd27a689d500d464782b521cfe4d3ba3773b31deaa918405bf00360`  
		Last Modified: Wed, 11 Jun 2025 06:22:26 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ac07f2e6ef175326e50c1bd2cf85379e771e86f4a328b5c55b1aea2a599461`  
		Last Modified: Wed, 11 Jun 2025 06:32:48 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c55ca73095fdaa794aecbd4c3aebff6b42c5244d706c4e6738e71ae615d03af`  
		Last Modified: Wed, 11 Jun 2025 06:32:53 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c645e919d16a33d78a137c93aeea649d028d210cf13c3c8ff265d891300a8e`  
		Last Modified: Wed, 11 Jun 2025 14:46:12 GMT  
		Size: 8.5 MB (8541742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d600b59e825f73f34851aedd55aed8c961e8e726f96223be55828e21e5223`  
		Last Modified: Wed, 11 Jun 2025 14:46:09 GMT  
		Size: 1000.8 KB (1000805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e75854b2f685539858040890b76c463291ef96594c5f9360814ffd9f61ffc`  
		Last Modified: Wed, 11 Jun 2025 14:46:10 GMT  
		Size: 9.3 MB (9251544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8264fc02354c4eb10990807f518a140c78aad29339f752609fd31f34e759d9`  
		Last Modified: Wed, 11 Jun 2025 14:46:09 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c05ac806666cd314befcad0b6b373481321d2e99442caa71585563d4e737cb`  
		Last Modified: Wed, 11 Jun 2025 14:46:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb881880a5e24a3c76b4cb52ec7828f4343d369d3fcd2d2a4336af49d7a1736`  
		Last Modified: Wed, 11 Jun 2025 14:46:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f4b19066c88f4db22f0413f546daefc4dfdbf98dfda6b5bd831339987de0a7`  
		Last Modified: Thu, 12 Jun 2025 11:29:32 GMT  
		Size: 59.5 MB (59459058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f3e9c5a6cdbdc171eba73c744570f7b14ee735ee7e3716ccfb272a997114c`  
		Last Modified: Thu, 12 Jun 2025 09:15:01 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f014287a43bd3534e817d74603b7b03d83ad7ad9cdee3248854bdcd5bb7c6662`  
		Last Modified: Thu, 12 Jun 2025 08:53:07 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:1ce5a258f5501403a14271e1705c101944a928da090d61a5a3841946a0c985a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 KB (60422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a58466566e0fdb760daccab87e73fdf489b34f14117d51e9baefe072a89242`

```dockerfile
```

-	Layers:
	-	`sha256:34eb9fe71e40b8a36c2e26080d7e611a36aabb81c18408d9515f5fb367922c91`  
		Last Modified: Thu, 12 Jun 2025 11:29:14 GMT  
		Size: 60.4 KB (60422 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:a496c18bd7b34c3c15c4b459403d23b82ec63f87e853b10ba61a77b4e65e9d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112295496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3181531688f5a66927d82c5d93614363600f31ea63e92fc97833cd6db11a92c8`
-	Entrypoint: `["\/entrypoint.sh"]`
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
ENV FRIENDICA_VERSION=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_ADDONS=2024.12
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Thu, 17 Apr 2025 16:08:36 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Thu, 17 Apr 2025 16:08:36 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apk del .fetch-deps # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Apr 2025 16:08:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Apr 2025 16:08:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9334ce794586a4a7b7438e664ddb5b86e3cce1e0a2fbc690532ce8b60488510`  
		Last Modified: Wed, 11 Jun 2025 08:16:40 GMT  
		Size: 12.6 MB (12576237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b5f7350b3a92e0711dac2da50783a7725cd1b40cd633e7547d23d902a052cd`  
		Last Modified: Wed, 11 Jun 2025 06:28:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06397ddb79c96539ad6e6e015a2347219e602ac265e8c83e456493f63b715bce`  
		Last Modified: Wed, 11 Jun 2025 08:16:50 GMT  
		Size: 13.2 MB (13209660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2df9cd85e7507e6e36c9fa149c62836bd4b44b04ce7b6e06f9a693162ab357`  
		Last Modified: Wed, 11 Jun 2025 06:31:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c988da2e76568a30f08e12cd28d8d8d543c44ca483fa49f5c95e8701f8b897fb`  
		Last Modified: Wed, 11 Jun 2025 08:16:57 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6af9f1c9f1c764ed8d022da83252658376c197bd19dc5d80b780570bc4dc7b`  
		Last Modified: Wed, 11 Jun 2025 08:17:02 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3962f62d49d12392d1353cff91aae9b50e5908b122ae865d0280394db5c636`  
		Last Modified: Thu, 12 Jun 2025 11:29:29 GMT  
		Size: 8.9 MB (8910002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effbad2559dadc7e10164a9175f34528005d9b744cec2834c9292771cfd21c6d`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 995.5 KB (995542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0741cc922ca982f722b062f0aaff5312315b565a37524c3b47c254c152bb503b`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 9.8 MB (9759823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a9b0a129910055a4572c96a6d99c7314975186dc9740319b49322e9640402`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0512ac2962f732c38301a68d8f57eb0ae5f228c1b5c98ccae877e03fee04bb4`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24bd1e17f359d19bd0ad66d2b2d4595f2e64e36908d3b99ebcbb453fa4ae5f2`  
		Last Modified: Thu, 12 Jun 2025 11:29:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28954374123bfbdec24064d7474ef877499f308b87177cf9fc16c53dc9f4014`  
		Last Modified: Thu, 12 Jun 2025 11:29:32 GMT  
		Size: 59.5 MB (59459065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60ba46dc15323ac5808ca539973dcebade534ae94ec922d3b0fef5a5c797eae`  
		Last Modified: Thu, 12 Jun 2025 11:29:29 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa4ba123af92a840cc7b56e5e5194e114a26b5aa54d5cc0c23a06296d675b4b`  
		Last Modified: Thu, 12 Jun 2025 11:29:29 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:4399803c4234784945c91086ae28b009bb91ec30aa8c16b2d014bc1a7ce512d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 KB (60364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf71b850efa1f40f56d40b4e4b8970060621246306c81e53915b1425179b189d`

```dockerfile
```

-	Layers:
	-	`sha256:0d38ade448138ffacbda01f99af2ccd484c72572b39afdf9b0271774f02ec815`  
		Last Modified: Thu, 12 Jun 2025 11:29:17 GMT  
		Size: 60.4 KB (60364 bytes)  
		MIME: application/vnd.in-toto+json
