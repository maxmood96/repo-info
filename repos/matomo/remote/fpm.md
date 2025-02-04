## `matomo:fpm`

```console
$ docker pull matomo@sha256:c7cc1a96238a9b9aed117be4a5b1b795f65d3aff9c972a835e83970d4654ad71
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:fpm` - linux; amd64

```console
$ docker pull matomo@sha256:b55ac02d3127bcb02a4640fe00d413796f20345248379f9b50de8399dc3d9256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198195852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4a5966159e51d0f41ce5a071cc498ce13565b9d72905cfea7d7b88de1e2309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fb9b2762214328a8c15405411d616c3a0a5165e14e187f6ae11029a528efb2`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6d2e549616e2d235d2c6ee091b5fc89136b4090b6bd83483b36e5ebbf16fb`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 104.3 MB (104345465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2327de212962dc8fb9c183a9cc211cdad285d6831fd3de227c461d946c2cacf4`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5c79ec7697bee203616406de6e2da668b853f5b9a0e5bf062e3dacc84a3fb6`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 12.7 MB (12654325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397611f822e1635fd5a71185e266667285eb763fa1b0df620e650ffbd2568be1`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6649c69bdbfa87a468be04c01ed690c68644040f7a6ec3cb9e90a4844ce1879d`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 27.8 MB (27827357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e26b94518e4eeaef60d008ddaac4529c95f312de4d4e6e696829c3940195b21`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b051782bf8d5fb8de0af5793bcbe37e02be8929bf321d4967fde92657a4e3fab`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cee8f7af261cbfa7452891ca4e3eb51f8c0c613a0a99e95b7a2280723f633e`  
		Last Modified: Tue, 04 Feb 2025 04:37:37 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f859ec804e55ead3c7753af6bb1dcbe9b3d896698e321610981fac341286e576`  
		Last Modified: Tue, 04 Feb 2025 05:19:33 GMT  
		Size: 3.3 MB (3257983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70a3b4151018e1d246767cca047b1f406120815ec752cfff2cc8b1e80941ed`  
		Last Modified: Tue, 04 Feb 2025 05:19:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed55ab0c2cc5f56746e0493486f6bbb50a6ab4e8423bd40dd00c39c770692300`  
		Last Modified: Tue, 04 Feb 2025 05:19:34 GMT  
		Size: 21.9 MB (21884092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd39138a3953783a4bba9b687d45bef14b0767e791630f11e50bb7de3b673ac`  
		Last Modified: Tue, 04 Feb 2025 05:19:32 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8fa216f4957cb9c3c571d7ae836ae9ebdd49ed389358f916cb95ad4c9d979e`  
		Last Modified: Tue, 04 Feb 2025 05:19:33 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:7d0949686d6af613c07ebb3245c025f749cf5ef6a225d02f450ccefd9e6b3290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 KB (32143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbaedbbf855263f63eef07077d548b2ebaa02f391e1af87260a98fae90594c`

```dockerfile
```

