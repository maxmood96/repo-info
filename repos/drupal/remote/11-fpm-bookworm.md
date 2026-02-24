## `drupal:11-fpm-bookworm`

```console
$ docker pull drupal@sha256:13044e99e48c3d31e1e0125b8f7b1ecfdae20b2ed7f2a0a88a865fd3036c8a1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `drupal:11-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:5c1af4d4603e1aabd9b76e18b46f0d2f166b959949e131d4d22e10b860dc655c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199638400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1c81f2e52509433fde99f5aa9a794ea177f8faf514b211e6879b6d15936363`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:08:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:09:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:09:12 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:11:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:11:45 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:11:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:11:45 GMT
CMD ["php-fpm"]
# Tue, 24 Feb 2026 20:05:03 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:05:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:05:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:05:03 GMT
ENV DRUPAL_VERSION=11.3.3
# Tue, 24 Feb 2026 20:05:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Feb 2026 20:05:03 GMT
WORKDIR /opt/drupal
# Tue, 24 Feb 2026 20:05:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 24 Feb 2026 20:05:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d996c80452b57f7326526308fde734c55eaacdd57d09f19a99325c100ca689`  
		Last Modified: Tue, 24 Feb 2026 19:12:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51205855d1d26569b08d3b5ae81e1b70660a87264812e808f68653971c59373`  
		Last Modified: Tue, 24 Feb 2026 19:12:08 GMT  
		Size: 104.3 MB (104335914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907c240b70e5e94cef1092e1f3e2138cea8e28815eeb0fbd98d3722e814fddaf`  
		Last Modified: Tue, 24 Feb 2026 19:12:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f48a42ece0eaeafc2d35cafdf2cec482e3b4899e0452bc12c08ea0943c89584`  
		Last Modified: Tue, 24 Feb 2026 19:12:06 GMT  
		Size: 13.8 MB (13785307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b8370ee487988b9e115ad8e28c559c6aae4b4ccc98c3436e3b476b819250a`  
		Last Modified: Tue, 24 Feb 2026 19:12:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129eb6b1f73200cb416dab8b90482c921233baa72903833ca59ef770d49b6e12`  
		Last Modified: Tue, 24 Feb 2026 19:12:08 GMT  
		Size: 29.6 MB (29628949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e1410afd18628a13b559d0324defc934e3454e6a70544921dccb74f2ed5d03`  
		Last Modified: Tue, 24 Feb 2026 19:12:07 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abca81b471270bac3fb6e8d3db0112b9db3026773e151f1f79ea98d51c7d2e00`  
		Last Modified: Tue, 24 Feb 2026 19:12:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea054bf834dcc2796d220a58e25d0ccf5218fe19c43ca8e2fde849ea76d4bf4`  
		Last Modified: Tue, 24 Feb 2026 19:12:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b28c334997a89ecab5010151a8154160a3d8f3ab6c60166cc5cd4f08dc1ba1`  
		Last Modified: Tue, 24 Feb 2026 19:12:09 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1182b67c15d60ff8c48bc5d2e290b176b5644d9a150f25d453ee5d3ebc087b8c`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 1.6 MB (1551815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5772172741adb6b96ebeac8aa2d4667aab7dd1e75c09af60280bdc90ade53`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0fd271b25b357563f92f17fbf143105fdaa9050f612f24dca61f472022e7ef`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 777.5 KB (777535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e6d2082e66726cb9b91757e72fc564e586ffb983e9374e2a2c1832fdea1e59`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baf4d309e5ac755cbcde0f4ce573e590570406051c921d7d7f3e0f6fc3560bc`  
		Last Modified: Tue, 24 Feb 2026 20:05:28 GMT  
		Size: 21.3 MB (21308987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:d48db6247733a29cebb8b84d63f40eab308aa62a931ce565a27592ab0cc1f9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3225e433f478409f54ee8df21f83d9d5bcdb7c078a8a9e50d62e3529f035fec1`

```dockerfile
```

-	Layers:
	-	`sha256:e8801a776d68e29c7ab5ad8b7d4426ef989411795027bf8511b54278054a9bc9`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 6.5 MB (6524309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a23aefed4d30dde0152a99892eeaa85c25127bdd027e8898837e09ab4f2fd71`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 35.7 KB (35745 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f522034c589714d6aa7ddfd1ca51763f301400ba684e6783073fa36aedf12165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164146459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ec0cb6a7885f880c6802a518c0d3910c3d1b7a6733512bdf46819890ab860b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Fri, 13 Feb 2026 18:35:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:35:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:35:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:35:41 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:35:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:35:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:38:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:38:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:38:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:38:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:38:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:38:19 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:38:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:38:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:38:19 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:38:19 GMT
CMD ["php-fpm"]
# Fri, 13 Feb 2026 20:14:57 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 20:14:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Feb 2026 20:14:57 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:14:57 GMT
ENV DRUPAL_VERSION=11.3.3
# Fri, 13 Feb 2026 20:14:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 13 Feb 2026 20:14:57 GMT
WORKDIR /opt/drupal
# Fri, 13 Feb 2026 20:15:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 13 Feb 2026 20:15:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd66f5b1628f05f4251a3a964ac79ee52ff478ba1fa269fe1ca546be4ac24bd`  
		Last Modified: Fri, 13 Feb 2026 18:38:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26cb554619f94fdac93e4647bfbb4d7a0e343b2be5291305b0df7796f7bcd3e`  
		Last Modified: Fri, 13 Feb 2026 18:38:36 GMT  
		Size: 76.2 MB (76154772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db947a7ae5fa3c686bbd7d4ef4b7f12a843b2b5b3dca8a8b387ffcff480452`  
		Last Modified: Fri, 13 Feb 2026 18:38:34 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d728ca3a7710c7fb2ef2e7d3ced453f6116c8576cd350fcd775c919ffa5106`  
		Last Modified: Fri, 13 Feb 2026 18:38:35 GMT  
		Size: 13.8 MB (13782893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c51f85c62482c6e93c29ccdd0104d2eac65ff8dd633ffc96010e6f05ca98d2`  
		Last Modified: Fri, 13 Feb 2026 18:38:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d42d1ddecd98d17f230370f7a5a779eddfb136d88277407410cdab086467059`  
		Last Modified: Fri, 13 Feb 2026 18:38:36 GMT  
		Size: 26.9 MB (26902492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ef5e74fe126706cd33c6dd0d5377838441e3fbc2a8faa3fd16f6cda4388c15`  
		Last Modified: Fri, 13 Feb 2026 18:38:36 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afe51eff00f4742ce0ed08a61cc096f6a10856767e66e9cadf6460253f6cc28`  
		Last Modified: Fri, 13 Feb 2026 18:38:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0850ecefe1616df4c38e727f8cc57daf9a4362807bd48b1168424c7577469bb`  
		Last Modified: Fri, 13 Feb 2026 18:38:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9170815e102675c112fe224d213826679fd38f07851a09ebaa909bbeb71f235`  
		Last Modified: Fri, 13 Feb 2026 18:38:37 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8504b7cc7cd34ed26289ba89a88b7b1bd7fd1109e0ce8a349f6483be2f29b5ae`  
		Last Modified: Fri, 13 Feb 2026 20:15:23 GMT  
		Size: 1.3 MB (1271937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8444662ef998e881a186d571fa3d4b3345486b973866d132f7bc3690a4d42f04`  
		Last Modified: Fri, 13 Feb 2026 20:15:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f003d2804d2a8cb8c766a94056b8a21e6e201a1a8a420e3e66509239e1d6860`  
		Last Modified: Fri, 13 Feb 2026 20:15:23 GMT  
		Size: 777.5 KB (777544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4535b087af18a2bddd8392612ea958ac94ade5f359900dec296833d0d6e4e1`  
		Last Modified: Fri, 13 Feb 2026 20:15:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a123ebf96bc71beb41662b585295ae2b2f05b670e7c1777b7c9ab32f47e99`  
		Last Modified: Fri, 13 Feb 2026 20:15:25 GMT  
		Size: 21.3 MB (21309106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bf2ae5e695b2eb984c2d4aef27efea434235c66a0a285bf50df524a4c7e12db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531a0b01ce1634082cee5ffddab2ed6af4e1cedbfd1901c33932b9ce38f0009d`

```dockerfile
```

-	Layers:
	-	`sha256:cd46323ed2080b86cdd8581ae391854d8075c2e42378c3fe2573b7feed73226a`  
		Last Modified: Fri, 13 Feb 2026 20:15:23 GMT  
		Size: 6.3 MB (6337629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37225cdfb1cdc55e39e66ed382f27825bf8821de6907143af11e6aa7e5c7a04`  
		Last Modified: Fri, 13 Feb 2026 20:15:23 GMT  
		Size: 35.9 KB (35897 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:491842760fcee02b4c42d053ab189ec10a8e2cf8a2153f3e92f9b8e83cc9df41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192960175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bc65ab129f510e9165bdf1e2a6def0fa548e0346126ad3bbfaf8592007a2ce`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:09:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:09:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:13:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:13:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:15:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:15:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:15:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:15:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:15:52 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:15:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:15:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:15:52 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:15:52 GMT
CMD ["php-fpm"]
# Tue, 24 Feb 2026 20:15:53 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:15:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:15:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:15:54 GMT
ENV DRUPAL_VERSION=11.3.3
# Tue, 24 Feb 2026 20:15:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Feb 2026 20:15:54 GMT
WORKDIR /opt/drupal
# Tue, 24 Feb 2026 20:16:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 24 Feb 2026 20:16:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f598ce440794ce45f250a2a4439aba7e3cf33c3cae52ad5948ab94d07edeec`  
		Last Modified: Tue, 24 Feb 2026 19:12:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cd883132144ea2041c27026a5c90f203aad51b234cb962da79f2a4441c7ad7`  
		Last Modified: Tue, 24 Feb 2026 19:12:46 GMT  
		Size: 98.2 MB (98168272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4e4ccfb995c3d6c23e576fabf0da5415bc28301583f78ee15b4e4a7edd9d62`  
		Last Modified: Tue, 24 Feb 2026 19:12:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9ae54f7f45e067f60fd0b1866e23042b632c3571d8d5a6aabff319c5d76834`  
		Last Modified: Tue, 24 Feb 2026 19:16:04 GMT  
		Size: 13.8 MB (13785095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d82e1cea8dda365a9a049191873987671491ff29fd8e2307be858ea3d16fc`  
		Last Modified: Tue, 24 Feb 2026 19:16:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd967612a28e09cb583ad93a0e80e5a5758a5dce15d89f6fdd12216a66980b5`  
		Last Modified: Tue, 24 Feb 2026 19:16:05 GMT  
		Size: 29.3 MB (29250492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d5bf4e35080ace60e82916edda422559a907339da987b6b19814513ae5d00d`  
		Last Modified: Tue, 24 Feb 2026 19:16:04 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94433fdc986aea8de46b20d165875680612715b1b5267acf510a4c089d26c05f`  
		Last Modified: Tue, 24 Feb 2026 19:16:05 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa3d895b8af3fef7333803f56c95ff4c155538dd98a4e9578d4abbad0e35c04`  
		Last Modified: Tue, 24 Feb 2026 19:16:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147ab7b2b1e3e5e2bca28dea1fb61e3cba8b2fd962098ea1cb754d37d6c15aa5`  
		Last Modified: Tue, 24 Feb 2026 19:16:06 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f44b1e461ae0b8327b58cacc998c7a4f06035bc0b077c63e3493a72f33467c`  
		Last Modified: Tue, 24 Feb 2026 20:16:19 GMT  
		Size: 1.5 MB (1539772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b905f5ec8ffa55f515184f18dd276929e2376631cc25461534a995a685b059`  
		Last Modified: Tue, 24 Feb 2026 20:16:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d73eb1189060ff2170273138314182eb184e29c88c0509cbbb839b960c7af7`  
		Last Modified: Tue, 24 Feb 2026 20:16:19 GMT  
		Size: 777.5 KB (777545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026710a9fd954b3abfad13a5f4deddba633bf88c552da887eb697c946f5d44eb`  
		Last Modified: Tue, 24 Feb 2026 20:16:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e1baee9c2fec03d6c6ad6f4464f6d75f08647317ac62be59442abbf7419183`  
		Last Modified: Tue, 24 Feb 2026 20:16:21 GMT  
		Size: 21.3 MB (21309290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:dbde179996760d73abe676221fc0680eec9f7f464527606ec9b531d9658a8632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6588701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a05b9ebb0d4e0c61f7d906ab55ffd19b2d860f296999c77728581a1c0b966f`

```dockerfile
```

-	Layers:
	-	`sha256:003253d4882bc603619f660c27c957945f712f027c603fd2e83f4be5ccc88678`  
		Last Modified: Tue, 24 Feb 2026 20:16:19 GMT  
		Size: 6.6 MB (6552754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e5b9d78b3e463a639ec51b7ee3369b04fb7de669aab8be7e8cf192d67298eb`  
		Last Modified: Tue, 24 Feb 2026 20:16:19 GMT  
		Size: 35.9 KB (35947 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:e970a0a3852bcb06173cf3d76000377c9054b004b0a4a4d199af539212d0df22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198469845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca4b38262556e5f6e9d6dbc86c2cef3f5f3c77402e6a246b8f9ddd20287b40`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:01:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:01:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:01:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:05:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:08:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:08:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:08:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:08:29 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:08:29 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:08:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:08:29 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:08:29 GMT
CMD ["php-fpm"]
# Tue, 24 Feb 2026 19:58:07 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:58:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 19:58:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:58:07 GMT
ENV DRUPAL_VERSION=11.3.3
# Tue, 24 Feb 2026 19:58:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Feb 2026 19:58:07 GMT
WORKDIR /opt/drupal
# Tue, 24 Feb 2026 19:58:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 24 Feb 2026 19:58:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1bada0816798a481d5694551065743798710a54795b5077bf911c43668de6f`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729aa62bcfdba517f3577f64c720c12e133726cec6a6a0164821de7dd86c765d`  
		Last Modified: Tue, 24 Feb 2026 19:05:18 GMT  
		Size: 101.5 MB (101526922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f318ec1fe3c296306ee9a5d7bf4364177c3fe97a1c8b15af6256088d2f5170`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f880ad7776d81aff6b08dfe1d58aef7246887d73c7cb6ad7f9a5dfba5289923`  
		Last Modified: Tue, 24 Feb 2026 19:08:41 GMT  
		Size: 13.8 MB (13784355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f11dbc5d73c5c0a6b250519582b5464744195e1b376887f1cf032cc0e0085b`  
		Last Modified: Tue, 24 Feb 2026 19:08:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91286c32f0b78c8c73df25c0d0cbd44778802da4958237c7a676086f27bed0f3`  
		Last Modified: Tue, 24 Feb 2026 19:08:41 GMT  
		Size: 30.2 MB (30212623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ea756252002cc09d1f55149681814f677114ff37bea9c291a3d308cf9979c9`  
		Last Modified: Tue, 24 Feb 2026 19:08:40 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dfddadb6c25d4d3acdaccca877c1af40d3ade32498171327ccf58052f31df`  
		Last Modified: Tue, 24 Feb 2026 19:08:41 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ed7193d48216d2ce0a3e25643732dd26418ff3a0e35907adbf39fa0082d7a1`  
		Last Modified: Tue, 24 Feb 2026 19:08:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94312c42309b2faad9faa48aa5e312513d7564ebba219d8d4e0aac2291a98182`  
		Last Modified: Tue, 24 Feb 2026 19:08:42 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95810b80bf0079c7c8a3d6f638313b3067f68b5b914bce8a0364416a57620a56`  
		Last Modified: Tue, 24 Feb 2026 19:58:31 GMT  
		Size: 1.6 MB (1624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcafa6235f78160e536f61e448b4f0b5fd18f666684e3f9b961e262be51a7c1`  
		Last Modified: Tue, 24 Feb 2026 19:58:30 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8174fe492587b8e6ab1bbfba673d46e59a68852608d154820921e2303abe0a`  
		Last Modified: Tue, 24 Feb 2026 19:58:31 GMT  
		Size: 777.5 KB (777539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24dbb6b11c3ac482c2014dfc7f98e98bc97813b81a4f0af9b77d59b71060b5`  
		Last Modified: Tue, 24 Feb 2026 19:58:31 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f454495128c627fa99021e8637b4d0d93272c6e08c6d7af5532a0cd61a7427ca`  
		Last Modified: Tue, 24 Feb 2026 19:58:32 GMT  
		Size: 21.3 MB (21309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:179b6d2da4a346c145e47d6f1072863961573d32df76dba5d2f66ce901a2ee42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c298cfa559da722de5c9f852745de3450e96e7645a8acc60bbd9cdd98adba4f`

```dockerfile
```

-	Layers:
	-	`sha256:08fae21a745e036e74d13179e9ecac6cdc403c8db28011820b3c51b71d289b92`  
		Last Modified: Tue, 24 Feb 2026 19:58:31 GMT  
		Size: 6.5 MB (6504069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166c3c8745f42d92862f1a5f6fffb75f84f1d77dbdcabb459353cb814abdd41a`  
		Last Modified: Tue, 24 Feb 2026 19:58:30 GMT  
		Size: 35.7 KB (35682 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:5b45bfa420722a158a1b1125c38e8a3e611ce9f5417eae2479fd787f3a1d4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203723000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be0b56f9dbbf198206dd05229bc18bb81b22ad11dea2529ed23a1da1d1c19e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:59:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 03:00:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 03:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:00:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 03:00:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 03:00:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 03:00:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 03:00:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 03:00:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 03 Feb 2026 03:00:14 GMT
ENV PHP_VERSION=8.4.18
# Tue, 03 Feb 2026 03:00:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 03 Feb 2026 03:00:14 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 19:40:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 19:40:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:51:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:51:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:51:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 19:51:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:51:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:51:59 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:52:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 19:52:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 19:52:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 19:52:00 GMT
CMD ["php-fpm"]
# Fri, 13 Feb 2026 21:21:37 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 21:21:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Feb 2026 21:21:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 21:21:38 GMT
ENV DRUPAL_VERSION=11.3.3
# Fri, 13 Feb 2026 21:21:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 13 Feb 2026 21:21:38 GMT
WORKDIR /opt/drupal
# Fri, 13 Feb 2026 21:21:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 13 Feb 2026 21:21:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ebb178bbcfc434182101d46fcca90f1bb2e7c11472e7dd531d21ef01dd49b2`  
		Last Modified: Tue, 03 Feb 2026 03:06:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec72ea046e890ed42e9f1d71aaf8ac39d92b94990eb041deef93a5332602e97b`  
		Last Modified: Tue, 03 Feb 2026 03:06:04 GMT  
		Size: 103.3 MB (103328614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd369ae85816b683b8af912f44c2e8a46bff69473116b4ea2cab4ec1d56b3c6`  
		Last Modified: Tue, 03 Feb 2026 03:06:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e671eeeb5a443b35eee5a75e39df7acf4012e0507753f39cf6507e26fb961aa`  
		Last Modified: Fri, 13 Feb 2026 19:46:35 GMT  
		Size: 13.8 MB (13784671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a087bd309062ace081303d7854efa1da56b60f72aef3358492cf6a03b9215`  
		Last Modified: Fri, 13 Feb 2026 19:46:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1520661ba5685e66dc968e59427536863f8a5bad7d1214fcb8c0309c690ac4a`  
		Last Modified: Fri, 13 Feb 2026 19:52:30 GMT  
		Size: 30.7 MB (30686665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040c4e011eb25497734a9e08943e1e7bc15d2975427f5b0ca135fbc7564dec88`  
		Last Modified: Fri, 13 Feb 2026 19:52:29 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259cfd0024c6772abcb8ced0d03528d8024da5307dc0a4166b282670230f7b7`  
		Last Modified: Fri, 13 Feb 2026 19:52:29 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bebef9ae52ddc2db3cad3af360553246ffd8026a0c7a54d6223d843c6efc54`  
		Last Modified: Fri, 13 Feb 2026 19:52:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80d3250033f085ab4eb4a580e1694352503a8189b3dcac9f6a2fc900f7078c`  
		Last Modified: Fri, 13 Feb 2026 19:52:30 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588e57cd93d1681a9d0df3066d09f22cbf63b47e34f2fd86a1589af2c3af1ce3`  
		Last Modified: Fri, 13 Feb 2026 21:22:46 GMT  
		Size: 1.8 MB (1753995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99e6baa5110d9f41a1f2a40d969bd598467b528e881645b1c24cd57ab16198`  
		Last Modified: Fri, 13 Feb 2026 21:22:46 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9962c558c98ea3137d052d59c14ebe032da8a35c028b0626f24a4a023edcb2fd`  
		Last Modified: Fri, 13 Feb 2026 21:22:46 GMT  
		Size: 777.5 KB (777542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7875737b09b9daa0f109ee6b8f3131c66d5a75f5541ca759da266298a4f79580`  
		Last Modified: Fri, 13 Feb 2026 21:22:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd3756683660379e1930b579008ee9b59ed508cbbc67a512451f13fa2dc55`  
		Last Modified: Fri, 13 Feb 2026 21:22:48 GMT  
		Size: 21.3 MB (21309174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b4b7c648e7e3053f0d3f35967c2165a31a1472f094714ad3b8792fe60c92e9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6536883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c6210b7eeac2a2df6e4d0be0eabafbee4fe95b749017c6a6f2a1edaececd33`

```dockerfile
```

-	Layers:
	-	`sha256:01878f3debf2e4dcc51698ed4d1c76c35a0c6076be9e944d9b4a0a8d6fe738a7`  
		Last Modified: Fri, 13 Feb 2026 21:22:46 GMT  
		Size: 6.5 MB (6501057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042d1f4a8ca11c777a19e7bcbfcd4667c1ed53a186befc000fc483c783afd54e`  
		Last Modified: Fri, 13 Feb 2026 21:22:46 GMT  
		Size: 35.8 KB (35826 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:071eff6425a587a6fad3454530f0cb91c8b9b8a51b563a1a55154fb2f73be709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.6 MB (173637019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e483783f4e73d7e081885c46abd37c212f09d0cc5c6f16050124cb553ece13f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:30:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:30:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:30:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:30:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:30:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:30:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:30:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:30:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:30:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 03 Feb 2026 02:30:17 GMT
ENV PHP_VERSION=8.4.18
# Tue, 03 Feb 2026 02:30:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 03 Feb 2026 02:30:17 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 19:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 19:05:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:10:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:10:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:10:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 19:10:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:10:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:10:37 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:10:37 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 19:10:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 19:10:37 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 19:10:37 GMT
CMD ["php-fpm"]
# Fri, 13 Feb 2026 20:15:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 20:15:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Feb 2026 20:15:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:15:10 GMT
ENV DRUPAL_VERSION=11.3.3
# Fri, 13 Feb 2026 20:15:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 13 Feb 2026 20:15:10 GMT
WORKDIR /opt/drupal
# Fri, 13 Feb 2026 20:15:21 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 13 Feb 2026 20:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9655ee6b195be2bfd3d61426ce4a2830906c8dfadd7e8c4124c8b58809dbfc2f`  
		Last Modified: Tue, 03 Feb 2026 02:33:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37231254b5d72887c0519ee4b1571cc4226576086afeb5bf52d7fcd998f461b`  
		Last Modified: Tue, 03 Feb 2026 02:33:33 GMT  
		Size: 80.8 MB (80826766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79851f442186981d5b09f3f1d669553b5d06fc32279c921226a6fa5901286864`  
		Last Modified: Tue, 03 Feb 2026 02:33:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b065f8a57b9336ca75425e908475a4e4552cad37594bfdfc70be75d6d8142233`  
		Last Modified: Fri, 13 Feb 2026 19:10:58 GMT  
		Size: 13.8 MB (13783491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b271352ec3b56712411e675de015ed7aa401e814492925332e4276dc7192d`  
		Last Modified: Fri, 13 Feb 2026 19:10:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc57485440222f4a65b270222767f34356da2d43c7c89a6b4ed310ac8488b05`  
		Last Modified: Fri, 13 Feb 2026 19:10:58 GMT  
		Size: 28.6 MB (28579968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8880f553cccc540a76e1a210528be2bb3ac534a88e4f3caa7051a58b70116a5d`  
		Last Modified: Fri, 13 Feb 2026 19:10:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3061d1416828e9e3a06e73621f3186df902477f28aca60ac63e81075751c3de3`  
		Last Modified: Fri, 13 Feb 2026 19:10:58 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b1b1f3513d2d7c47a95e749289000675d686f779cc15445bc6a59a2491ad17`  
		Last Modified: Fri, 13 Feb 2026 19:10:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61b5194c2edfd92278ef8b370bf8268b36ae5d8efe07c380ff02e734e34587d`  
		Last Modified: Fri, 13 Feb 2026 19:10:59 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82ecd39d11e68c14906b18d7f892db8a31e161d4997c838a37f322351f82e38`  
		Last Modified: Fri, 13 Feb 2026 20:15:45 GMT  
		Size: 1.5 MB (1462377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051c74998519b59f0f1183a45c6ad4d1cf5d6c66a1bc74d8ce27618ea0c08728`  
		Last Modified: Fri, 13 Feb 2026 20:15:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c218b5eeb0b643d08cc8d75fdc300f9d3b315e6372566122e0a3bb6f4b6c42`  
		Last Modified: Fri, 13 Feb 2026 20:15:45 GMT  
		Size: 777.5 KB (777539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e1493c5694fd344dd3556efec61da96c2a0117522174f408afb6a55ae3e3f`  
		Last Modified: Fri, 13 Feb 2026 20:15:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca43d348619792d1bc88da122da4c7405a19ca4c1c2070a456c8d93b40c9ddbf`  
		Last Modified: Fri, 13 Feb 2026 20:15:47 GMT  
		Size: 21.3 MB (21308861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:348fa76ca2074bb7702eedbc6f3dd49b57872e36615933fe0539b5342664a404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98eb30c0eac95792afbf8ffb06a91341ab9acda7b79798337aeb3eb8f60a3a8e`

```dockerfile
```

-	Layers:
	-	`sha256:1cd277bba277738704f47f5b313303a81ed61d68166a5626a88435f3ff403d46`  
		Last Modified: Fri, 13 Feb 2026 20:15:45 GMT  
		Size: 6.4 MB (6361527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92d52e3e30dd5cd0348ac80727bb121177afd4f807d9f0d50cb85ed69f5fe82`  
		Last Modified: Fri, 13 Feb 2026 20:15:45 GMT  
		Size: 35.7 KB (35739 bytes)  
		MIME: application/vnd.in-toto+json
