## `phpmyadmin:fpm`

```console
$ docker pull phpmyadmin@sha256:a022361fa7fe0cffe4574502303a3bc86d6544204cf551700130fbfe3b96f641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `phpmyadmin:fpm` - linux; amd64

```console
$ docker pull phpmyadmin@sha256:1538033ce99025c5e09093903dffb2fc2ab5787eb89c94e819d33a8c24b7f551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191248173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9101c236dac91d8d72d13b761a10e2f8bd48d19018fbad079d4866c55c46e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836b4fbe4b6fad94869056fc3b0fdea9bf52d3e553165f22e95a66003e800dc5`  
		Last Modified: Tue, 30 Sep 2025 00:05:13 GMT  
		Size: 12.3 MB (12309754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363c276d0dc2444bfa0f1f7419d0be936eeb687ccdcbca90611b294f60f9ee52`  
		Last Modified: Tue, 30 Sep 2025 00:05:12 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5623a61e9c2d6f1d8f9ba131f6c0b4ac9bacb08c9670db2f4d10d89bee9acc`  
		Last Modified: Tue, 30 Sep 2025 00:05:13 GMT  
		Size: 11.6 MB (11642764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5743de172d68f7ccff07d26761aafe54540d45cc8ba75f3532f2a8d6363a4213`  
		Last Modified: Tue, 30 Sep 2025 00:05:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdee73376b7e8f7faab42acd6f1f78c65ab56bcfc01b15a24c0b997d6dd6dc6`  
		Last Modified: Tue, 30 Sep 2025 00:05:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f602367faaea287d4b185e1790b0179a16981b94c4349f3ba1e5fb5d40b3a2c5`  
		Last Modified: Tue, 30 Sep 2025 00:05:13 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba33e986f5ac35fa069271ceae8a67bf4f5bd443c605803aad9f4a1feff186d`  
		Last Modified: Tue, 30 Sep 2025 00:05:12 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba717c6f9b48b694b0d1ef32baef0fb77bd330714478875b773e849e6dc3b57`  
		Last Modified: Tue, 30 Sep 2025 03:12:10 GMT  
		Size: 6.3 MB (6257421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03e8acdb1c01efb6fe11178f4c90a7100503aadbaeb5fc9c0fe3a7a6ebf025`  
		Last Modified: Tue, 30 Sep 2025 03:12:09 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2a02341dcccd25541852c0e0fe1a6cd522da96d69016a46c23579a314b57e7`  
		Last Modified: Tue, 30 Sep 2025 03:12:12 GMT  
		Size: 13.4 MB (13406048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e2b67e2e793f6b57dd67315601c51065ec656e7fd9aa8de3cc33a36d8ada20`  
		Last Modified: Tue, 30 Sep 2025 03:12:10 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d376b5b41bf6b6c03a85c0ad684a00a238d1963a94101c0226c318c9129f4e8`  
		Last Modified: Tue, 30 Sep 2025 03:12:11 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e4a78909b586e3d6ec38cd2187bb1c48ae226b44a9b085aa3ff88fdda1bd0f`  
		Last Modified: Tue, 30 Sep 2025 03:12:11 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:e16259021604bf5452153015593f61719893c9c5391181c5c22d1c8e5e51c805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 KB (44464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04efa02280cbdb8822c0caa67b61394881e52f229c1160b93bb8af5e2c3d03`

```dockerfile
```

-	Layers:
	-	`sha256:bd63e1736132ae3506bf15dcf1348f7fa8fa78872badc0224bace35840429433`  
		Last Modified: Wed, 01 Oct 2025 14:40:33 GMT  
		Size: 44.5 KB (44464 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; arm variant v5

```console
$ docker pull phpmyadmin@sha256:ccdac050f90f1ae1b4a7d485ac81948100b23032d25b430403614f125b00d6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164337547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da50d80d009374b5fd79d0f6101199ee1b934f4efa86bf2910c371bbae7e680`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc57522d9f42dbd24b5d080f4f8bdd9603c0632ecb16e24a2c07c125cacc8f9`  
		Last Modified: Mon, 29 Sep 2025 23:54:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6b796db92ec741e406f3c33411aef6a4296d3bb720b2da6dffd0fabae717c8`  
		Last Modified: Mon, 29 Sep 2025 23:54:06 GMT  
		Size: 94.9 MB (94874040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada408669de76a3c82ff5d6aff439ed152278eeb68dabc91360cd588956f1982`  
		Last Modified: Mon, 29 Sep 2025 23:54:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517434f3e84587f4cfe79aabe2ed71205fd4a82bf4fccaef84463d0fd2153e0e`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 12.3 MB (12307267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee30ac8b5ee4d46c0ed451c208d67832cdde09176c579091a730734c2789f81`  
		Last Modified: Mon, 29 Sep 2025 23:54:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fea52bb9c57eaffadf9cdc11cdcdb7d59a0fa97f4cf55f3495220f9984a2905`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 10.5 MB (10459973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b72db761d11478c5aa0b7500f03592d399de47f7886a655e6ffb13c8b2aaad`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aaef8a2cd0161bfd6f8449438c7148bc4acf328d027436def69955a7f88966`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51b4924d1cadf8f37665cc5b29240dd0d1ee19489cc53ec74dcec73b705ee0f`  
		Last Modified: Mon, 29 Sep 2025 23:54:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c5821dae8b50541865b3b7e298eeae62eac5934d7fd4c30d422adf4cbe7a1d`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d46fefbee27447baf086bfc1193b8a99281b483f5887f00f5b8e9454841349`  
		Last Modified: Tue, 30 Sep 2025 02:14:13 GMT  
		Size: 5.3 MB (5326495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48b37876da8b9be07c9cf3848f0448a39701b46921c73242b33fe2076202df2`  
		Last Modified: Tue, 30 Sep 2025 02:14:12 GMT  
		Size: 654.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5af6d7b965d5a5024633c82188754e36a3d5b57e7645bc901221a9f61ab0ce0`  
		Last Modified: Tue, 30 Sep 2025 02:14:13 GMT  
		Size: 13.4 MB (13406074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6c688b96400b4912284710cb24a7128760380f5acc0f9dea084ac99a706ca6`  
		Last Modified: Tue, 30 Sep 2025 02:14:12 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7407f84caa00e325030340e123818cd109e26416adaeb17f13db8ab19da281f`  
		Last Modified: Tue, 30 Sep 2025 02:14:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f00b87fa0ff1eaff828a6b9eaddb1f74ee72b73cc5b500aee74b4a105ae97c`  
		Last Modified: Tue, 30 Sep 2025 02:14:13 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:74ac79af06b408be4d22371f98b7e72e8166b43bdb8343b3c5c0210f9c5914c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608d48f2d590c52c1d49a8e40c389990aafafb8ed850a0ecac185a2da80f6224`

```dockerfile
```

-	Layers:
	-	`sha256:3eb9c3b6784e45455342dd665c2e1157d1e4dcfe8891174848031d2917691377`  
		Last Modified: Tue, 30 Sep 2025 08:40:35 GMT  
		Size: 44.6 KB (44563 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:9c896d3b3249f0c0b93c7ac97c07b69805b59d0ec2b513a2480e104bd1f93c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152950622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9461e5e917e0cea4804dbe6c9ca68d90612b2b49b377e471a8ac1ac50d0b850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124035b6df0178965919a1689b6d95bc60dad98b242a4f3d99f310ba260ae50`  
		Last Modified: Tue, 30 Sep 2025 00:12:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554f6fed754e85d4fe404bdb7da53a97c211fe10064fbff863dde76db978d257`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 86.2 MB (86245515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95ba12bcb10e5e7a752090f559e99e8a257b19757a067f5c0d5dd98124a34bd`  
		Last Modified: Tue, 30 Sep 2025 00:12:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca017d74a37798b8f1a4b86f65013b869aa88f753f5dffeebcac0b0789c968ce`  
		Last Modified: Tue, 30 Sep 2025 00:22:15 GMT  
		Size: 12.3 MB (12307360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87a8f00ae2cbcf51913be6f8d2f20dd68a931e63d9fccb1cb4264c34e412f90`  
		Last Modified: Tue, 30 Sep 2025 00:22:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb207eaeb3722ffd543575ceca5abb24b2aa1a072503bb5a325e6c05e0539d8e`  
		Last Modified: Tue, 30 Sep 2025 00:22:19 GMT  
		Size: 9.9 MB (9852690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77431726681b0a03300b77f2c8a4e49739b247ad236b46f686396351392522f3`  
		Last Modified: Tue, 30 Sep 2025 00:22:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445dfc1de0f670d9be3b304aa3e5c70f06ab59a82ad52e598d8979f5c7e554d8`  
		Last Modified: Tue, 30 Sep 2025 00:22:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058183c41d0d13c72e3a9738b0a08e74c9bff555db18b37b70385559a35d3fe6`  
		Last Modified: Tue, 30 Sep 2025 00:22:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e39b8eda62754af0b1c087ee74d4ebc4aae71d4585923e972f732dc3f2ea21`  
		Last Modified: Tue, 30 Sep 2025 00:22:19 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84711a35ea4dc84a17e9429b891ccb5d818720feee0074feafec7159a2f84770`  
		Last Modified: Tue, 30 Sep 2025 02:36:06 GMT  
		Size: 4.9 MB (4908715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f0ca638a11025de2313baea2508dbb034e5b087dfcd23de436316792962cce`  
		Last Modified: Tue, 30 Sep 2025 02:36:05 GMT  
		Size: 653.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66aded5d828c29506395aeb4e937622d2f96243efab5eab8dbe31fe26c75e97`  
		Last Modified: Tue, 30 Sep 2025 02:36:10 GMT  
		Size: 13.4 MB (13406048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190b2d4d1fbb88a3ef25c5160cd1cc51fcfc9e5efbe11eb0c8853f57400c7847`  
		Last Modified: Tue, 30 Sep 2025 02:36:06 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42620fb4ce262d025c9ea11ba1ac3dca437e1a6de5a09c38de2af08341fa050`  
		Last Modified: Tue, 30 Sep 2025 02:36:06 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f56ac3cfe7616b04091a060550b8d9523019bf5c873763cf08be2b313ddb06`  
		Last Modified: Tue, 30 Sep 2025 02:36:06 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:0eef3d8dc94c9390924e5a70f3ca353f41888fdaa06d5bf4d8233bc927f22137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aade6b306cc63ffd7ecd26a4c81fb048c8587447cd3028d077e05076835f131c`

```dockerfile
```

-	Layers:
	-	`sha256:44108168e1857dd48eeea229c815e65991bf4d12ef01f01f66ad7e219524509c`  
		Last Modified: Wed, 01 Oct 2025 20:41:13 GMT  
		Size: 44.6 KB (44555 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:313eedf04448ee0e5a50b474d453502987e3828ef29f1ce3eceac965b400589f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184086702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503cb44caa50031d803a1223053e02f4d746548b67761c8a218b36033d5f22ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325e87446101a86960da1588163447c1198447a48bd44fcb5efa2062c2514e9`  
		Last Modified: Mon, 29 Sep 2025 23:53:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8ef5442630c413a5c9992ae040ca50d34b1e2524044804f3b885d7bd35033a`  
		Last Modified: Mon, 29 Sep 2025 23:53:40 GMT  
		Size: 110.2 MB (110163046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b4297d20872e106efa28d4f39ee99f6afec32ca7426170a75d0fc5b4a3b0e8`  
		Last Modified: Mon, 29 Sep 2025 23:53:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613fc4af0d4566696818f46db921a0fed09733c81c3df824409a9690aa23b93f`  
		Last Modified: Tue, 30 Sep 2025 00:08:16 GMT  
		Size: 12.3 MB (12309278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52230fca13a2a00f5008b8f871031252a330fece902b06c59e0bee075d74a83b`  
		Last Modified: Tue, 30 Sep 2025 00:08:16 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125912ed0a4a89618b9fe308020b8d9ba9a247c186ce424ef7521d39e2d34743`  
		Last Modified: Tue, 30 Sep 2025 00:08:17 GMT  
		Size: 11.7 MB (11683008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bae357a77230ef10a0304bb33e5505b8c724295bd4b491cba244e40b0470553`  
		Last Modified: Tue, 30 Sep 2025 00:08:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c6debf1aea0f45ac9ce715a94446bf60602a4f020a1b2146eb84f11ac18592`  
		Last Modified: Tue, 30 Sep 2025 00:08:16 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af082b4939de2e0a0ea0981e4750ca5168932220bd26c6ee6527c157202284`  
		Last Modified: Tue, 30 Sep 2025 00:08:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b265996b67f72b182e0408dff9c5ffcd2fd872ecc46a0e8ea0657887aa0b1f`  
		Last Modified: Tue, 30 Sep 2025 00:08:17 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7904327a0a80caa796f6843dd9af17ff86daad58b95a7973f7596b1ffb625d9`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 6.4 MB (6366968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d356967917dfe9fa431bd6a2c228bd405c02ec4bf24720b1b04664f42a97430`  
		Last Modified: Tue, 30 Sep 2025 00:59:30 GMT  
		Size: 655.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9a7749e09c638ae7fbb8999c14608b96c675e3c1e9157146aacffe32a4da8f`  
		Last Modified: Tue, 30 Sep 2025 00:59:32 GMT  
		Size: 13.4 MB (13406013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4486bdb819adba80e69d1517d0e37b66838e475493079961a1987f35b8096b`  
		Last Modified: Tue, 30 Sep 2025 00:59:30 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29011b978a781a32d748a9da5d79540c5d9321c15df7b2f5666709a106057dc0`  
		Last Modified: Tue, 30 Sep 2025 00:59:31 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9b6d0dc65b2dcd8f4512d7ff5f460299386329534f3a2cdbfa6acbc897a07b`  
		Last Modified: Tue, 30 Sep 2025 00:59:31 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:cf2e3b175fc7ddce2908c92a76bb692ff394d7ebdee2a27e4e8dedfc3285ca31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e28105630f513d54a16053b9201af2a391937d2e6993161046b660a3762f190`

```dockerfile
```

-	Layers:
	-	`sha256:0086f8c2dc1dd4eb2112fd0666e751699cff002599a9ac22d60b64ca1b1b024f`  
		Last Modified: Wed, 01 Oct 2025 20:41:16 GMT  
		Size: 44.6 KB (44598 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; 386

```console
$ docker pull phpmyadmin@sha256:6b52c095f2718520e72cf8361131b3d30e64870d871e4521dc2e1bd004f5322f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e75c8c75e3dc7867c27bdd35ec78388e5ce0ca4beac9f0a8f5089f99bdd4137`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41bdd8c83e35e4f0fca94acf5c17dfef47a147161024a9cb52c35bd689d181`  
		Last Modified: Tue, 30 Sep 2025 00:17:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d485f10ce08ba68dc6849cac58c522826b879da4a662e1faf536a9ecd5e9999`  
		Last Modified: Tue, 30 Sep 2025 00:48:19 GMT  
		Size: 116.1 MB (116138258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b7eb309dfc29f46ead78bb7d3980867d1d365827a97ba1833f82b4459c1d12`  
		Last Modified: Tue, 30 Sep 2025 00:48:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c79c4a9f95f1e9c1b04d9a9916cadbc56193123ab3a0640944a59d1b00ddaf`  
		Last Modified: Tue, 30 Sep 2025 00:48:12 GMT  
		Size: 12.3 MB (12308696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d105c2fc7aaf995a6763bf9ad8e47b003c8d8d9185c515e08946a6043f95790`  
		Last Modified: Tue, 30 Sep 2025 00:17:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a05169265ae65149838d7ccb4f0215c0e2ebc8d74cacbea89fa33f534a218`  
		Last Modified: Tue, 30 Sep 2025 00:48:12 GMT  
		Size: 11.9 MB (11869535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd86275c754538c037a25f26aeb6a5ad553a0025d1c693410838f634a72f17e`  
		Last Modified: Tue, 30 Sep 2025 00:17:55 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770737fe82154c7917959111ca4e7fc405c05fe47653e4845bae5044069ba11c`  
		Last Modified: Tue, 30 Sep 2025 00:17:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94773e2716b065c7e95ff6d2b19394c3fed6c2a36ad00f36b93a4b61b71ccaf`  
		Last Modified: Tue, 30 Sep 2025 00:18:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db20975e33f57329bed64bc23aacbc97bb94c35ef489a1b4ca8b3e7199c67619`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da856b9066afbfbdc88f39d7e88ca79db7787dd36a80e86ffa4e21e1fc6acb2f`  
		Last Modified: Tue, 30 Sep 2025 00:49:33 GMT  
		Size: 6.5 MB (6493383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc1eb4044c8aa9d76cfebb81de8dae72e35e5b7531b2818b294d4b9e0ce895e`  
		Last Modified: Tue, 30 Sep 2025 00:49:32 GMT  
		Size: 655.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e22571d526eab0894e14f0b64ac8e12fac750d990e25b34f77c2a86e2fb5d0`  
		Last Modified: Tue, 30 Sep 2025 00:49:33 GMT  
		Size: 13.4 MB (13406070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f33198fed61a78a7270e9419441e8b4faf243160284cff6864924ed7854b408`  
		Last Modified: Tue, 30 Sep 2025 00:49:33 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8991116bf88e2a475a3aa2f0e4a78002b310132fc2ba1ad33c83ba421ed7b8b8`  
		Last Modified: Tue, 30 Sep 2025 00:49:33 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea917d557966ef7bfd14077162cb5d5a992028fbe3d91c9d8d84a723b005d22`  
		Last Modified: Tue, 30 Sep 2025 00:49:33 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:6448094ad988a60ca8341453e28626440eb76ed8f21edd88330df75cc5b3e165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662f15149118e5680486680c45d3effa3c92f86922b53409e6340251b96f39aa`

```dockerfile
```

-	Layers:
	-	`sha256:08b5540ed528bc1e1ad90b0c1a9514e2a653ec855b0584f71bc9bc24a5402127`  
		Last Modified: Wed, 01 Oct 2025 17:40:43 GMT  
		Size: 44.4 KB (44428 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:626a3d87351a221c33e1aca927bb3ec9ccf4f40048e57fcbcdaf5db8a8e28327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187790663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb851be2f3ae88572aab19fc0fa8a9b6f47424a3d3ae2ba2f8b20efceae567f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d8f05f06dc824d87111df6e83c98b44d4b30120744017674fa115b47c2dbe6`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75015a3f4b08f0357c989a4c27950c8a6de956a67874e0df0e8876482f1c6285`  
		Last Modified: Tue, 30 Sep 2025 07:16:10 GMT  
		Size: 109.6 MB (109597733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbf93152fe00ebb17d96bb0b9dce5763e9ee0f645695274ef06bcf783421bd`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ebf56ee6def1f8a9ce586662586247278a634ea42d854693bad65d3ecef0ad`  
		Last Modified: Tue, 30 Sep 2025 08:11:18 GMT  
		Size: 12.3 MB (12308804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f3f2867628fe61df9c76460ba20abb9982386de131cd4d0296824d81a954c8`  
		Last Modified: Tue, 30 Sep 2025 08:11:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06c3bc5b23592add08e40e7180107be7f0b91212fa994a880e89fe6b54b1b7`  
		Last Modified: Wed, 01 Oct 2025 10:31:42 GMT  
		Size: 12.2 MB (12188742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bed157d051b120223e35d481cb53751bdc4a8979b3bbdc659747fd5b0515bcf`  
		Last Modified: Tue, 30 Sep 2025 09:09:42 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638fca3e5179dfd89ae5155af51768ea5416bdbece5f72d07ce68e058871935c`  
		Last Modified: Tue, 30 Sep 2025 09:09:43 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d1116caf2c688a1983bc5ef0e0589dd4d168c7ef963012436eaa5b9688230`  
		Last Modified: Tue, 30 Sep 2025 09:09:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620abf8c2db61dff464fc04b90d7632ca55610d06d6c5557a5c16018e27dd235`  
		Last Modified: Tue, 30 Sep 2025 09:09:43 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b3b1656d088dfbee4687d44be083554837304016e225d77b8139f988aae1a1`  
		Last Modified: Tue, 30 Sep 2025 18:18:13 GMT  
		Size: 6.7 MB (6673321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee44c3ce26c4b9aceae09796f7712e38b76e6091e9b4ad95ddaa47393c2a18`  
		Last Modified: Tue, 30 Sep 2025 18:18:13 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7680dff174eea235a9d91997c7ebbc3f8fef9c4dabe0048f15f2c13b391a0f`  
		Last Modified: Tue, 30 Sep 2025 18:18:14 GMT  
		Size: 13.4 MB (13406050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c7ab3679491232ef7a0ae5a64854b3cb438020224ccf94be2feafb4581edb`  
		Last Modified: Tue, 30 Sep 2025 18:18:13 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14914bd48c240be6daac741ed14dbd217115d2365016f4b872619a9a00a6d9`  
		Last Modified: Tue, 30 Sep 2025 18:18:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe5816ff84df124a4336ceb515a79de119496cdc98a8aeabba8f0008189384e`  
		Last Modified: Tue, 30 Sep 2025 18:18:14 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:df2f184cf4c4e48f4d7fcb8e8e6c26a51511f5480d8c48ddb99bd3cb228bba95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 KB (44512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd974e0ca1809063c7c896076dcfe866c1c0c8307f6b3dc9f24980b0f92429ba`

```dockerfile
```

-	Layers:
	-	`sha256:84806b166c77cf2e8d57e932e71bd7b50208780c3ec4d7fb02df5cf116cf5629`  
		Last Modified: Wed, 01 Oct 2025 20:41:21 GMT  
		Size: 44.5 KB (44512 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; riscv64

```console
$ docker pull phpmyadmin@sha256:3a69fb119cb4bdb97eadb3e30ce6792ede30625e87fbaace79e05942e2a256b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217314096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d812d4ef637388ddcc09b790efa7fbbe8f6e827c68952e02c1bb6a69ea8edbeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10c25f1d43bda19fe1addca79e55bd60680b6683c485853db1be0763dd7e2`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03438fb8247e71c15afcd0508b678af32b8a41a4cd64dda788e8224b32557902`  
		Last Modified: Tue, 30 Sep 2025 15:10:17 GMT  
		Size: 146.6 MB (146579364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df117f051d654fe662d0af341155be2d955517920079566410cd20daddb0a237`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f042d2aa047700b5536dc4e530084843b7039007f0d28cb25306b5c867dae50e`  
		Last Modified: Tue, 30 Sep 2025 16:33:25 GMT  
		Size: 12.3 MB (12323328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54516e295cb33a7ff2ac5761875afc8159f2277df518d40b5c010b27dfccb52`  
		Last Modified: Tue, 30 Sep 2025 16:33:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31b7bb6a2c4a74308c31500c9022411a1088b301e11bc7d096e3967f7b618b`  
		Last Modified: Tue, 30 Sep 2025 18:11:00 GMT  
		Size: 11.0 MB (11009352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c197fd30742810b94cacc4500dcb2ff2b213504adc8c5a908cc212346d98ca`  
		Last Modified: Tue, 30 Sep 2025 18:10:59 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfa31021c1eb7e094c28ecb5ff78d8a9c8625d0ed83af9b14328c33ec3b2aa7`  
		Last Modified: Tue, 30 Sep 2025 18:10:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b34c6e889ed93052460c5c97668f7c42adbc4b1ae58edb988a9056fd63020f`  
		Last Modified: Tue, 30 Sep 2025 18:10:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea65a7492edbd55053d0da8fd46171e55e08cc04ca29885678febbd73cff1fb3`  
		Last Modified: Tue, 30 Sep 2025 18:10:59 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a76f7b88f47bf08663e3dbad560a6a37086a5d2dcbd6edb9e66f8877226843c`  
		Last Modified: Sat, 04 Oct 2025 16:13:27 GMT  
		Size: 5.7 MB (5702912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2652b7d96dc0d02ec63dfb19d6e3061ce769c385316e44f46d8201f3892f8fb6`  
		Last Modified: Sat, 04 Oct 2025 16:13:26 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c5f723586f1d963e830d81a8f517c6f22dacf4749ba97a0585721e5449a152`  
		Last Modified: Sat, 04 Oct 2025 16:13:27 GMT  
		Size: 13.4 MB (13406076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a180633b5a471948bb8289ebdb07b25943323b768a6f25479dc10056e20595a`  
		Last Modified: Sat, 04 Oct 2025 16:13:26 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1f88d48845ca8cae433f78f9b8d227b5e906789bc3a10d804874668b66af1`  
		Last Modified: Sat, 04 Oct 2025 16:13:26 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0504a6f193964b152c6127dbdce55c24dfbca1f185dc4dcea1c9632aa241b0`  
		Last Modified: Sat, 04 Oct 2025 16:13:26 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:e041aba963856ba4041908cab7e242a30ac049cc5467a94ac9db4fe052d08528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 KB (44512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f85b60096e9e687047c71f6dd3d24dd5c231d84a1908fc46370bf4b5dd16ac`

```dockerfile
```

-	Layers:
	-	`sha256:db30f89de7b28b9d8c812c30df2acca3b19ecac009787e6f875c305b35e4f354`  
		Last Modified: Sat, 04 Oct 2025 17:40:37 GMT  
		Size: 44.5 KB (44512 bytes)  
		MIME: application/vnd.in-toto+json

### `phpmyadmin:fpm` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:03fc2b0f1a3cc343495eae090ba2eeb05bed4062f090e05d42a522809bb4334d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165532034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5cb475f25cd11d078fbb816f2960381ac892b70424691bfc08ca9d167a7f8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 01 Feb 2025 20:29:24 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 01 Feb 2025 20:29:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_VERSION=8.2.29
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2025 20:29:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 01 Feb 2025 20:29:24 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         savedAptMark="$(apt-mark showmanual)";         apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;); # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
ENV PMA_SSL_DIR=/etc/phpmyadmin/ssl
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MAX_EXECUTION_TIME=600
# Sat, 01 Feb 2025 20:29:24 GMT
ENV MEMORY_LIMIT=512M
# Sat, 01 Feb 2025 20:29:24 GMT
ENV UPLOAD_LIMIT=2048K
# Sat, 01 Feb 2025 20:29:24 GMT
ENV TZ=UTC
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SESSION_SAVE_PATH=/sessions
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     mkdir $SESSION_SAVE_PATH;     mkdir -p $PMA_SSL_DIR;     chmod 1777 $SESSION_SAVE_PATH;     chmod 755 $PMA_SSL_DIR;     chown www-data:www-data /etc/phpmyadmin;     chown www-data:www-data $PMA_SSL_DIR;     chown www-data:www-data $SESSION_SAVE_PATH;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER www-data:www-data
# Sat, 01 Feb 2025 20:29:24 GMT
ENV VERSION=5.2.2
# Sat, 01 Feb 2025 20:29:24 GMT
ENV SHA256=f881819a3b11e653b0212afaf0cc105db85c767715cb3f5852670f7fc36c9669
# Sat, 01 Feb 2025 20:29:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.2/phpMyAdmin-5.2.2-all-languages.tar.xz
# Sat, 01 Feb 2025 20:29:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.2 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Sat, 01 Feb 2025 20:29:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;     find /var/www/html -type d -exec chmod 555 {} \;;     find /var/www/html -type f -exec chmod 444 {} \;;     chmod 1777 /var/www/html/tmp; # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data config.inc.php /etc/phpmyadmin/config.inc.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY --chown=www-data:www-data helpers.php /etc/phpmyadmin/helpers.php # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Sat, 01 Feb 2025 20:29:24 GMT
USER root
# Sat, 01 Feb 2025 20:29:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Feb 2025 20:29:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9ee178226f7ea0f482af09b7dc3ba5fca7c07de96e60ad828b1737709e6b19`  
		Last Modified: Tue, 30 Sep 2025 06:40:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b8c6f589e7cb0b9aff90a6df6a7cccfae60ed23d9fc4328b15d0c44aa0266e`  
		Last Modified: Tue, 30 Sep 2025 06:40:25 GMT  
		Size: 92.6 MB (92564454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674ff7c7e8a7de8708af6056d40b56dffeb3ae246f618226bf482e0f207ff014`  
		Last Modified: Tue, 30 Sep 2025 06:40:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3da8af74e14c8d9e99e7d276f5bda28b0257ab9fa5bb8399d7599a042796e`  
		Last Modified: Wed, 01 Oct 2025 09:31:05 GMT  
		Size: 12.3 MB (12308125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79831d9dea0209ac248dae2fe789601fa96a7c02f738d19c7c3ed0231dbfea5e`  
		Last Modified: Tue, 30 Sep 2025 08:25:37 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ab515039d52cc215e9089f6c85fa0f38fd8f84ac43704a2ef9b3855ef510e2`  
		Last Modified: Tue, 30 Sep 2025 07:44:05 GMT  
		Size: 11.5 MB (11531377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4d1f69de61e700d3554081f84d336f90300354f51a3eefe9f550979708f120`  
		Last Modified: Tue, 30 Sep 2025 07:44:02 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e10a3bccfb23ddb2fad8db2bf1591f106c6deada823a631cec6e41701e949e`  
		Last Modified: Tue, 30 Sep 2025 07:44:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcdfcc48d92cb1ac57592be3454831447d60c7ebf2f5c18fbd916be0122e7d0`  
		Last Modified: Tue, 30 Sep 2025 07:44:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da00ca5ce4e96cf69e8d5ea8c6f85b89f2b9ca923de37e659a060d00ce5679d`  
		Last Modified: Tue, 30 Sep 2025 07:44:02 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e22b5be2ef05ca485c826b753e12ad1b28440f7338dcca54d497148a0b7af3`  
		Last Modified: Tue, 30 Sep 2025 15:24:19 GMT  
		Size: 5.9 MB (5867234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c37f2795d2aee721f0dfacfe02d6d4560af4e98f0ecb909766d97e34ddff86`  
		Last Modified: Tue, 30 Sep 2025 15:24:14 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4fad10eb1905087cf5d766b581440d252e0e208f910b5b5a73ff9485ae4a77`  
		Last Modified: Tue, 30 Sep 2025 15:24:15 GMT  
		Size: 13.4 MB (13406076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfbf29f69854f93ea17a49849642b52cf74e1bf237d139a4b22918e32cf37ba`  
		Last Modified: Tue, 30 Sep 2025 15:24:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f720d69a79c818761d99446e09d8609b90f0d7fa9d34f48abdc1fe1d46be3500`  
		Last Modified: Tue, 30 Sep 2025 15:24:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abf17ad4ee549fc702cd1dce4ad764ce75ca99e7ef706ad7191c78485d1e30b`  
		Last Modified: Tue, 30 Sep 2025 15:24:15 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `phpmyadmin:fpm` - unknown; unknown

```console
$ docker pull phpmyadmin@sha256:addb42f3043da0b6bc7c684f5c592b0f7b71b61b099781a70047ff646e8d4393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 KB (44457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9c32310ff82a13c30152b0b0ff716979261d629ba2587572e051da60bb35df`

```dockerfile
```

-	Layers:
	-	`sha256:3b4911d61e4f8f2f2425f2bdc2ce66eeb1cd43c71a1d841d5b58aaa9d9fc18f6`  
		Last Modified: Wed, 01 Oct 2025 20:41:26 GMT  
		Size: 44.5 KB (44457 bytes)  
		MIME: application/vnd.in-toto+json
