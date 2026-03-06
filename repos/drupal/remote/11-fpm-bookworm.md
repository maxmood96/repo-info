## `drupal:11-fpm-bookworm`

```console
$ docker pull drupal@sha256:d082ad63285902de400d1ab17eb9d7d9bc55c3a5bc2958393af7a1dc3ad53cb9
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
$ docker pull drupal@sha256:a771c54ae48678f1ef8302722fd957a379b7d4643b75dc5d26b13779e66cf353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199665247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2863f18f0329b156b5c623c602f5314cb1c778ab62c69c59d2e110e24495aa`
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
# Fri, 06 Mar 2026 18:33:30 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:33:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:33:30 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:33:30 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:33:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:33:30 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:33:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:33:49 GMT
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
	-	`sha256:8d413a10d516b65c8cf0875020065cf7833c2f0d47b8168bb98e946308bd8401`  
		Last Modified: Fri, 06 Mar 2026 18:34:05 GMT  
		Size: 1.6 MB (1551771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55bfb8d21a2475cbea2e0cc8b1709e98899c3852f04b27b0016e391a4445d8`  
		Last Modified: Fri, 06 Mar 2026 18:34:04 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195827c5301f4ac9a61c418a76167ed6ed50879be95eae02d2e94493caed2e3`  
		Last Modified: Fri, 06 Mar 2026 18:34:04 GMT  
		Size: 777.5 KB (777541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70049c38f5846efa253a9178ad07a9f0f35226a1a7ac054b7256780bbe210664`  
		Last Modified: Fri, 06 Mar 2026 18:33:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbaa8e60f1585da23c6e4bf25e2edc2c05c0b484b5b602499a5ee12cae2742e`  
		Last Modified: Fri, 06 Mar 2026 18:34:05 GMT  
		Size: 21.3 MB (21335870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:7241b8a5ca1f962a17df7f8e964cd90c3e0962a9d3c0c9c5e837c2fa9a23bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c4576b2d99293c8c061847452045cd911202e248b886f81fa4ff62c770b6d9`

```dockerfile
```

-	Layers:
	-	`sha256:d8671d8008e6ac889112e20d3601fccbca2ee70cb1660a1d8077a6b736475648`  
		Last Modified: Fri, 06 Mar 2026 18:34:04 GMT  
		Size: 6.5 MB (6524309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8fd7c9da50cbc81a814888af90feb2f5993a9859f75025887438b1b7f9aab1`  
		Last Modified: Fri, 06 Mar 2026 18:34:04 GMT  
		Size: 35.7 KB (35745 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:56dfc910b580965cb24065451a68655a5c124ed14fd07696cd7534df909e819e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164179191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d6bc0a65746b452d3679f7c83eab631b85349537f090b20f7d51d84d678614`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:09:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:10:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:10:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:17:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:19:45 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:19:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:19:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:19:45 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:56:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:56:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:56:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:56:09 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:56:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:56:09 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:56:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:56:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa3a48ce9256276c0109937eac189d16b2e2fbe93cf8606c77fe3f68cee49e`  
		Last Modified: Tue, 24 Feb 2026 19:13:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c3a5bda1260cd7b803040797b179cb927b05cb6bf53b89c51916a7d2b40d7b`  
		Last Modified: Tue, 24 Feb 2026 19:13:34 GMT  
		Size: 76.2 MB (76154208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c1c70025682dd699f2927e2abc746e3cce6ca1011d72bb215e0f7a2c4f581b`  
		Last Modified: Tue, 24 Feb 2026 19:13:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45520559e6b45276e7cd778a2c59a6fc7bc3ad84f840926c5ebedd55cd7368`  
		Last Modified: Tue, 24 Feb 2026 19:19:56 GMT  
		Size: 13.8 MB (13782913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc695f09632732a89e2b3e31b4e3f9a5eca10e375ae5a777721b95bdacf3f2b2`  
		Last Modified: Tue, 24 Feb 2026 19:19:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221eb911113bc102b0e02ff82cb8ef71cc5e97333e85217c5aa90ba2b591530b`  
		Last Modified: Tue, 24 Feb 2026 19:19:56 GMT  
		Size: 26.9 MB (26902509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230947232c814f7959438efe8326355aa5776ce3ca6b6a07ef5c470f264459e`  
		Last Modified: Tue, 24 Feb 2026 19:19:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d88c31b58352cbfdd0149261d4b30bdc08b257afe9e990b19f902b931dd35e`  
		Last Modified: Tue, 24 Feb 2026 19:19:56 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62272553c6e79ca47c8db20f7b03d10d36b994a319ba1a959d558ebfacba75e6`  
		Last Modified: Tue, 24 Feb 2026 19:19:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c831e8dccb4fb25f73d523a2573e0ad05416e0b83cb1055b45cc7900e8b3f47`  
		Last Modified: Tue, 24 Feb 2026 19:19:57 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e43ee1d97ac84358d132cbe78ad029b7d1af216cdfd01aad8bbd9dc163906b9`  
		Last Modified: Fri, 06 Mar 2026 18:56:33 GMT  
		Size: 1.3 MB (1272013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff53b588b84cd7d7cae36b90e476ab473c422c00d95fdbd47b0cc5c0e2b19fd`  
		Last Modified: Fri, 06 Mar 2026 18:56:33 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8a538dc7ef2028e3be4160238c592c05ec9052a8cc9ce7c94f967ed55408b5`  
		Last Modified: Fri, 06 Mar 2026 18:56:33 GMT  
		Size: 777.5 KB (777549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e897da24923dbfb014397d5f8bcc1f01c535f019c8ca7049a25dacc8b43775f`  
		Last Modified: Fri, 06 Mar 2026 18:56:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9ea21618062212735abc0c1fe2ceb2e7adcd16539d6797fa7a9a3ada42cab4`  
		Last Modified: Fri, 06 Mar 2026 18:56:35 GMT  
		Size: 21.3 MB (21334975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f5b6bf545f9dffbd441e063141cf05cdaed97213a0cbb16d038775810bfecd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058106133a17250cce5d3b9b062f2ac29e4e48be28852c1919d8fc7cf0571d13`

```dockerfile
```

-	Layers:
	-	`sha256:72bbcf4f06d3ba87cb5dbf590697d1184f0a863420ff483716cf723692d880c7`  
		Last Modified: Fri, 06 Mar 2026 18:56:33 GMT  
		Size: 6.3 MB (6337629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81c761602c38da4791c57527083f8c6768fcc0a47dffd72d4e2d451ffdf30be`  
		Last Modified: Fri, 06 Mar 2026 18:56:33 GMT  
		Size: 35.9 KB (35899 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:12eb2957826a97032028816303bcdd1cc746a3f16542e4eba1334b953b8fa1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192985675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175f8f0586ca574aa4909f27c433a92b2d161d08d7633fa44b9bb227d4a7b36c`
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
# Fri, 06 Mar 2026 18:59:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:59:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:59:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:59:27 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:59:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:59:27 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 19:00:00 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 19:00:00 GMT
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
	-	`sha256:5b7a5add28d4d57de69e18b76a76329cb6ba76f2b8679adf9c5423681977c1d2`  
		Last Modified: Fri, 06 Mar 2026 19:00:18 GMT  
		Size: 1.5 MB (1539885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2addf0fad13039f7b0ce8229a0ec89a817fc763c445b2a3f34f6dd969c80e62e`  
		Last Modified: Fri, 06 Mar 2026 19:00:19 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732fca4f64300dae1a343b681b718792c6d4e62fe51352756dcf335cb6da540a`  
		Last Modified: Fri, 06 Mar 2026 19:00:18 GMT  
		Size: 777.5 KB (777550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa8e3b34539bc9d2b0d3e7be6fed287425ba1def95bcda901ca8177f53e236`  
		Last Modified: Fri, 06 Mar 2026 19:00:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fbc75dc6cf03401fb12f5f1aa2636480b6232334e33a6a362956f8e131c179`  
		Last Modified: Fri, 06 Mar 2026 19:00:21 GMT  
		Size: 21.3 MB (21334671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2e90e1d846ad3d1f0c011d995d5621938343af06fc5429132ae184d775cef606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6588701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb36aab4837e8371ae73e04615c2ad3edbc192ba814966e2dd4cca12fe4c0e`

```dockerfile
```

-	Layers:
	-	`sha256:e895c73f8e2e2d3f963d94f6316a10d4a145aa321472412b541de7a8c2e4b9f9`  
		Last Modified: Fri, 06 Mar 2026 19:00:21 GMT  
		Size: 6.6 MB (6552754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06d7c052b2a40f6e31045f6edb0d7185c2b656f68c3334361875171714f862d2`  
		Last Modified: Fri, 06 Mar 2026 19:00:18 GMT  
		Size: 35.9 KB (35947 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:e667152ee045e0a567c0296a7640377b004a99605878e3ba889b6c3c042bf776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198496728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1b633934538815497d1ccfa8b6ad0b5d55c4c68ed651fd9ac5305a21424005`
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
# Fri, 06 Mar 2026 18:35:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:35:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:35:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:35:13 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:35:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:35:13 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:35:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:35:20 GMT
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
	-	`sha256:f7dc1fde8bdca672ae7a6a05ff6fbe362c8833e3e2e485915531da25c45a77fd`  
		Last Modified: Fri, 06 Mar 2026 18:35:36 GMT  
		Size: 1.6 MB (1624094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df78f20eb617600021891d12d40ae4ab5cc7b5704b4223bd13a85ebc3a49e774`  
		Last Modified: Fri, 06 Mar 2026 18:35:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f67b85ca130d68e1f8b59b8cbeee942893423996f587b2e9e85113e214270`  
		Last Modified: Fri, 06 Mar 2026 18:35:36 GMT  
		Size: 777.5 KB (777547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0c73a13a82f0ee18680a03843a0a559df8aebc74757ae08f902a178d28415a`  
		Last Modified: Fri, 06 Mar 2026 18:35:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e14c1e610bdb90155e913b54b132c47310f5d738ebb65576464fdeeb27e658`  
		Last Modified: Fri, 06 Mar 2026 18:35:38 GMT  
		Size: 21.3 MB (21335863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:7d2462b68a5a882a431968f6f3bd5580f9e99b8202f19b263bd5f118bb6625ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989a11363bddfb3a01ac062f413ebe432ec58c06ea4312a5be03ba3bf25e26c7`

```dockerfile
```

-	Layers:
	-	`sha256:f0c3ee8142cb474b57860384d9175cf09f8a5e4db189567167d21bac7473d464`  
		Last Modified: Fri, 06 Mar 2026 18:35:36 GMT  
		Size: 6.5 MB (6504069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59e54d2a5d291e360d531125f34ab43a0c3fccc826da7bf4c567ad84623c117`  
		Last Modified: Fri, 06 Mar 2026 18:35:36 GMT  
		Size: 35.7 KB (35682 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:396e5352dbb6db2eea6bc38de69782c41e065201c3d54e4593f42b678a4e89e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203760860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8207b5bdb1c2881e1a2903cdf01a35db88825544781a86dc001a955a8452cd2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:45:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:45:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:45:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:45:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:45:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:45:53 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:45:53 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:45:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:45:53 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 20:08:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:08:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 20:17:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:17:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 20:17:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 20:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 20:17:43 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 20:17:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 20:17:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 20:17:44 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 20:17:44 GMT
CMD ["php-fpm"]
# Thu, 05 Mar 2026 18:56:01 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 18:56:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 18:56:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:56:02 GMT
ENV DRUPAL_VERSION=11.3.5
# Thu, 05 Mar 2026 18:56:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Mar 2026 18:56:02 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 19:14:07 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 19:14:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8909961eea48ef1b6874fc78e0a2a67be659ef1f501c141db727def77188f`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee44b9ad8e875a3f516f25b3e3c40a3cd26acc45cc0e89783e3044adfc8d3f`  
		Last Modified: Tue, 24 Feb 2026 19:51:33 GMT  
		Size: 103.3 MB (103330209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1044ec1105edb234be52095b7e7657e4bc5695912aac59d3a42b6d4609d990`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19367d3f784a05f1cfaad1782f501be3d78bf5ee81e1ae2d8946dee71549149`  
		Last Modified: Tue, 24 Feb 2026 20:13:18 GMT  
		Size: 13.8 MB (13784700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255fe82a69731a5ba9891f71acee93982521b06f68f218b08da97cfd7cd6bd2f`  
		Last Modified: Tue, 24 Feb 2026 20:13:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f3d08785a9cd9099617c124939f0c43a07cf2b90b6022833a1a006735df86b`  
		Last Modified: Tue, 24 Feb 2026 20:18:11 GMT  
		Size: 30.7 MB (30686678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf450c78c6650713d3af99e1bd58e0b3a5e0c859447d7f82ec8633367e19873`  
		Last Modified: Tue, 24 Feb 2026 20:18:10 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aaf03b48f0c0b5331742fbe4f8c4d9a7169264950fcce9dedb49147c38154e`  
		Last Modified: Tue, 24 Feb 2026 20:18:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d19091646b8f37a3c52f21608d6513a1a2da13e16b9e70c85d1ddf801b6c760`  
		Last Modified: Tue, 24 Feb 2026 20:18:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7b85ed1d8e7abaafafa758d486a33981cfbfa8496544f7680a178a8865a2d8`  
		Last Modified: Tue, 24 Feb 2026 20:18:11 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a324828ac744281280e2e6daf61c50af33985813e0a10634028df7db49a1dc21`  
		Last Modified: Thu, 05 Mar 2026 18:57:09 GMT  
		Size: 1.8 MB (1753916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0962592cc358599a04c1851b09a307f35a00a1710badc559f4a683d5bfc443e7`  
		Last Modified: Thu, 05 Mar 2026 18:57:09 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8cd6544f74516ef6e0991e09c8b922603846edcbd9de4d3f0a94dadb93806e`  
		Last Modified: Thu, 05 Mar 2026 18:57:09 GMT  
		Size: 777.5 KB (777547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71195fba3f2af5c864f33434ee2930aab10965f91a6fec0c8c190457ba47dbba`  
		Last Modified: Thu, 05 Mar 2026 18:57:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b050b69b31bdef5be1cf6243f71feada625fa7882cf055c410a040acab6b77b6`  
		Last Modified: Fri, 06 Mar 2026 19:14:44 GMT  
		Size: 21.3 MB (21335865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:0bacb9b87426d29040780c951ad009115d05a980e35db2f6d39a47de2299eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6536884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a92b4a9ccc26f26e014d196131196faae6ca34615c5b83a2141271dbfb3874`

```dockerfile
```

-	Layers:
	-	`sha256:81d6d86e55b6417f47e2188a8c60b58339c7ca4d27e38ab65fc42cd514f49f26`  
		Last Modified: Fri, 06 Mar 2026 19:14:43 GMT  
		Size: 6.5 MB (6501057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66079ef9eaaad7f4211dea5f0a6260ef2c1a27ffce9d15526f4e68a57f2af883`  
		Last Modified: Fri, 06 Mar 2026 19:14:43 GMT  
		Size: 35.8 KB (35827 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:f7e0b2c85ac9a7fbf9b195ff312b9accc805701373f8b8c59d12d1d9f2b74b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173673343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eb4c572fe13e34fdffd6ca24ececd3157a5e2d613ab4b280987fbe912d6fe2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:15:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:16:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:16:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:16:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:16:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:16:37 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:16:37 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:16:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:16:37 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:28:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:28:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:37:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:37:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:37:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:37:34 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:37:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:37:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:37:36 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:37:36 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:55:33 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:55:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:55:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:55:33 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:55:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:55:33 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:55:39 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:55:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888ddcf8d56ba1585c0143811b54347b2dea83987a0f877602efadae824c515e`  
		Last Modified: Tue, 24 Feb 2026 19:22:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6599039cf0d4c26d33b25e5f55305201c9c5442bd67befd50e9a7af182db7d2`  
		Last Modified: Tue, 24 Feb 2026 19:22:17 GMT  
		Size: 80.8 MB (80828334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b0b090ea9d1e02f423938fd0ed61df3e83aca17b89627a2331d38b8486ff18`  
		Last Modified: Tue, 24 Feb 2026 19:22:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92bd91b85c84eb41e066eb92718c63a636a02194a89f7e21064f993afe03c5`  
		Last Modified: Tue, 24 Feb 2026 19:32:42 GMT  
		Size: 13.8 MB (13783729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dbd5dd7b5b1bb84827ac8a16f205c2cd1ae17e5fd9de931d9b1c577253bb65`  
		Last Modified: Tue, 24 Feb 2026 19:32:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f30628a147595c74e90ba351e2c15969420183cb55a20fb88af6c7171905260`  
		Last Modified: Tue, 24 Feb 2026 19:38:00 GMT  
		Size: 28.6 MB (28580157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c34d7d8cde94e8ce00ac5906e5724e85451b5a3ad3e657bd088f2fba7904dba`  
		Last Modified: Tue, 24 Feb 2026 19:38:00 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62c3e23a2db151fc121abdc719a74f6613bcf266e2658676ee7f10eb1ab9da8`  
		Last Modified: Tue, 24 Feb 2026 19:38:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02c227546f2ae584711356c10a780316e748db1dd1e74535292ad0cbd53102c`  
		Last Modified: Tue, 24 Feb 2026 19:38:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2a9d616b138c96ae6617c71cdb64faada8d282d222c87535ff6dd1085d0b0`  
		Last Modified: Tue, 24 Feb 2026 19:38:01 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5ecd9a8dc524e84b5f101dacf65ec5d6097c7a0c80139d67877e046594ca05`  
		Last Modified: Fri, 06 Mar 2026 18:56:02 GMT  
		Size: 1.5 MB (1462608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f17d8fe477f991a7730a210939edb4f7dd3a563b6f97056dcd128f25e93358`  
		Last Modified: Fri, 06 Mar 2026 18:56:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b074c0a25db6504e4263cf60f5db74c0852aa37e7534f60161f40fbd410d1`  
		Last Modified: Fri, 06 Mar 2026 18:56:02 GMT  
		Size: 777.5 KB (777546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3de4195e8e7af02985fa5381d89b936909a572e92b525e0ee28d6fa52e36b38`  
		Last Modified: Fri, 06 Mar 2026 18:56:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb28e15b59efeee4455ab3dc79e67fcd5b094e67441601da850ad918889f03e1`  
		Last Modified: Fri, 06 Mar 2026 18:56:03 GMT  
		Size: 21.3 MB (21335817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:3240f813902edc4485ba2cd18d9bdd1ba00fb01633a5e137673730686627bff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60c545cd6faf1f6491cfceb6abf306f31f426126bf9c7740dda546bc49a88c7`

```dockerfile
```

-	Layers:
	-	`sha256:c0e1b83ab9c0179291df319979bb01500bca7574d252596ca3b476023deb5b75`  
		Last Modified: Fri, 06 Mar 2026 18:56:02 GMT  
		Size: 6.4 MB (6361527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f3de02c288c44609023ea5bd5f510e6e8df6dbd09eb24122aa4cf9e9beb27a`  
		Last Modified: Fri, 06 Mar 2026 18:56:02 GMT  
		Size: 35.7 KB (35736 bytes)  
		MIME: application/vnd.in-toto+json
