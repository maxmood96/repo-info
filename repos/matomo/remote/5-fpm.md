## `matomo:5-fpm`

```console
$ docker pull matomo@sha256:57d3b2f11301613c93e0b3833e272675a57f7698f8f43d8b56c7ccba393123cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `matomo:5-fpm` - linux; amd64

```console
$ docker pull matomo@sha256:11140c1d0ce39b931fe84885f74a37537736e8ce9cc777dbda5f4bdc9cfbb773
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198376908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c6ea38acf880a26048b17a19a3c3974ed3dad502d8f312fdb3e657e02b6d91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:57:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 02:57:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 02:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:57:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 02:57:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 02:57:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 02:57:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 02:57:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:56:48 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 04:25:29 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 04:25:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 04:25:29 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 04:25:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 04:25:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 04:36:44 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:36:45 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 04:36:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 04:36:45 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 04:36:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 04:36:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 04:36:46 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 04:36:46 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 14:33:23 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 12 Mar 2024 14:35:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 14:35:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Mar 2024 14:35:04 GMT
ENV MATOMO_VERSION=5.0.3
# Tue, 12 Mar 2024 14:35:18 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 14:35:19 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Tue, 12 Mar 2024 14:35:19 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Tue, 12 Mar 2024 14:35:19 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 14:35:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 14:35:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de14226e1706b621fe796af63b375db247a2490752558ed4f5ea40648234129`  
		Last Modified: Tue, 12 Mar 2024 05:25:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aaf617d1d2bc41efbec77e9f05370e6f35d8f4363fb26fa04883ec538b7d66`  
		Last Modified: Tue, 12 Mar 2024 05:25:37 GMT  
		Size: 104.4 MB (104355586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba065e262ff15c57d91609cae32d80920edac1e9b0826e0d8cf5f0f3c60107`  
		Last Modified: Tue, 12 Mar 2024 05:25:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006b8ba633cafcfa2be36c73bdb548b234c20a710d43d16853d949f225280ac0`  
		Last Modified: Tue, 12 Mar 2024 05:33:45 GMT  
		Size: 12.4 MB (12399763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c35782713764d40912dba6b044b88aaa5aa97fef356c401dd31aa2068ae67a`  
		Last Modified: Tue, 12 Mar 2024 05:33:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a002d6b865abcbff20e0b470b1d792cc3ed74b6c7a988fbb4047e630dad6f`  
		Last Modified: Tue, 12 Mar 2024 05:34:28 GMT  
		Size: 27.8 MB (27773975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223a51b68688a932a4bcb81234ebcf47219c60e1ccb1c96324df259fbd432daf`  
		Last Modified: Tue, 12 Mar 2024 05:34:25 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef561950c6a2f2050ce07f62d258c0480ea22f155624200fea13634f9ceba0c8`  
		Last Modified: Tue, 12 Mar 2024 05:34:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8695a429c11332e5ba26147662c6ab9203f1bd2714a52e1ba1725aa2c31d660e`  
		Last Modified: Tue, 12 Mar 2024 05:34:25 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d6ff42bdf7d22f81f297c3a6ade4fcfcc6fa99be82f1b94a250106ea213fa1`  
		Last Modified: Tue, 12 Mar 2024 14:36:16 GMT  
		Size: 3.4 MB (3438327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d005c40c10a3bd69468032a431009556e966184ae7795f5a723e7c7023a9b615`  
		Last Modified: Tue, 12 Mar 2024 14:36:16 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174e7934fdd677d9baba6172ccadabc0040266c93ad12e8c5446e916e5218a2`  
		Last Modified: Tue, 12 Mar 2024 14:36:19 GMT  
		Size: 21.3 MB (21270717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9193350a1b72d185fc7965fbfab4997e15e86574efc5c6611a32eb06bc7eb987`  
		Last Modified: Tue, 12 Mar 2024 14:36:15 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1425464e13a5004e51fa65bd34b2be180e27afe7ca38ee432645e16d1ad840`  
		Last Modified: Tue, 12 Mar 2024 14:36:15 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; arm variant v5

```console
$ docker pull matomo@sha256:205bf84ab20c7c8dec21088b138768fa37e53ab9e82226119aa9d66bcf97a891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171743612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4742f986fc20f06f59ccef4312c61a0090c98ba60e404ca898bf7127a4895937`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:47:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:47:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:47:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:47:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:47:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:47:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:47:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:47:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 02:38:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 03:01:41 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 03:01:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 03:01:42 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 03:01:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 03:01:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 03:11:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 03:11:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 03:11:24 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 03:11:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 03:11:24 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 03:11:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 03:11:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 03:11:25 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 03:11:25 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 08:43:11 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 12 Mar 2024 08:44:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:44:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Mar 2024 08:44:42 GMT
ENV MATOMO_VERSION=5.0.3
# Tue, 12 Mar 2024 08:45:01 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:45:01 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Tue, 12 Mar 2024 08:45:01 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Tue, 12 Mar 2024 08:45:02 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 08:45:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 08:45:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d115fea1b4a8106e263db629be1619e1687e09620739ce2ec2b09ef0f7216b`  
		Last Modified: Tue, 12 Mar 2024 03:51:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1c5741512c603cc1e5fdb27395ab09059c53c3871664e3c0fa08051670462`  
		Last Modified: Tue, 12 Mar 2024 03:51:27 GMT  
		Size: 82.0 MB (81999306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0a94ea1638e6635c0e4c239bab002203d65e36eb7b12bb6d9fdfece6154dc1`  
		Last Modified: Tue, 12 Mar 2024 03:51:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde26409f32bb7fcab5a7fd52409a06b77ec3bdf5c9f17bff0fe8aa7d142c36c`  
		Last Modified: Tue, 12 Mar 2024 03:59:34 GMT  
		Size: 12.4 MB (12397727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c09bdab390aa330b0607c8f7190d802ea7a456a0466ee94a9f8209ef30aa91`  
		Last Modified: Tue, 12 Mar 2024 03:59:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc82f19b75c0dbf7d9a5aa766fbd2badb5d0ab6168cf16c8a3d32f02936820cb`  
		Last Modified: Tue, 12 Mar 2024 04:00:24 GMT  
		Size: 26.3 MB (26273025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab29c53f01ebc06d79e15e5c4fd328d7417486c8de9db43eb46a3c2528c2fda2`  
		Last Modified: Tue, 12 Mar 2024 04:00:20 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e71767d816b2965ec8ab971ce13b5d8da5060ad35852d2321e0b513a87180`  
		Last Modified: Tue, 12 Mar 2024 04:00:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9c8c20c4f655f69feb26ca288950dcb509a6990b12e87e2889667c9f65d50`  
		Last Modified: Tue, 12 Mar 2024 04:00:20 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad14a766df7e48f3b5a260d65979e0274ce036faeaeb9ff5ecdd0380100bcffd`  
		Last Modified: Tue, 12 Mar 2024 08:45:45 GMT  
		Size: 2.9 MB (2906206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de60f32ed6e1bc6c0f4c79e8a44600945f8d1c86b3879edc9bc675092246289`  
		Last Modified: Tue, 12 Mar 2024 08:45:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056c354ccb56f511988a11be4eba7796fc9c44d5e829909cdd3b1eef8e840b0b`  
		Last Modified: Tue, 12 Mar 2024 08:45:50 GMT  
		Size: 21.3 MB (21268965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a20fafae28ff60e4567467e3444b3d10ff22b5ab19d8e3dcce90d7f7e9a61f`  
		Last Modified: Tue, 12 Mar 2024 08:45:44 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008f61d6032ae82c4419d28e6a25ef18fdb4aaa1a71cbe313ce9cb9a594a5686`  
		Last Modified: Tue, 12 Mar 2024 08:45:45 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; arm variant v7

```console
$ docker pull matomo@sha256:c656e6a78c04cfc99d5ac05ade13961d66a61395d553bbd6e50f71a79aa441c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162739482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7b5e0471a2ca167712dc8232e0b399899eab035dbb218a71e369af4e4596d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:23:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 07:23:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 07:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:23:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 07:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 07:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:23:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 08:13:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 08:38:40 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 08:38:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 08:38:41 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 08:38:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 08:38:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:46:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 08:46:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:46:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 08:46:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 08:46:52 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 08:46:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 08:46:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 08:46:53 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 08:46:53 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 12:50:59 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 12 Mar 2024 12:53:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 12:53:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Mar 2024 12:53:29 GMT
ENV MATOMO_VERSION=5.0.3
# Tue, 12 Mar 2024 12:53:44 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 12:53:45 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Tue, 12 Mar 2024 12:53:45 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Tue, 12 Mar 2024 12:53:45 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 12:53:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 12:53:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd82a33324e79052aa5fed0978c223b7d05b5a41532eca869d5602ee24d0c7c`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57829c9789b8ee6e6ebe4a80c39f9393df7fcf20975d1d8135fc2142cad63d8`  
		Last Modified: Tue, 12 Mar 2024 09:24:42 GMT  
		Size: 76.2 MB (76169934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff1e9e48950eb6ede1065099dd2b976917707ffa4953e5c351638a845668823`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b604a6f4cee5f6ca52306f01ad9901f8afd322d4d7f4c78e6a8f21aa46501a8`  
		Last Modified: Tue, 12 Mar 2024 09:32:55 GMT  
		Size: 12.4 MB (12397774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfae62ee17797767c892349c76e5cf2c92f52911372be557060171af4ea3ba`  
		Last Modified: Tue, 12 Mar 2024 09:32:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eb1403fca13541a8b50a12ac80af046eaa4427517aec442f9da3603803f0f2`  
		Last Modified: Tue, 12 Mar 2024 09:33:41 GMT  
		Size: 25.4 MB (25386500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c2ce338debc8508e3a14f8ccb6770a9778536cb0c305bad8a95f964c45169`  
		Last Modified: Tue, 12 Mar 2024 09:33:36 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99ad8236ea7fb04acc47f599429210247b74eb3ca46ba8a5b202a2934d34772`  
		Last Modified: Tue, 12 Mar 2024 09:33:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bf13cbe45021427884c1f09fa92eb6a3b55459a3c0973e4b182f289b1bfda4`  
		Last Modified: Tue, 12 Mar 2024 09:33:36 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ad41bc2a7bfbe19b63f9dd1ba26a525d8d788f549ba194882aa6f402572143`  
		Last Modified: Tue, 12 Mar 2024 12:54:33 GMT  
		Size: 2.8 MB (2785143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1cc58022ddbfb47cba8ef5a14c8f45034f8fc3cb1e46e7d021e240b5277527`  
		Last Modified: Tue, 12 Mar 2024 12:54:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8501ffa39793ab7907971ff4f1c494fec5de49e8ef2e359a1cb5f986c8db14`  
		Last Modified: Tue, 12 Mar 2024 12:54:37 GMT  
		Size: 21.3 MB (21269036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b2b8b339200d2360ba34dcd75ac54f16a05e03b28d1462fa22645d2a7b1e3`  
		Last Modified: Tue, 12 Mar 2024 12:54:32 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c60f54fe35a75624a03aa869c681c8ebe8800283ba86287dfe2792855abf04`  
		Last Modified: Tue, 12 Mar 2024 12:54:32 GMT  
		Size: 824.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:003b411633d6ff6258805bbe436efaa39facdf4c3d63c0f297c1169c93aade05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192383415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da5a322ab9e56362c785bd45d109873fdc5294b1347cd01bc730e155d804fc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:38:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 04:38:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 04:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 04:39:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:39:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 05:36:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 06:02:18 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 06:02:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 06:02:18 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 06:03:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 06:03:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 06:13:15 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:13:16 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 06:13:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 06:13:16 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 06:13:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 06:13:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 06:13:16 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 06:13:16 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 12:02:57 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 12 Mar 2024 12:04:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 12:04:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Mar 2024 12:04:49 GMT
ENV MATOMO_VERSION=5.0.3
# Tue, 12 Mar 2024 12:05:01 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 12:05:02 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Tue, 12 Mar 2024 12:05:02 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Tue, 12 Mar 2024 12:05:02 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 12:05:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 12:05:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b17d6e35656ac020a43a3f9453f06b61a9c61212e0437b31bac9d2b974cb4d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8431cb294ec999c969b368afe1f6bb5484654b2ce2932cb1a6780d9c52781090`  
		Last Modified: Tue, 12 Mar 2024 06:57:29 GMT  
		Size: 98.1 MB (98126016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735009beb2cceac6bf57add7c26d3a77c8d92fc49ea5e05d8b2452e84a09b61d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99216a786ef35591403f1e3f19f45e61338d667451e3400c37eebdb10b4e0063`  
		Last Modified: Tue, 12 Mar 2024 07:05:08 GMT  
		Size: 12.4 MB (12399630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06463876919baa94743dadcd1a36e107254104053c7b7bf361f99cb1bf43488d`  
		Last Modified: Tue, 12 Mar 2024 07:05:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b2bc10aa863bb53e84fb58cb7f92c2b7f289207dcda8a58b90000446d8a771`  
		Last Modified: Tue, 12 Mar 2024 07:05:49 GMT  
		Size: 27.7 MB (27732779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7534a7f58b7255bbd7947516d24a6cae2efa17c974df263abc3d75d76d79bf3`  
		Last Modified: Tue, 12 Mar 2024 07:05:46 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125b17a16e71a2c839d12d5be1c1dda3da399e282e7e4ba687c5fe0344aad9d`  
		Last Modified: Tue, 12 Mar 2024 07:05:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea281c827291cc569846936d7125212ec6ef40b36d3b7abe2507e10261401d5`  
		Last Modified: Tue, 12 Mar 2024 07:05:46 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b382afec01e3d919be740a1338c048cb86408b30133b096ecdab22a33f43051f`  
		Last Modified: Tue, 12 Mar 2024 12:05:44 GMT  
		Size: 3.7 MB (3683669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655d30023a92ce1f787c93de087ea4136943e2a99012f55c1e6b072b43fe1d85`  
		Last Modified: Tue, 12 Mar 2024 12:05:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c838943afe7b9ca96326d963a96ec67a09c4faa11dbcf683d96be3f376c527`  
		Last Modified: Tue, 12 Mar 2024 12:05:46 GMT  
		Size: 21.3 MB (21270523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c8bbbaefb86dc4e9efe5005e40133576ee95845010eebbf165e32529a47d00`  
		Last Modified: Tue, 12 Mar 2024 12:05:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42673a9cf5844db1ac0cb62550f999fcc82426a6309ca23eb79bbfcac193d73e`  
		Last Modified: Tue, 12 Mar 2024 12:05:43 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; 386

```console
$ docker pull matomo@sha256:e824c1fc8225334fe1fb18b8eef6cedd365b27372ee9967dbd23c4adb6b67969
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197028232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccd285dcc381ae4d0bbd7a55c74755a8c9c5ab8e2ec18b1bcae46089e1606cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:39:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:39:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:39:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:39:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:39:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:22:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 04:11:19 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 04:11:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 04:11:20 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 04:11:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 04:11:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:31:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 04:31:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:31:14 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 04:31:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 04:31:15 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 04:31:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 04:31:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 04:31:16 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 04:31:16 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 15:30:53 GMT
ENV PHP_MEMORY_LIMIT=256M
# Tue, 12 Mar 2024 15:33:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 15:33:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Mar 2024 15:33:05 GMT
ENV MATOMO_VERSION=5.0.3
# Tue, 12 Mar 2024 15:33:23 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 15:33:24 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Tue, 12 Mar 2024 15:33:24 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Tue, 12 Mar 2024 15:33:24 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 15:33:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 15:33:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc8b418f2e8ebe03c4a8d60a403099d5bd9956664693b358caef9096763fabd`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572f25d2333bd6d54c124fa174175081a9c95780122966ffb6532bd93757a9bd`  
		Last Modified: Tue, 12 Mar 2024 05:53:38 GMT  
		Size: 101.5 MB (101519737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6e71adc002ea9786257601b0d391da402881cf3c46d70b1bf238b5e218a47`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42183acb22a45a407ee391e5e1d7a5c1d96995d4d8e3ddcdf08ff2aded487bd7`  
		Last Modified: Tue, 12 Mar 2024 06:02:54 GMT  
		Size: 12.4 MB (12398901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd5e6cd825d866eab7a61de4336aa90d884cafa3280d3b48126a9e03001b23`  
		Last Modified: Tue, 12 Mar 2024 06:02:52 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ca69524da358af17c6f55b6600e01a968d6797fae7776870a4c6392316f4b1`  
		Last Modified: Tue, 12 Mar 2024 06:03:50 GMT  
		Size: 28.3 MB (28293941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9303eb1ea19869d6d30d33f1cb8125f344dd94b387678c6e8261df9e536d46`  
		Last Modified: Tue, 12 Mar 2024 06:03:44 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4183c81f1921bb46e4c57377b130e6b2b89848dfe9dc6b2e60837832fb88d7`  
		Last Modified: Tue, 12 Mar 2024 06:03:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cc35e67f17a0b472ff39c94114a980588db98efea00509977b20ed64466cf2`  
		Last Modified: Tue, 12 Mar 2024 06:03:44 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e217de5f124f25ce24fa01d3d7938a39c728ccb3d496a5d1faa15b7df70ad1`  
		Last Modified: Tue, 12 Mar 2024 15:34:15 GMT  
		Size: 3.4 MB (3389537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a12234250b5fabb51412f4525eebbad20095740d8b4479db208028882e13f40`  
		Last Modified: Tue, 12 Mar 2024 15:34:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c6ae9f6f9d8ce57e8083e438357dd667a1278e79ad9dea3e96e05ecf7db87a`  
		Last Modified: Tue, 12 Mar 2024 15:34:20 GMT  
		Size: 21.3 MB (21269880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd13e8cf5c95451eb9f8f90c03061479406f532ce4e8d3b25d6e210dd2e9f42`  
		Last Modified: Tue, 12 Mar 2024 15:34:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e5d99549fa12165725aace502719742e6e9278423f57fc4bec42007263ddc7`  
		Last Modified: Tue, 12 Mar 2024 15:34:14 GMT  
		Size: 822.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; mips64le

```console
$ docker pull matomo@sha256:1a5e3d34f82edb24fc66bc95cc0a7d48cadffb1500935aa0e30b39d5dea23526
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172532811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2760d70419bff30ed61b3e5b56281f31cc55c5595dc273eb40f5eaa570c1aae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:14 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Tue, 13 Feb 2024 02:04:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:47:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 07:47:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 07:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:49:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 07:49:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 07:49:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 07:50:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 07:50:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 12:03:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 22:17:39 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 22:17:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 22:17:45 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 22:18:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 22:18:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:08:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 23:08:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:09:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 23:09:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 23:09:08 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 23:09:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 23:09:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 23:09:21 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 23:09:24 GMT
CMD ["php-fpm"]
# Sat, 17 Feb 2024 03:03:14 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sat, 17 Feb 2024 03:08:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2024 03:08:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Mar 2024 20:18:27 GMT
ENV MATOMO_VERSION=5.0.3
# Fri, 08 Mar 2024 20:19:33 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 20:19:39 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Fri, 08 Mar 2024 20:19:44 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Fri, 08 Mar 2024 20:19:50 GMT
VOLUME [/var/www/html]
# Fri, 08 Mar 2024 20:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 20:20:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a21685927545579c956a485112e5f2dc77a3d66b4398a490bf6f7eef2b6f26c`  
		Last Modified: Tue, 13 Feb 2024 18:11:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b18ee5ec9cb02365c8ace7580a68b57f8a60cf99c6445f321fb4f00d6f022c`  
		Last Modified: Tue, 13 Feb 2024 18:12:00 GMT  
		Size: 80.7 MB (80667136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c441db64bfe56f8d986d21cab01a3af285e5b84032ab2c030bb242ac622d256`  
		Last Modified: Tue, 13 Feb 2024 18:11:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6207d79d03e917382744830208a5274842c7ec3b10747764dea63d2a4fad771d`  
		Last Modified: Sat, 17 Feb 2024 00:30:25 GMT  
		Size: 12.2 MB (12192328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c35f3025ce675092f7cc0615a040a7c8889f3dbda249252c0b12d2db8a6087`  
		Last Modified: Sat, 17 Feb 2024 00:30:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0869616d6d74d817814fc1048d15b45c31884bf75648b94098551c9400d88a47`  
		Last Modified: Sat, 17 Feb 2024 00:32:00 GMT  
		Size: 26.7 MB (26667400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150b8ea521a388900e7fe88f1258dc7792537bfbf8b3a85d00213a5cd5fb2c62`  
		Last Modified: Sat, 17 Feb 2024 00:31:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6206c00e59b2f241fdcc09eeeebd78c06fe1c86a56a2a07ac6a89c38318828db`  
		Last Modified: Sat, 17 Feb 2024 00:31:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724acbcf9b432538ca6154a4be5bb3625adf2371fb1e45944acf84fc5807782a`  
		Last Modified: Sat, 17 Feb 2024 00:31:43 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6985c1274dabfb02d390670d9177ee29cfd64f2893bbb383d39ba461a38d15`  
		Last Modified: Sat, 17 Feb 2024 03:11:27 GMT  
		Size: 2.8 MB (2808275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab63feb82b5d2d40ddea6386f43a9de0367ede7c7efd7488a0dbb7241de57af`  
		Last Modified: Sat, 17 Feb 2024 03:11:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2117b66945db9d39e029b19b62f0cbffe26e10b1dae57c8c57f0ce9abb200c`  
		Last Modified: Fri, 08 Mar 2024 20:21:40 GMT  
		Size: 21.1 MB (21064249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c60998684d1d8d86b2a18d46e5eb69948502b56cc6cb1d75ce013c754352846`  
		Last Modified: Fri, 08 Mar 2024 20:21:24 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c82afef34bd31f4ca6cb5c0ff6f1d95bfc6f06c5d0b78720019f2d9eb88966`  
		Last Modified: Fri, 08 Mar 2024 20:21:24 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; ppc64le

```console
$ docker pull matomo@sha256:56b89f89911f463757d305b0e0f29cb727db22c716b07f3fa0c320b31e9ddc72
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.3 MB (202298353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d074db6e33ed81501b8fffa2cd1faea30e00bf7a9271d5850e272bf4d2db11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:19:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 04:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 04:20:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:20:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 04:20:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 04:20:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:20:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:20:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 05:19:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 21:11:15 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 21:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 21:11:17 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 21:11:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 21:11:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:23:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 21:23:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:23:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 21:23:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 21:23:09 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 21:23:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 21:23:11 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 21:23:11 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 21:23:11 GMT
CMD ["php-fpm"]
# Sat, 17 Feb 2024 01:42:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sat, 17 Feb 2024 01:44:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2024 01:44:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Mar 2024 20:26:20 GMT
ENV MATOMO_VERSION=5.0.3
# Fri, 08 Mar 2024 20:26:51 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 20:26:54 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Fri, 08 Mar 2024 20:26:54 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Fri, 08 Mar 2024 20:26:56 GMT
VOLUME [/var/www/html]
# Fri, 08 Mar 2024 20:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 20:26:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388f1023e69b0297ca1b43f02b0de9f2700c16c9f3bc3cd4d532dce1fed98a82`  
		Last Modified: Tue, 13 Feb 2024 06:43:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c21152df6e3694f2bd61235e4c23ee7e24735cd91cfff9f6dca5abb307a801`  
		Last Modified: Tue, 13 Feb 2024 06:43:58 GMT  
		Size: 103.3 MB (103313095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0608cc469fd017def730be29629f988d7db21971cb60c627d4043f3f4ff24e3d`  
		Last Modified: Tue, 13 Feb 2024 06:43:40 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a203fd75ec04cbe787a887225043374015454791636c00611646d2a602a0d4c`  
		Last Modified: Fri, 16 Feb 2024 22:08:33 GMT  
		Size: 12.4 MB (12399429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526712d7b40a6d5cae9297f3090fe03b836cacbdd09d269e6dfa76960fda084d`  
		Last Modified: Fri, 16 Feb 2024 22:08:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c1e341e65653967dd13d0050a4e608e6a5a526f8573e80554115609d5d2500`  
		Last Modified: Fri, 16 Feb 2024 22:09:30 GMT  
		Size: 28.8 MB (28831186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba43a03a3435e7d6ec275628fd48fcddc2e440a08a4aecf402961fd1331beb03`  
		Last Modified: Fri, 16 Feb 2024 22:09:25 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144712d05cf3a83624bdc7acb8d984bfcc7b00ff7ead27628621f9ca46c448e1`  
		Last Modified: Fri, 16 Feb 2024 22:09:25 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf053640bd06d0f9c188b6def3991cc4da52ca4c4e35bf662617969241d74d`  
		Last Modified: Fri, 16 Feb 2024 22:09:25 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911fd4497513dced942732709f4823c4b79bab790615b01dfe2f418fb641d5e7`  
		Last Modified: Sat, 17 Feb 2024 01:55:56 GMT  
		Size: 3.4 MB (3350730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77cade2d8d60e8f93af14a03192e46de18fa6aade7df24ba4fbc814a89acbc`  
		Last Modified: Sat, 17 Feb 2024 01:55:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2915724765af615431380bb9ea459a2ec2aa75393793082f0c21b0e2c7b5e06a`  
		Last Modified: Fri, 08 Mar 2024 20:28:26 GMT  
		Size: 21.3 MB (21270635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c245c532262781f223b9695a0b9c01ae1e57962aaca285bd0a747dd985171ad6`  
		Last Modified: Fri, 08 Mar 2024 20:28:22 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f084a55f4838aef7f032acba387df732ca9208cad8d4e3458d35fcd4a5b68450`  
		Last Modified: Fri, 08 Mar 2024 20:28:21 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:5-fpm` - linux; s390x

```console
$ docker pull matomo@sha256:11fd9bc159f376615f3f3ebfd784262ef4fc9bc98d30a567b85f6d9441a8cec2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171669073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783351deec1f2e06848dd4cc23ab2e2037fa128732c7d6f07e24eae4f111c25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 05:08:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 05:08:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 05:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 05:09:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 05:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 05:09:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:09:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:09:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 06:22:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 22:06:37 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 22:06:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 22:06:37 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 22:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 22:06:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:16:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 22:16:53 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:16:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 22:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 22:16:54 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 22:16:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 22:16:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 22:16:55 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 22:16:55 GMT
CMD ["php-fpm"]
# Sat, 17 Feb 2024 03:14:06 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sat, 17 Feb 2024 03:15:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.23; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2024 03:15:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Mar 2024 20:04:28 GMT
ENV MATOMO_VERSION=5.0.3
# Fri, 08 Mar 2024 20:04:41 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 20:04:43 GMT
COPY file:f4ea35cff07e183c01b4e508329d1f5c342d9f4d330bda7f28faa530ced0d166 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Fri, 08 Mar 2024 20:04:43 GMT
COPY file:900c144bc42a0cece349bbd3acad78e18e4d9e022616b0b2897604ea1fa1c744 in /entrypoint.sh 
# Fri, 08 Mar 2024 20:04:43 GMT
VOLUME [/var/www/html]
# Fri, 08 Mar 2024 20:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 20:04:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db025363a3a1d7c6b99da4e14d1125b74c4b842740cab764d0f3f92123eda2ae`  
		Last Modified: Tue, 13 Feb 2024 08:11:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d7e20d739007df636f4e0bffb8c753fe34b5834c77a8560ad481209b713da9`  
		Last Modified: Tue, 13 Feb 2024 08:12:10 GMT  
		Size: 80.8 MB (80808538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231f09f66b39d784560a47b0a9a35c9ffc75c958ac6d714b931e2f10052eeccc`  
		Last Modified: Tue, 13 Feb 2024 08:11:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e3fe89b565c02dfa6816ccb2014c267550787688747263f24ff4429f3834e4`  
		Last Modified: Fri, 16 Feb 2024 23:21:50 GMT  
		Size: 12.4 MB (12398244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1c6b25716aca660c3d239245ebb6fe371aa5723bec8cb6da2e11e4c8cef68a`  
		Last Modified: Fri, 16 Feb 2024 23:21:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3a994334c2424ced39c6a5eae80fc7980478e7a217a072c033427f5f915f03`  
		Last Modified: Fri, 16 Feb 2024 23:22:21 GMT  
		Size: 26.7 MB (26706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8169e191cd1156ac06525d1a7ef0baf6a96ba5b0a6c036b0a184b8120070d5`  
		Last Modified: Fri, 16 Feb 2024 23:22:17 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c47b3037d6ab903e95d464fb0aba20b9acf3c02cf155ae6f90e14d781d5947`  
		Last Modified: Fri, 16 Feb 2024 23:22:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19163db2f08d5c74995e67f659dd374c9197af8aab0e19f5ea049090aae32bd2`  
		Last Modified: Fri, 16 Feb 2024 23:22:17 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c49023ed4e3fca6cb0932a5706c7210f3ff87721b1b135020f70aa2b1d5481`  
		Last Modified: Sat, 17 Feb 2024 03:27:59 GMT  
		Size: 3.0 MB (2983798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e5d2cf1cf5ec50f00bd4b86717816708dec2648959eea4ef72b72ee119d23`  
		Last Modified: Sat, 17 Feb 2024 03:27:59 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde01b1c51616854249a332837edce3ccf1c4df4b3d1c98e41566ea4be50f14c`  
		Last Modified: Fri, 08 Mar 2024 20:07:46 GMT  
		Size: 21.3 MB (21269470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efc2274dea3115e78691b37f543a3bdbd1e001a4925de60caafafde1139ef02`  
		Last Modified: Fri, 08 Mar 2024 20:07:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a625d273a5b147547d65e1c60db8c36ce4132f701d3ff63a0aa98533cbbc729d`  
		Last Modified: Fri, 08 Mar 2024 20:07:42 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
