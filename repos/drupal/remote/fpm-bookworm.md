## `drupal:fpm-bookworm`

```console
$ docker pull drupal@sha256:f36f340f636cfb93a5463a33779fc5095711433c71ad564a5e4f87ca7cdf2f25
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

### `drupal:fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:47da2850a0fa1e943d109fb8e6a4c16c601a8dbf91f1de2ce87361efc03da8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199443284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3287a41babd81f5a9b7d066d75228500480f130cb8d74e30db67503e2d79e46c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c25be817a835befbaadae87f2657fb370d8f40e4de6e20a0ce7fe0f95622d8`  
		Last Modified: Tue, 12 Aug 2025 22:31:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b6ab636ad18b9656bf3f6c19aaa9c667b779892eeb2c6609297e3d28621ce`  
		Last Modified: Tue, 12 Aug 2025 22:32:26 GMT  
		Size: 104.3 MB (104333251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7993c6bc3e951174f25d2629444ab1d9ca97b3fd7f8410f197871f2acdfcc3a`  
		Last Modified: Tue, 12 Aug 2025 22:31:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c2c07b11ef6a1cc199233ee1a3930cca4dd61252206520c728b726d244609d`  
		Last Modified: Tue, 12 Aug 2025 22:32:20 GMT  
		Size: 13.7 MB (13742135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e9486f8efeb9bc8b7331d26c56b0a2316dee37ab12b79f1e83903add8e6625`  
		Last Modified: Tue, 12 Aug 2025 22:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3831f8545efd4c32130dff6fe79b1bfd3fc90b51ace4346d5446ec664df7d`  
		Last Modified: Tue, 12 Aug 2025 22:32:22 GMT  
		Size: 30.3 MB (30290909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262b8435b959036f85a57829ab279a5393e0aae490a8f3a428f923a9c228f3d`  
		Last Modified: Tue, 12 Aug 2025 22:32:16 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b296f48da085ecee9ac0f7ac1d4431d01afe73cd2526827fabbf1e5624b5a734`  
		Last Modified: Tue, 12 Aug 2025 22:32:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2894e5dd7b5b222244b1722f530eed6fc1e92cfa8cee8bc4e9896a6eee67782b`  
		Last Modified: Tue, 12 Aug 2025 22:32:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10a1d2f410cea7f6bfaf5948f36e1d6b6680a6529c6416a26c94cd3d9df8cfb`  
		Last Modified: Tue, 12 Aug 2025 22:32:17 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec0622ee17d9183b7908f4c1e382979d85c7636540661c8f49e9d03e9706f2a`  
		Last Modified: Wed, 13 Aug 2025 22:46:14 GMT  
		Size: 1.6 MB (1550003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb47c81d9db427ac2f92da5b798d42e71432360f04b10228a26baae06c5383`  
		Last Modified: Wed, 13 Aug 2025 22:46:06 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72168cfac1baac03634fe6bc7f2c93d8e41205aa6b010daa116fcce7d96fd9aa`  
		Last Modified: Wed, 13 Aug 2025 22:46:06 GMT  
		Size: 748.7 KB (748716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197cad4bdeb7792e3ca36a81bdc531bbda039e3b6f388eb1bfe62732c3444945`  
		Last Modified: Wed, 13 Aug 2025 22:46:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41900eddb97e0af7de1fe362754e6b384354b3b6feaa223c7abbba11368fa864`  
		Last Modified: Thu, 14 Aug 2025 07:54:23 GMT  
		Size: 20.5 MB (20534474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:890d37dba6ed4fed097743e28fc3b4f90e572ede76dc2f5d0b12d8c0602615bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf87d00edb04647387e359e4c47b8062b5b01ea8dce0c90db654ff1e19919b6`

```dockerfile
```

-	Layers:
	-	`sha256:4b19434c2e3c5479e323e70c31c857af4ace1338c29d1f5c2d4b8fae6079859f`  
		Last Modified: Wed, 13 Aug 2025 23:03:32 GMT  
		Size: 6.5 MB (6524214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a945b306d63c94f8f3d36862a5b9db8ccb7740d845807efad7dc4b16ab954d65`  
		Last Modified: Wed, 13 Aug 2025 23:03:33 GMT  
		Size: 35.9 KB (35943 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:149e6753020576e819f43b0567af24f28078536f3bcc03309b64d3d9e5ebf2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163991906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92247351171d9b1d49cfda2c3046898d12d7801897ba722eac79b120935fa93`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd152e133ed3c4f7b6111971ebb032fa5347cab0e4ed3c3923003220f8ec4`  
		Last Modified: Tue, 12 Aug 2025 22:02:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48d5562d819ed1d81511a866ab9cfa69e1c7f0351806797ebf63ebbb4bacc7c`  
		Last Modified: Tue, 12 Aug 2025 22:02:48 GMT  
		Size: 76.2 MB (76153041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4000aa6f8df46ea73922bba283db07ef24d97efded72dc7d1e798c0d32e96`  
		Last Modified: Tue, 12 Aug 2025 22:02:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd5494683719c0fe1148ef916e62135afc24c7aa79c3dddc3c8a5609a8fc38`  
		Last Modified: Wed, 13 Aug 2025 07:05:49 GMT  
		Size: 13.7 MB (13740403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329cc10c9af3b5e918a5c4e0b28d886c6274dd1f71e17fe3747994eb217854bb`  
		Last Modified: Wed, 13 Aug 2025 04:03:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d04b8adba6e6775ededba7a83287d97bfe256d9066d7cf143965da2aed1455`  
		Last Modified: Wed, 13 Aug 2025 08:28:44 GMT  
		Size: 27.6 MB (27591624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38febe1e7c037dfd9d8b7e5fbbbe54a707ff12345f8dcf479a02154ae0ba6a9f`  
		Last Modified: Wed, 13 Aug 2025 04:03:28 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e5aafe3eb4d3113b81da06306ac0d95d2e0d3bbfe9a7f8f19ae01a7f615f8e`  
		Last Modified: Wed, 13 Aug 2025 03:55:34 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b070a35343ba385862c75b0e607f69c0186760c000a95191ad84201ff5d54e`  
		Last Modified: Wed, 13 Aug 2025 03:55:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e57639d39b93f74e6f4648a998b8c76c8629dfd6b5dd70cebfec1fb8c6b9f52`  
		Last Modified: Wed, 13 Aug 2025 03:55:35 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62a680f039b982ef3547e1b93b28bb213144daae526e70c754abf3c97fed81d`  
		Last Modified: Thu, 14 Aug 2025 03:54:11 GMT  
		Size: 1.3 MB (1271017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad6fed1de568eff2354611a7c4f23ecc813a6c21120a8ffef7f6970871b2d31`  
		Last Modified: Thu, 14 Aug 2025 03:54:12 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c21b58ce368d642c2517fcc47363bc11e2b80965b1185576a9c68586707db4`  
		Last Modified: Thu, 14 Aug 2025 03:54:12 GMT  
		Size: 748.7 KB (748718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7323444aeccf1e49040f2b536030eb7a8c1435ff9341dfb33f1714949fd63e87`  
		Last Modified: Thu, 14 Aug 2025 03:54:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7508ccc0acb1d50189dae378d68c1982d64d10c7ae129539ea4bc69ad4861d1`  
		Last Modified: Thu, 14 Aug 2025 03:54:16 GMT  
		Size: 20.5 MB (20534623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:a2ac4b9b7a979924c1bca31d81a2c2433fbf31669caf07267b6619122c6636af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96c0c44ebeb6b906c79596990260cab5bee891881ad4cc9c6464da24cfbca8f`

```dockerfile
```

-	Layers:
	-	`sha256:9f97254669729aac53b513d33c209125d333747755977367a4840987574fa18a`  
		Last Modified: Thu, 14 Aug 2025 05:01:37 GMT  
		Size: 6.3 MB (6337534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d7ceb2591f9a4e878e702dff4a01871aa0f0d57c83b819168e59834cfaa6a2`  
		Last Modified: Thu, 14 Aug 2025 05:01:38 GMT  
		Size: 36.1 KB (36091 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:12df44abafadf347882f79746fa31779f1d3db0bb209401eb416c6e6a47f06ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192721527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7549518fe4d333f672bf9c06a565464d640e67ba2fb373b6ec607a3d4f11e0b7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b489405183f5b9a8efdd3a37c57d3bebb68253f8352b3cc28d4c561af742934`  
		Last Modified: Wed, 13 Aug 2025 03:33:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62173f3c06dd14e87e8ea952140162b61079d18bca9964b5d7193323dfb968`  
		Last Modified: Wed, 13 Aug 2025 03:34:13 GMT  
		Size: 98.2 MB (98153226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b333dd5f982a93ffa19de68383bcbeebbfee4cc755b55e6e4dc21b63a60875a0`  
		Last Modified: Wed, 13 Aug 2025 03:33:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ee4708b92d1141b15c9bd989e4bcb9f707f7f848d3c835ec718b7314872da6`  
		Last Modified: Wed, 13 Aug 2025 05:10:44 GMT  
		Size: 13.7 MB (13742005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dd4b96bb6f6e6eea910f090ee6005dded324ae1b0ad2114b424b1e63a3dab3`  
		Last Modified: Wed, 13 Aug 2025 04:25:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e7c0b3270fe671242bb49331ef20e09d2b709c26b6f3aa235a80d4fcab874`  
		Last Modified: Wed, 13 Aug 2025 08:06:09 GMT  
		Size: 29.9 MB (29911887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f0dab13688199fd000a9c3c952ec600239568c5d1fc42ef78d101949a8c6f`  
		Last Modified: Wed, 13 Aug 2025 04:30:21 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5cb42930d55c36368116a2aaf8e76d1e92cac00a9cd9c92e7d954dd0f81fb6`  
		Last Modified: Wed, 13 Aug 2025 04:30:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041599a8ef3bf97b8d7c32314a0dfe4e40c312c8cf799ab6063e647139a5be99`  
		Last Modified: Wed, 13 Aug 2025 04:30:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3daf65d164d2ce412358237e3a25e3c7de4ecfbc813eaf029f2398c4d84879`  
		Last Modified: Wed, 13 Aug 2025 04:30:22 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb1602172b6cd34d32177fbd1ddbf2f55fe7371ce9c4f43ee941637778f108`  
		Last Modified: Wed, 13 Aug 2025 23:19:31 GMT  
		Size: 1.5 MB (1535666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112d4f3e7ae06a20bcb1e6f9b29b39954f903d237e26388378e1c0a612e627ef`  
		Last Modified: Wed, 13 Aug 2025 23:19:30 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4432d4d4f72e52e01965bc83f19feadb4b62308665df32aa2be805625c0a91`  
		Last Modified: Wed, 13 Aug 2025 23:19:31 GMT  
		Size: 748.7 KB (748720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da97aa9add3690615968d46d011debf23d3ad58a70ae00be697e09bc512f9f24`  
		Last Modified: Wed, 13 Aug 2025 23:19:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d12d904488e271590948f6c7e0a91ea39ce055961d19d2afe4ca581bc09867`  
		Last Modified: Wed, 13 Aug 2025 23:19:32 GMT  
		Size: 20.5 MB (20534482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:1dd71d641d10690a8e4fba8d34f1033a197cbbcb1040724068b0f5334822f3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6588803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947d14a7147cb3881c40f2008bc31e4e7cf15f2201211087632b9475f33ff2ba`

```dockerfile
```

-	Layers:
	-	`sha256:0289f5bd4da3495a795293e0bcba61a0f9130ae9df8193d690051a4f5bd47687`  
		Last Modified: Thu, 14 Aug 2025 02:02:15 GMT  
		Size: 6.6 MB (6552659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d690336aa6320c3c4b840fbbcb90d6e3e79cd0244ae0204131bc077fa24687e0`  
		Last Modified: Thu, 14 Aug 2025 02:02:16 GMT  
		Size: 36.1 KB (36144 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:5d86ae962b1a068e2665083ae278b20b6596d4ca41873a0fe063465305d66bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198260934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0efaf4e8e8c53f01efd07cad3850fbe55231faa3f2af4812e79188fa3c8a1b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2b4babf50467b1d04b3e62c523cb3151b33c64e35495e9501d12a15b63f666`  
		Last Modified: Tue, 12 Aug 2025 22:32:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1228856396fa6f4efb8a50b45e68aa9a2021a203ebc0e45731b92dfc40fee256`  
		Last Modified: Tue, 12 Aug 2025 22:47:48 GMT  
		Size: 101.5 MB (101516086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189312da1c9016a4f52cd71965c7664a762fa866649a45a563a203bcfe5251e1`  
		Last Modified: Tue, 12 Aug 2025 22:32:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ced495af7499f6d8f48a48f39d4ec091e7eddc7fd6e3d0f6712b66a86856f1`  
		Last Modified: Tue, 12 Aug 2025 22:47:43 GMT  
		Size: 13.7 MB (13741417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01e6c21c922246cdb9183351998a2071e8cfe4decf2aa58c98fb48c87d22608`  
		Last Modified: Tue, 12 Aug 2025 22:47:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125d3379381d33831bd378a6ea0bfb965fe1a0efa002b5099b67bb3a085ea14`  
		Last Modified: Tue, 12 Aug 2025 22:47:43 GMT  
		Size: 30.9 MB (30872984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a9ff6d09b7b7e33505425c03a2891a2185503ce1ae3e59a6286d5e4052e7dd`  
		Last Modified: Tue, 12 Aug 2025 22:47:41 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836efc7e005b4917351d978dc5579a55ed5825727d719d8e76c6676b12301a44`  
		Last Modified: Tue, 12 Aug 2025 22:47:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08452fccb88e317ee02070d4943b2eb40050aa1de485f636cd34eae7b887bf98`  
		Last Modified: Tue, 12 Aug 2025 22:47:41 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49072c748bf13bf4ef150fc40010b317482a4cc473f7faa507bcb8a9d3e9e569`  
		Last Modified: Tue, 12 Aug 2025 22:47:41 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde6b219d4233f2352447a67754808d6ec29f4a1084de3572df9054b1ae01d58`  
		Last Modified: Thu, 14 Aug 2025 02:38:18 GMT  
		Size: 1.6 MB (1621422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2285e0b98f4157a09b0ce5193414c2ae63af764659e6ade83af1f01d41662bab`  
		Last Modified: Thu, 14 Aug 2025 02:42:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ad47e50f4cf67b033836a7f28725bcd24db7d8f33aa78c59a4ca3bc3a0752`  
		Last Modified: Thu, 14 Aug 2025 02:34:21 GMT  
		Size: 748.7 KB (748717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee2948c8fe1af2964151f31e9aa176d256fdab20d4cbb0c2d0ac2c2d0f785b6`  
		Last Modified: Thu, 14 Aug 2025 02:42:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd772669a7132d51cbc8aae22aefa9bd162b2f244359b6e02371e258f471b479`  
		Last Modified: Wed, 13 Aug 2025 22:06:00 GMT  
		Size: 20.5 MB (20534160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:a23d7e58560087d9b067cc0b8822abd9766dcfa3a62b4eafaef8ad768b6038f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151c551d9a33edf4b562d44179905326c79c8dbe880605107bafa2426fc852c6`

```dockerfile
```

-	Layers:
	-	`sha256:a8b6c4f9f4f8a62444224cd2bcd5c1afd4c7694f8ab011773496e14b15d934b0`  
		Last Modified: Wed, 13 Aug 2025 23:03:47 GMT  
		Size: 6.5 MB (6503974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c32029240dd8ba4c8bebe9cf74d1da6bb2113a5c6a139d91cb13bc25e07584`  
		Last Modified: Wed, 13 Aug 2025 23:03:48 GMT  
		Size: 35.9 KB (35880 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:54556bc9ad11e63f142a4c3ff1e8a8e022360fdc9183c64253abacbc09d7e7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203549301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f4bf2de0742989c4772fa1cc39c292c856126fe7abe607fc4cd07a8e1e971`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a363500f88bae53ed85a0884af78492e18e2de8fc3862f1472e7a5a3e503dc87`  
		Last Modified: Wed, 13 Aug 2025 06:51:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb370a99493c04fbb6a54fc3c2fa12bf4afac30b54e58e473794b525eaca2d`  
		Last Modified: Wed, 13 Aug 2025 07:37:29 GMT  
		Size: 103.3 MB (103328754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc5ef6f8d35100f42cd71cdbcef48544c8e88e6827718d834112c80e310f368`  
		Last Modified: Wed, 13 Aug 2025 07:05:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da22e2ec6c934227472e45c6e4c3dcfd66a21a4ad21a47144e03d56979d1dbe`  
		Last Modified: Wed, 13 Aug 2025 08:30:12 GMT  
		Size: 13.7 MB (13741731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304759033b88a9089e57a86b599e82d9382c7f6d17b2238ca8b05ac768fddf26`  
		Last Modified: Wed, 13 Aug 2025 07:05:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd61c79d3656f2b11eb0551e9ff1cea7f77b48d9b423a8912e9bf8c13233f7f`  
		Last Modified: Wed, 13 Aug 2025 06:31:58 GMT  
		Size: 31.4 MB (31357930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6fe6c48d35d7dd636a6e2327533462f1ce01946e424741007b452ad9649b83`  
		Last Modified: Wed, 13 Aug 2025 06:31:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50720dd05def9bbc168767baa7fd107888d32c5094fa82b0f917436f7f1e382`  
		Last Modified: Wed, 13 Aug 2025 06:31:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265e88774e0c228afbd455f528584f33760dc3d6f95924ad9f64e4258f37eeb2`  
		Last Modified: Wed, 13 Aug 2025 06:31:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af33d886b8fa9f524d9619d62f94141ebc11d0212e30e55beaacbff01476c04`  
		Last Modified: Wed, 13 Aug 2025 06:31:53 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d202147bbfabd4dc50dc884382ddea614e515a77711f361e886e5dc2b58a58a7`  
		Last Modified: Thu, 14 Aug 2025 03:48:30 GMT  
		Size: 1.8 MB (1751685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad141b48a1cc4e4080d827f9f9bc25f44b43d6e378400e943a77f7c53f8bd`  
		Last Modified: Thu, 14 Aug 2025 03:48:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989def85fe8dd26899d95947a9048baa2d9eef7d10dae0d749d757c130884858`  
		Last Modified: Thu, 14 Aug 2025 03:48:33 GMT  
		Size: 748.7 KB (748720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d977bd2c7326a7436f7757af9badcb71a0cbadbf6fa4de3f8618e101f654fb`  
		Last Modified: Thu, 14 Aug 2025 03:48:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f8c2a6d7efb84e4333c96483e222adf91e2638b20358e5196006d4e183ecb5`  
		Last Modified: Thu, 14 Aug 2025 03:48:33 GMT  
		Size: 20.5 MB (20533510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:cf9fa940e0bf9f8909f2693c2d71c9ff625692bc1f29e7f7544bfbab06eb32bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6536987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de5df8de821c39867fcdaa318f3fec617b3e1fd7e2087c39aef1ff0a58a3c9c`

```dockerfile
```

-	Layers:
	-	`sha256:66648c5997ae7eb89030162606f4698a97858674b17ac10d2c4abd078d9da725`  
		Last Modified: Thu, 14 Aug 2025 05:01:53 GMT  
		Size: 6.5 MB (6500962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907dbf82c9cebdd36c8c5b395fb20aafc6c577ed9a90f4e9bab625f843d5712f`  
		Last Modified: Thu, 14 Aug 2025 05:01:54 GMT  
		Size: 36.0 KB (36025 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:aef973de7a42308eab61bb55836cc75fc222513d3c8a3c74fb242793c6c69399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173758478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb21e194b3f8c9090c482e55dfc4c6e847755e9e51c98e824a5c31da46a399a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160fd1a1a421ab2a967d88788fa69f4a8c0d0124bb8618a96dadd2d0b88b93ca`  
		Last Modified: Wed, 13 Aug 2025 10:57:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62186e269f8e7afe7503ad0b95ed43cf9977a95fe4bf4276d7b309de1b2630`  
		Last Modified: Wed, 13 Aug 2025 11:56:29 GMT  
		Size: 80.8 MB (80826980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283e45bba3759ef3324f879c06fb1eebcda36d5470316f27b6e2fd8d86a8a0d2`  
		Last Modified: Wed, 13 Aug 2025 10:57:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339109104405b4a6ee339d0338285d870c405abba4f15e841617157f85f57098`  
		Last Modified: Wed, 13 Aug 2025 17:22:17 GMT  
		Size: 13.7 MB (13740789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c627aa012ab4300f3789442a8064ac255c91af699d0367c012dcbbd838e7624d`  
		Last Modified: Wed, 13 Aug 2025 11:14:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ebe8e5c49a314b9da52619208f3a3ce063238519ce36417a7df9b11e411ed3`  
		Last Modified: Wed, 13 Aug 2025 10:39:40 GMT  
		Size: 29.5 MB (29545701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b80b5ee2c04c91a99af157ac02dea45c2e3438e6b30589dfc421c2be71f35a`  
		Last Modified: Wed, 13 Aug 2025 10:39:34 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cf99df27b9099082008857a17a5ce052e217cc4b09dd70f8659ef53e3ddade`  
		Last Modified: Wed, 13 Aug 2025 10:39:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ae3def76b8d5cd8c957de11cd4ec5c15950a8b484c4447ef2defe54d8be017`  
		Last Modified: Wed, 13 Aug 2025 10:39:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c46fa427a1f24b212de3d2fe65d5f18a92e18326313014f9ef48013b21f0b3`  
		Last Modified: Wed, 13 Aug 2025 10:39:34 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b858cc49378087949060effea4e17523a7cc1e55aba2c1897689af1e76543546`  
		Last Modified: Thu, 14 Aug 2025 03:22:33 GMT  
		Size: 1.5 MB (1461059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da21efe7cc96519cb53d2b5f65c71bb4dc35a0ff4368b6f15b80be7b3427770`  
		Last Modified: Thu, 14 Aug 2025 03:22:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98aca6b17baf66132d02f3c4d6fe83ff5644a76f4c05ea035037427d32ace6d5`  
		Last Modified: Thu, 14 Aug 2025 03:22:33 GMT  
		Size: 748.7 KB (748720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1701536f452ad5f49806793fc16195f302a408b1bf7555251a2b5d9107dd74`  
		Last Modified: Thu, 14 Aug 2025 03:22:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c8d0a1c9a36cd10f37742ed08f4b71a05b93fe7b463e5d8d0323d3d0138939`  
		Last Modified: Thu, 14 Aug 2025 03:22:40 GMT  
		Size: 20.5 MB (20533855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f63b686e09c22c31b1bc5ded89755346a7e5509176b58db16492fc5210e3bf3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378fef63d6770044f8ab11671509e674380ef2399cbb726adb7b531ee716f5c`

```dockerfile
```

-	Layers:
	-	`sha256:b210d985f595b604f0092b1daefc2f6585f0d263fe97b3c1c3be29c56a497497`  
		Last Modified: Thu, 14 Aug 2025 05:02:00 GMT  
		Size: 6.4 MB (6361432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad102a693a50716e4d1c52aca3245242dfd3ed3c52d6131b06b12f5298c9ba4`  
		Last Modified: Thu, 14 Aug 2025 05:02:01 GMT  
		Size: 35.9 KB (35937 bytes)  
		MIME: application/vnd.in-toto+json