-	Layers:
	-	`sha256:d45ff1f208fa5281f7d92b0e6cbd7e9c7cfb41f086f14045d80f9ab76834802c`  
		Last Modified: Tue, 04 Feb 2025 05:19:32 GMT  
		Size: 32.1 KB (32143 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm variant v5

```console
$ docker pull matomo@sha256:1f75360bf479ed4efbc49495914ea52e3ff791e76408dd74c3fcd9546ad0390a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171305505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50ab5f9d8c8362fa77ba732b1ad98287f13350b3ff231cc4f0fb1f0c8414eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972786f04f039fb3a4d1b82c728a7c7ea9ffc0e85efd517dc45b571b1f62752d`  
		Last Modified: Tue, 04 Feb 2025 05:11:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e43da89859192986d7ea9c98d997ffc5a0763c751bc8a114b8ac40e7013eb3`  
		Last Modified: Tue, 04 Feb 2025 05:11:25 GMT  
		Size: 82.0 MB (81993010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d164497324e1f248e21428931b6af1422a36e02ee93ec9321130fe7aef51ee`  
		Last Modified: Tue, 04 Feb 2025 05:11:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c321b1e7463b13f13b9bfb8337f1d08a83a4c11a2c104cac009b30bd9821f`  
		Last Modified: Tue, 04 Feb 2025 05:56:14 GMT  
		Size: 12.7 MB (12652215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55760e0de3ebbbb2733f123173ae7de86d21103e2b3e2edf35cb630cead3f43a`  
		Last Modified: Tue, 04 Feb 2025 05:56:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efe9b4309bb86bfeb2b806a0bc852d4b3e638698c5095a397a6b8064d233202`  
		Last Modified: Tue, 04 Feb 2025 06:03:21 GMT  
		Size: 26.3 MB (26302322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0821f75439e02910fc40e276884eaeca9af2e274b7636586a2857eb36a2a7857`  
		Last Modified: Tue, 04 Feb 2025 06:03:20 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b756ebb7b3b93f776b93f0eb84189b69db0ceafc0a16380e62dda4b7ff8343f`  
		Last Modified: Tue, 04 Feb 2025 06:03:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605000b2a5822d8bf907c863fdb7aabe5669275b5f6703c97afb41d690f840`  
		Last Modified: Tue, 04 Feb 2025 06:03:20 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396616645d431cc16d44e58592f881f2e55f505879b25f21acd8c9c02ddeca31`  
		Last Modified: Tue, 04 Feb 2025 12:14:40 GMT  
		Size: 2.7 MB (2724744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dadba1b2bc11c8df09fe22e8c9039f73b4435b21137f33a9cc6aec7088fa00`  
		Last Modified: Tue, 04 Feb 2025 12:14:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f053935b90e80669b8952df6c494dc77b58af871bd93a6d5572ddfdc33f736cd`  
		Last Modified: Tue, 04 Feb 2025 12:14:41 GMT  
		Size: 21.9 MB (21882322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f420c1a5cba69f2ae93e4b64f3aa4461304a07889c0c9f4363d15a10f3fa38`  
		Last Modified: Tue, 04 Feb 2025 12:14:40 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065baa02079e7c408abb8a88542946586e8a5b431d054734c850447edaf2b773`  
		Last Modified: Fri, 24 Jan 2025 23:32:37 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:27eafffa15012db9454e9ffbb3d70857eb349c3e59d5de828916eaba16109db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acdfc30cff12a7f786cf50a7bc9f6a18af056ef1becfeab2926b5e3f30118b9`

```dockerfile
```

-	Layers:
	-	`sha256:9a8c414570210801b4da00255f3d191e96c04da71da9c4d72e6c5e9085fe36d3`  
		Last Modified: Tue, 04 Feb 2025 12:14:39 GMT  
		Size: 32.2 KB (32239 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm variant v7

```console
$ docker pull matomo@sha256:24bd83fce82dd889d6419ce0ba1c0f1f2ccb743efba370389370927d87fb30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162638453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9c2b209696d44c5552dd8014dea3cf310e1028ef1a87abd1f06635dabccc2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d546b00afb4b9d040080c0bcc406bf33316623067156773fc2c6b01571dc5c3`  
		Last Modified: Tue, 14 Jan 2025 02:49:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbadf9d833fbe1e5f7e579b22da5a224c4248d4c38649c1535310aa87b326e8`  
		Last Modified: Tue, 14 Jan 2025 02:49:20 GMT  
		Size: 76.2 MB (76162940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827c0e6243599ec0c52a40858b85fe86d2ce54a4d77185b826e94ce33c26525`  
		Last Modified: Tue, 14 Jan 2025 02:49:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a0dc85150671dd83e1962960212d480e409c75ec3a68cbf72db784fb249d53`  
		Last Modified: Fri, 17 Jan 2025 01:34:19 GMT  
		Size: 12.7 MB (12652145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328e89c1cc2c9fd0f94c28fc95f69605ed48642cd799099c8480187e0a23988f`  
		Last Modified: Fri, 17 Jan 2025 01:34:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d6842c02f3dc4b9ff95828d43722a5498b73962be60189ef268e9085cc90bc`  
		Last Modified: Fri, 17 Jan 2025 01:45:41 GMT  
		Size: 25.4 MB (25409174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e3da82300789d8881c7a8893f59dbe59a0added320d1fa9f48039601a1a7c2`  
		Last Modified: Fri, 17 Jan 2025 01:45:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6620ac91454b52afb1bd3c92036bf7c1191980afbda76f576fd79cb114b34793`  
		Last Modified: Fri, 17 Jan 2025 01:45:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1c29624f9af7b8a2566c90d3e8e9de7ebfaf25034e49af595d191dd9e45b9b`  
		Last Modified: Fri, 17 Jan 2025 01:45:41 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c97d969da277394b5f5b738c42db93b7635592561987afbe53e24cf29b86a5`  
		Last Modified: Fri, 24 Jan 2025 23:30:06 GMT  
		Size: 2.6 MB (2602950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c58839b5138b01db6e916a3a52e8099426cb183370c95c04d8db367734dc3d1`  
		Last Modified: Fri, 24 Jan 2025 23:30:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0136fe89ef1f583bcdf49c81eaef58169e1c88f26dcbbdfde4ce9d8c2a6f51`  
		Last Modified: Fri, 24 Jan 2025 23:30:06 GMT  
		Size: 21.9 MB (21882308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf58822f521019ff22a922f7cd42cccce97edecf74de90cc224bd28ac4fa1`  
		Last Modified: Fri, 24 Jan 2025 23:30:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eebe040ebd377c914d8b1eff7f0cc658695c4690990fca16caeb6bcd0feeec0`  
		Last Modified: Fri, 24 Jan 2025 23:30:06 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:063d58c8630976f3e006061393ace9772d4d1913641ef4722b73a7aea1649813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deff0a235532dddf3e1f32a57a6b94dce54d9e653337d354a00d16eaf0bbf0a3`

```dockerfile
```

-	Layers:
	-	`sha256:a832c8ca0e2cda64a966ec6f4ad619bb6392609c3b2109b2de02a87b57b9827d`  
		Last Modified: Fri, 24 Jan 2025 23:30:04 GMT  
		Size: 32.2 KB (32239 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:096321317790b4f50df993466f7a88a2590de6dbceea99859e041887c51a1e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191995368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8c3794415b6320839784d30396b4b6f0ec1c691481cfc91ba56533f42b606`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48015c6e07faccdd2a54d1e2ccecbd028511c6c5d8cf9a4f84b8d4d42d775ba8`  
		Last Modified: Tue, 14 Jan 2025 03:14:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f6eaa105a9e29cbbbc0157f5082daabecac6d65df1a6be8e50afa6dd8b23a3`  
		Last Modified: Tue, 14 Jan 2025 03:14:38 GMT  
		Size: 98.1 MB (98130619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f24c5a85b79cc5db518b237cd81340b2b5649ed577353635cba0aa5362458`  
		Last Modified: Tue, 14 Jan 2025 03:14:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c20c74d7ca7b0f75e754614dd97f97b6e9fe680040e8e6d911ecee26dac89e1`  
		Last Modified: Fri, 17 Jan 2025 01:35:50 GMT  
		Size: 12.7 MB (12654217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f213f403d3868d9c24423423236fc923b73268ace6db9f05835fe73837068d6b`  
		Last Modified: Fri, 17 Jan 2025 01:35:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c057c056ab0501dcf7cca96dc9470d5a3fb26a25f782042bdc51feb4178c74`  
		Last Modified: Fri, 17 Jan 2025 01:35:49 GMT  
		Size: 27.8 MB (27763147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c3816f32f79f6255c8b359254e39f45550e9bd5f31200f4e095c5d298027b0`  
		Last Modified: Fri, 17 Jan 2025 01:35:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cbc6131e57ebbe08e604d2af1b14eda619e2e5855da44e14075fb51779dbb6`  
		Last Modified: Fri, 17 Jan 2025 01:35:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6615aabb22e40576bc8b69d7f187813c6a18b35a92bf32b042067462b9694b5`  
		Last Modified: Fri, 17 Jan 2025 01:35:49 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492c6382ee0cd57d0ee2b56670670107c68a9fea3f7bf074b57231073fe289bd`  
		Last Modified: Fri, 24 Jan 2025 23:34:20 GMT  
		Size: 3.5 MB (3508002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d814411ccf293aafadafaa018950c5987be770aa4c758e52a9f76961325dfb`  
		Last Modified: Fri, 24 Jan 2025 23:34:20 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a01cc91c42bec5a09a3ef41a5523a8a1d4653488035d5953edd7374c0757ec`  
		Last Modified: Fri, 24 Jan 2025 23:34:22 GMT  
		Size: 21.9 MB (21884016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbac3262765d295f7d52bd71580f1561918cc8ad61960d1785aae1df96d436`  
		Last Modified: Fri, 24 Jan 2025 23:34:20 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030a52d1cf34fb7a9b54b823f698d764f0d0d8385f421d1e6979d55887c4fda9`  
		Last Modified: Fri, 24 Jan 2025 23:34:21 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:daaa095f3bac7545893f2114383976ed61ee2a6a85ff6ae0f607c89a8eb81048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b605c1773178b09cda89ab3392974cc5342a5d7e836cfe19cd177fef839d6f`

```dockerfile
```

-	Layers:
	-	`sha256:62c5e162b68f4d108d903871a326194bc835ff4807310c14eeb458a40aded135`  
		Last Modified: Fri, 24 Jan 2025 23:34:19 GMT  
		Size: 32.3 KB (32271 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; 386

```console
$ docker pull matomo@sha256:c8e055a426e31a5a07df7d677be705348728364381cb86d9fca1bae281c979fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196797858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae3bee068707fd90bbe5777eeef209c5b4427d173ed1dec021bef79bfc2a48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea09fb36a8099f1bcb59bd46c7d715db7cdefb7975374b0711ad22ffc7b23432`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693904ad59bbd2a8798ef195d49e8fbc5ce0a2e6573a884c2d7d28e6ee99b7a3`  
		Last Modified: Tue, 04 Feb 2025 04:37:04 GMT  
		Size: 101.5 MB (101513189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ad2b94d4db4515b71f8fb2531591234c0cf7539976dcfac45251553f6f778`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e62d0fc0b15af05f5f61e2e61d26d488c4d5d8133f6bce5148bc24598c619`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 12.7 MB (12653404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f603b816c1838e02a4e96697b02f4f7231ae56c6df15f4a84c33ffd1ce763fd`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93f61e4b8c60ef4b9e9b569aebb77e67d1ee6fb0a9c98bbde9372f31044f747`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 28.3 MB (28336315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e541abcbf1d075e22aa8a544d489f9729ea8d66bea505786e8a7c8af9d4f3e`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a53fb1986722c767931688948d7b91fec36e9af83fc2636797266f375cf5cfd`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52b1bfde8607427823e5899da9ddb5ce7c4a3c27828b6042710d7cb9d89d33c`  
		Last Modified: Tue, 04 Feb 2025 04:37:03 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9c315e5d95f58dafb56a5dbd6b8e3f7b82ed2f7de3b39bf87170fbbedda0c7`  
		Last Modified: Tue, 04 Feb 2025 05:24:01 GMT  
		Size: 3.2 MB (3209822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f448485fea0b2452dfab53047ba86657df5c47cebafcc3289850a1c7e8d1291b`  
		Last Modified: Tue, 04 Feb 2025 05:24:01 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e61dc801dbd044c6b88fbbd46b3d76f2eb8d2989201bbc12ded59fbb04abce2`  
		Last Modified: Tue, 04 Feb 2025 05:24:02 GMT  
		Size: 21.9 MB (21883340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fca685cb8eed679b29db9992da86994afee75db8c669c8e928f77f5940beefe`  
		Last Modified: Tue, 04 Feb 2025 05:24:01 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da759aa3de4fd155b512a7329ff86499290422510ee21d26729476d223c55f78`  
		Last Modified: Tue, 04 Feb 2025 05:24:02 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:caf9bb0e0c02971e4c2d9fa77c6d4f7cf948847a618224d9256167b5129e586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 KB (32107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8ef82f9856ed4a5cc5e3417c95303c419aae64b4ce54cf8f094f5154cf439f`

```dockerfile
```

-	Layers:
	-	`sha256:acb903ac5a45d8c8ec449526c506e1ae643ea2af7424d9d9f5a4c2df64752802`  
		Last Modified: Tue, 04 Feb 2025 05:24:01 GMT  
		Size: 32.1 KB (32107 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; mips64le

```console
$ docker pull matomo@sha256:365ed8087e61d23e603fe847c4b344b7851cf399585957011cc894fceaf86750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173450941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609880745992a5ebdd87934552117fb86a5f6ed9ebe6164ad604d12962e8d952`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89185b6d37a912303ece30771194df4d9a4bd81c186ebd0c112827238102177a`  
		Last Modified: Tue, 14 Jan 2025 04:25:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b93be406fdfc396e7ea27bf3106aaa3e69436152e180b74a54061e746a13506`  
		Last Modified: Tue, 14 Jan 2025 04:25:19 GMT  
		Size: 80.7 MB (80668955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c06af120fe87200b0a7299150015ee7a1b24d5687e5fd9ff3e0b2c26b7b1bd`  
		Last Modified: Tue, 14 Jan 2025 04:25:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d684a3d1dd2d4e9b9da185d69c2be691fc4e1230281d16382f6f404c0ac945a5`  
		Last Modified: Fri, 17 Jan 2025 01:44:34 GMT  
		Size: 12.7 MB (12651587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aa6f8f0605791fa93ec7897f18f862c4823aae8843250ded7420ef7068b46d`  
		Last Modified: Fri, 17 Jan 2025 01:44:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38320a98cb5f0676da1435ed3fe9e6a122ef690c7bccd137d37944fd148d4ad`  
		Last Modified: Fri, 17 Jan 2025 02:18:47 GMT  
		Size: 26.9 MB (26915752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5eb8a051c8f00a43f20bddd12422366fce574587a6baae549b86b8d73213ff`  
		Last Modified: Fri, 17 Jan 2025 02:18:44 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351b62533f1ab850bcd4ef672002e8e03e0bfd41979e5daaacce2e9e2188672`  
		Last Modified: Fri, 17 Jan 2025 02:18:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb141edd8aa38079b2f1e0c310ddffb56819720b70d0739fe65c434b13991f`  
		Last Modified: Fri, 17 Jan 2025 02:18:45 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e499de46e56ac5683ced8793242161b8a55a5c5d88e2ea91abc3cacca026a1`  
		Last Modified: Fri, 17 Jan 2025 04:01:58 GMT  
		Size: 2.8 MB (2831169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0282b7a4b9f2d64a7f221059e4f5742b8c796c19ae0f6eb096c6c087af0c300`  
		Last Modified: Fri, 17 Jan 2025 04:01:58 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0da19aea1965b191d553f7ce2e55dbaa28cbc6d5e9e57a403d98ec796e2bbf`  
		Last Modified: Fri, 24 Jan 2025 23:30:03 GMT  
		Size: 21.9 MB (21882491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ae41cc07230e0aa4d77a047bf2210d7934622155c1e80ce9a14a4280715df`  
		Last Modified: Fri, 24 Jan 2025 23:30:01 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e5ef254be158f4bf4536fdf2f08b89cebd22ad1c084023047e02839a368e70`  
		Last Modified: Fri, 24 Jan 2025 23:30:01 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:1a5abffccffa7538703e030eb5cc76327b7f25435062175e901cb6b9a2b2f731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acc7faddda0754513c11d9156febc594a9ab069b740fbadebfc85ab40ea9475`

```dockerfile
```

-	Layers:
	-	`sha256:8e56cbbeb821014a3faefaaf83deb2c71f688ee42720d8e36ce2b0fa16e61d51`  
		Last Modified: Fri, 24 Jan 2025 23:30:00 GMT  
		Size: 32.2 KB (32209 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; ppc64le

```console
$ docker pull matomo@sha256:fcc9c77073cc3e2316afa8218685cb452cb4808c189656bb5731f3282e826cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (201974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71cd48cbee75fc9700afc86889d809b175a7a64774a7864aa82dff73ed00417`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880827561304c75010a4d05501b52a649ab01b28573a0e1238b8b2cfc0987b4a`  
		Last Modified: Tue, 14 Jan 2025 03:20:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8101bc0347decf245b442b5f7813aa3ea26f953213626a52bbbf98a1f1d3319c`  
		Last Modified: Tue, 14 Jan 2025 03:20:52 GMT  
		Size: 103.3 MB (103324779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88d523ef6cd37508f451e4c05ba1fe1868379b426cce9cbb1f53b8af157e5d`  
		Last Modified: Tue, 14 Jan 2025 03:20:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84047d3ba6fbe1711208c33216ae0845c2b3c9845a49f32b641b2dad2cd16e44`  
		Last Modified: Fri, 17 Jan 2025 01:30:37 GMT  
		Size: 12.7 MB (12653784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5252de6700252b48c5251fe04658fafbb582a6ee0ccaabb011f6d5c66860917`  
		Last Modified: Fri, 17 Jan 2025 01:30:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a3db788575b02bcd9ba17e093a780341806070ead8d5d880bb5316e7adb19`  
		Last Modified: Fri, 17 Jan 2025 01:34:06 GMT  
		Size: 28.9 MB (28886147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2d41cff347225bb9c5d1643c590ddf0648d63d0005ab87017c9216641baba`  
		Last Modified: Fri, 17 Jan 2025 01:34:05 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451025b7406e496f49c514e3a2aa0d4e8821eb5aa02ecacab5537a148f06886e`  
		Last Modified: Fri, 17 Jan 2025 01:34:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b61980dfa130f6cb63661d6635830b8f826ffadb1c91bc949b03743d9984d8`  
		Last Modified: Fri, 17 Jan 2025 01:34:06 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a3a8ee99f99280dbe79cca7a967c716f13616acd4596d3703462492df5194c`  
		Last Modified: Fri, 24 Jan 2025 23:31:11 GMT  
		Size: 3.2 MB (3166746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e84845d602bb9a5dc865e7355c0b106cf8307504c6a82cc71aff47ca792e9d`  
		Last Modified: Fri, 24 Jan 2025 23:31:10 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3369f9bf4bd7933906d70d03137483de4a48349e53b3624a033cfbf288a00d`  
		Last Modified: Fri, 24 Jan 2025 23:31:12 GMT  
		Size: 21.9 MB (21883970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050be12105be4a7e5165eb82c3a31bb3acb030a514df0c2b7d51b39aee2fd3f8`  
		Last Modified: Fri, 24 Jan 2025 23:31:11 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d01bdc09f9c4e91e4cc505cf34a8aae80a107d2e3fd7437a7a6771c089abb35`  
		Last Modified: Fri, 24 Jan 2025 23:31:11 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:3291d587278c39507ca3001b74ea47970091aa9d495d3c2ce7e40fe01a1bdd32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b178f2d21ccb19f6b99ead7a0468e3003d671a6e53accaf6b44525f0c04b8ff`

```dockerfile
```

-	Layers:
	-	`sha256:49f4e48407968c214c0f40da8de218ca9c4703e80adbc0450c2901cbfbcd52c2`  
		Last Modified: Fri, 24 Jan 2025 23:31:10 GMT  
		Size: 32.2 KB (32191 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; s390x

```console
$ docker pull matomo@sha256:12cfb01ac19f70c9189020c3c81898a37c2f4f04f34752fb0b5daa3b2dc7a2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171949809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d646e3345810724468af3d12a5d174fc3ddbf921895262c3cfe21e4fa7fdd2b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 05:16:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 05:16:13 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 05:16:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1d54343fdf4189be98bca62d5af4bba69360a111a84090af72c0ba9396bd84`  
		Last Modified: Tue, 04 Feb 2025 06:08:45 GMT  
		Size: 12.7 MB (12652581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ddf30ec4a44bab4aef6e34e4cb700ded326a0e84510c17be2bd428baae3d5`  
		Last Modified: Tue, 04 Feb 2025 06:08:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f860f6051485bceade5172875be371c77cc5f238037378a506f69aa5a754e7`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 26.9 MB (26921925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05189f452a1f81f87353268d939602ecec5aae28ab59b7404665f7a3e7240617`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7818f8df4bca466c625f91cd16c3f8ac75a298f3f6cd2bfed2f2daa93cf54`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34deef4e13cd87f26cb7444f1d8c4f26c604fd5a1a8e0ccb1319f67c0c814cc9`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498055d70e36690871c3e876d8e4e7e68d4b5160131854ffde21984380c2da14`  
		Last Modified: Tue, 04 Feb 2025 13:30:26 GMT  
		Size: 2.8 MB (2802136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a84376fe45d295979cebc11cfa604bec5657faf00b3559c1d7e2794a5a24bdf`  
		Last Modified: Tue, 04 Feb 2025 13:30:26 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fdbca5e828f7f128c5d8d6003ee9a224574c9fe11a87d52dfc98f87c317f25`  
		Last Modified: Tue, 04 Feb 2025 13:30:28 GMT  
		Size: 21.9 MB (21882988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bb37e01ca6a516a0a7499448d833e69c37ef8542a6cb66296a3a9aa9dd64e4`  
		Last Modified: Tue, 04 Feb 2025 13:30:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69c4cf666a00396a38b9c7f0572986d548aae2cc528c9cfda36a85385c64f4`  
		Last Modified: Tue, 04 Feb 2025 13:30:27 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:3769f35ea34fce19368e2d555172385f13bc495fac3e6f49252a54e8fb240539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 KB (32136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0189af573d7d6370025dc3accc16b7676410c730a68e9cb8c3242ac43ac3a5d`

```dockerfile
```

-	Layers:
	-	`sha256:5480488d1b63d420a753704b57e7c03f853d731dcac44c18954c02758a67aaa3`  
		Last Modified: Tue, 04 Feb 2025 13:30:26 GMT  
		Size: 32.1 KB (32136 bytes)  
		MIME: application/vnd.in-toto+json
