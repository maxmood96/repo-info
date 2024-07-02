## `friendica:rc-fpm`

```console
$ docker pull friendica@sha256:b5ec264bd3b2c19dcca4cf9bb7fee73591d59f60a280b300797a8bef3b5f814f
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

### `friendica:rc-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:dbfec8be0a97abca270009023c4abd2eae2d134f13b96612b5e1575138818efa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214118496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f616e21c065e2b4dadf87bf7934e51d002303bd65c051ae162fc69c78e5ac358`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:25:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:25:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:25:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:25:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 04:21:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 04:21:11 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 04:21:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 04:21:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 04:21:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 04:21:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:31:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 04:31:01 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:31:02 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 04:31:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 04:31:02 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:31:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 04:31:03 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 04:31:03 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 04:31:03 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 07:19:13 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 07:19:14 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 07:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 07:22:02 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 07:22:02 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 07:22:02 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 07:22:03 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 07:22:03 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 07:22:03 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 07:24:05 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 07:24:05 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 07:24:11 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 07:24:11 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 07:24:11 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 07:24:11 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 07:24:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dbe43e30a1ec070f064e78ba481c34bcddadbad30a2204b3674f7551121b4e`  
		Last Modified: Tue, 02 Jul 2024 04:37:51 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759ee6bd3706c33b42cb784d34dec8a4eabbea15cfca2530b93bb24821b7adc1`  
		Last Modified: Tue, 02 Jul 2024 04:38:06 GMT  
		Size: 91.7 MB (91650270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3df42241e90d0821c6beaae0b632772ca7c45471efc1fd020bb51049f741038`  
		Last Modified: Tue, 02 Jul 2024 04:37:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459faeb9f9ff3e1c5b52defbeda8ec79c32f4679c116085172d9a98bcc2bd09b`  
		Last Modified: Tue, 02 Jul 2024 04:47:32 GMT  
		Size: 12.1 MB (12144733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d252436181f5104a1a896500cd8589a51587409f33b09f0455c3c7d8d3ee1d6`  
		Last Modified: Tue, 02 Jul 2024 04:47:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdf8be35eca58e8789ccd6b1c12005965e4bd35271c429accdea053e7b94cb5`  
		Last Modified: Tue, 02 Jul 2024 04:48:02 GMT  
		Size: 26.3 MB (26268222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30887d639de14cf7214dc1c77d1bf8ac82b9f729a68370872d8979ac20c586`  
		Last Modified: Tue, 02 Jul 2024 04:47:58 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8cfb6d7d892e835d8cb1bb4c02a8e3aadf66289a2b39d9e5dcda85a5132090`  
		Last Modified: Tue, 02 Jul 2024 04:47:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52adbbe8cd99e8e29b12c39b7304a32e933134e1070e845606141c671b5eb7c4`  
		Last Modified: Tue, 02 Jul 2024 04:47:58 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6356b09157fc0b839ef47335f600341713f5cf0d1c690a53a3dbd1ae23c49258`  
		Last Modified: Tue, 02 Jul 2024 07:24:51 GMT  
		Size: 15.6 MB (15607883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0b2c078331a9b0db8e917309af8f7cea663dfd8bc0484441bfdffd4d699614`  
		Last Modified: Tue, 02 Jul 2024 07:24:50 GMT  
		Size: 1.3 MB (1270291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e77ae8fa334c74350b726f42b051e5c46e7d720f93d7239e3b04f881229817`  
		Last Modified: Tue, 02 Jul 2024 07:24:50 GMT  
		Size: 18.3 MB (18321987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37507a3429509e4686987441eae4a84cf2a20134b28fa403bee0578c9376d55`  
		Last Modified: Tue, 02 Jul 2024 07:24:47 GMT  
		Size: 650.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3690381a068b246761e18fbac636cb75f25ae82f9779151a9904dd5fe4ae2f14`  
		Last Modified: Tue, 02 Jul 2024 07:26:28 GMT  
		Size: 17.4 MB (17414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5b12f64a212f97d7799f6131593b4ee0c3a3d76c6fce95ddddbf3a84c4e0a5`  
		Last Modified: Tue, 02 Jul 2024 07:26:26 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda13f9bf3fedc6dd9b54c1e0c13bafd914cd4f2b8524384fd42b2e65a63ab5f`  
		Last Modified: Tue, 02 Jul 2024 07:26:26 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:4de72e64457906f04aafaf5657942687a5b4762c556089644a3c28da075c8823
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189529661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d9b1d8c0ed382ec1e5b69803dba9da01d0b4febcf773909a8ca8838031e6cd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:43 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Tue, 02 Jul 2024 00:48:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:39:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:39:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:39:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:39:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:39:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:39:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:39:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:25:46 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 03:25:46 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 03:25:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 03:25:46 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 03:25:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 03:25:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:36:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:36:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:36:25 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:36:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:36:25 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:36:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 03:36:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 03:36:26 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 03:36:26 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 05:56:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 05:56:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 05:56:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 05:59:04 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:59:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 05:59:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 05:59:05 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 05:59:05 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 05:59:06 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 06:01:16 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 06:01:16 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 06:01:23 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 06:01:24 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 06:01:24 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 06:01:24 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 06:01:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:63678471745dce46512f823fc94716da7f08aa84c931dde61ae18c67b55c3085`  
		Last Modified: Tue, 02 Jul 2024 00:52:13 GMT  
		Size: 28.9 MB (28924714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ea1d136a0316c3c6cfab8ae6bb76454b8562314f8d7e552a5f06ba7d8d4fbe`  
		Last Modified: Tue, 02 Jul 2024 03:42:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cc766543faef6c79562d3f8d742bbb34bae433bdccfb9554ff78708c3b6637`  
		Last Modified: Tue, 02 Jul 2024 03:42:51 GMT  
		Size: 73.7 MB (73698312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1beb3b5ace36342878b3bf9adb858ec9286b901c9b292868aa0adc017dcfae2`  
		Last Modified: Tue, 02 Jul 2024 03:42:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d82b6a01790e0977063202174c6d75ff3527b032c3550a06969629f035ea4bd`  
		Last Modified: Tue, 02 Jul 2024 03:52:34 GMT  
		Size: 12.1 MB (12142933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b31b804a07c1c55cca801eef700e5a5ba313343e20786a0adb9fdc9108900`  
		Last Modified: Tue, 02 Jul 2024 03:52:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c2d5e428d62e2515f5880bc0544f13f4bab9ac9527162eba77d958944cf0f`  
		Last Modified: Tue, 02 Jul 2024 03:53:04 GMT  
		Size: 24.8 MB (24849351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51bfe08cdcf5682213f875cfb6726feb65f6cc5194a3a8accd51ed33f1989ce`  
		Last Modified: Tue, 02 Jul 2024 03:53:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88be603110f2097a4532ceb3f4729218f509ee48a7f1475facb246bd50d1c615`  
		Last Modified: Tue, 02 Jul 2024 03:53:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d528e86eaeda24a88ac21c0b50d3fde31e6f159793adb365f86e3833f221d8c`  
		Last Modified: Tue, 02 Jul 2024 03:53:00 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07ec9752bc08a4614817651481bb64eb2a1b1d1c5c266894c6423920d98d6c1`  
		Last Modified: Tue, 02 Jul 2024 06:01:59 GMT  
		Size: 15.5 MB (15501550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0cb22fcc632423147c3f0d4a338730fd03caa7e3050a5f47ee079046052c8c`  
		Last Modified: Tue, 02 Jul 2024 06:01:58 GMT  
		Size: 1.2 MB (1233247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fcb196910ed1d8129c2d8acbdfa3644d003bc56b91e0ea033869049c406079`  
		Last Modified: Tue, 02 Jul 2024 06:01:58 GMT  
		Size: 16.0 MB (15995149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febcf1b343f82a705648fed03a6b1734775ba0b4040dd305b1b8678f6d50330f`  
		Last Modified: Tue, 02 Jul 2024 06:01:56 GMT  
		Size: 650.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65f038ecb6c0f5eaa416cedff7375336be281724ad7d31a7d68982e26dfedff`  
		Last Modified: Tue, 02 Jul 2024 06:03:37 GMT  
		Size: 17.2 MB (17166498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d876cbf3bab09fe6374adedea1f9de3bf0c5f86564da137d63a1de9d5d2eb918`  
		Last Modified: Tue, 02 Jul 2024 06:03:36 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b079ed40d2366eca27769b3b74850f73327fdb49c7a373a094329c8dc6f44fa4`  
		Last Modified: Tue, 02 Jul 2024 06:03:36 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:e039f111f2408b51e6993144195ec6c6dd8e7007072615f9af7732a8cd36996d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180793881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf5d5c6e3c088cccf27699e703e21d04137dac16e6940c3afc2e1ec062cf6df`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:02:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:02:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:02:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:45:49 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 03:45:49 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 03:45:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 03:45:50 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 03:45:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 03:46:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:52:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:52:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:52:55 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:52:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:52:56 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:52:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 03:52:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 03:52:56 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 03:52:56 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 05:50:22 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 05:50:22 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 05:50:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 05:52:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:52:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 05:52:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 05:52:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 05:52:48 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 05:52:48 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 05:54:58 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 05:54:58 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 05:55:04 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 05:55:04 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 05:55:04 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 05:55:04 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 05:55:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169340bbc9b11466dc02ad185ab4ec5be5ae3f2d1bfadf025062aee784d7cf8`  
		Last Modified: Tue, 02 Jul 2024 03:58:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33cc5c115210ef3a85f7c10ea07381ce083592b603b1061dc201bea60ecafbd`  
		Last Modified: Tue, 02 Jul 2024 03:58:41 GMT  
		Size: 69.3 MB (69327786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fcbcd04aaf63c6b9ff83a247cf90682f60d62cabedfca5e92463f2e670db42`  
		Last Modified: Tue, 02 Jul 2024 03:58:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e552054ccd8cf87087227e6ce85dec6390d42dd34358d1ec9b10aa1cc5fcb8`  
		Last Modified: Tue, 02 Jul 2024 04:08:56 GMT  
		Size: 12.1 MB (12142942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac3f459bb1b6663d1017b4d172ee51caba2485eb11036f819d8efed56e8b549`  
		Last Modified: Tue, 02 Jul 2024 04:08:55 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4477e8ee91d4cd6e38461901de84d3fa298824fa5f5a9eb5f8820bd07a7042`  
		Last Modified: Tue, 02 Jul 2024 04:09:30 GMT  
		Size: 24.0 MB (24010312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e7dfed5209ee1669834651050c607ce9c6ff84e4df7e36f602890ce2aaecdd`  
		Last Modified: Tue, 02 Jul 2024 04:09:25 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90345b63f553885abacc8e25e5ce270ea0775775d6675a5e1f6b5f3c98e99741`  
		Last Modified: Tue, 02 Jul 2024 04:09:25 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167865caa99c33ea560df9694039e47bf224e751dedb24c3759de1686e32a41`  
		Last Modified: Tue, 02 Jul 2024 04:09:25 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b04b3017ba970f8ea0a9a62f9afc1144719e5caebf3f4c0e6eec016396356be`  
		Last Modified: Tue, 02 Jul 2024 05:55:41 GMT  
		Size: 15.6 MB (15573711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be8ba157726d968249645dbac4f8291d87558ae2c4e31437c6bcc33cf4958eb`  
		Last Modified: Tue, 02 Jul 2024 05:55:39 GMT  
		Size: 1.2 MB (1225160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba1e5cafd65ee212d2f20f56616688cc8e274e292f39e55d92b87a7ccba1ba`  
		Last Modified: Tue, 02 Jul 2024 05:55:39 GMT  
		Size: 14.9 MB (14867574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b268a405b5005b4e878d0c3f550b67075d866088d795522d43d5619d9cdd78d7`  
		Last Modified: Tue, 02 Jul 2024 05:55:37 GMT  
		Size: 649.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e91ab48492b39e6749432d84d94f83e728efd5966aa6ddd7b1969d5a5deb8c`  
		Last Modified: Tue, 02 Jul 2024 05:57:17 GMT  
		Size: 17.0 MB (17045795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e22d9ece9e08dbd9f9b71fc88a1e11ba563a94c010f55a88274d864f841e613`  
		Last Modified: Tue, 02 Jul 2024 05:57:15 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a945df6995a8a2db4c80b18ab541ca2d3e3fd1a3bdf55d609b903989b35c46ad`  
		Last Modified: Tue, 02 Jul 2024 05:57:15 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:21672d2d5b8cfe9c73e7ccb9193e119b70798432e85eb3448ce67b683c75c4b4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205793270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782b6d2c63a7b25a6a6dc3645300b9bdd19e351c28620a35c4421d5b2d112a0e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:33:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:33:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:34:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:34:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:22:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 03:22:22 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 03:22:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 03:22:22 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 03:22:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 03:22:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:31:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:31:24 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:31:24 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:31:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:31:24 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:31:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 03:31:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 03:31:25 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 03:31:25 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 06:40:19 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 06:40:19 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 06:40:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 06:43:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:43:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 06:43:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 06:43:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 06:43:06 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 06:43:07 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 06:44:50 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 06:44:50 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 06:44:54 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 06:44:55 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 06:44:55 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 06:44:55 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 06:44:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c335aec71aeb153fbea1427f7ea534c8097ca1898940f18317d638023574b8ee`  
		Last Modified: Tue, 02 Jul 2024 03:37:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bc195ca28e4f92808a4f6fd9b73331db6859db9e2ec74c189e231c415818e0`  
		Last Modified: Tue, 02 Jul 2024 03:38:01 GMT  
		Size: 86.9 MB (86939700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451e19963414458f43c8264137cea0d3aaaf9648417827bdcd7a2db62f7e0f89`  
		Last Modified: Tue, 02 Jul 2024 03:37:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb7a20e87aadcd261f19e011685a2b4550b64f1d37c21d63aba52853e42ee6b`  
		Last Modified: Tue, 02 Jul 2024 03:47:18 GMT  
		Size: 12.1 MB (12143874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62939dd17d3ce7a30cbe9e982e2f1bc0a9104225fb2479aa4001a474c119d2ee`  
		Last Modified: Tue, 02 Jul 2024 03:47:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569e5ef224370e4cde8cfdb822522b1acd50bb29cc3b913bd8e1b6b364936eca`  
		Last Modified: Tue, 02 Jul 2024 03:47:45 GMT  
		Size: 26.3 MB (26308828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea65559c6312fb3f4dc4e35c50763c600ab870243d7eddcaf8666c850d28a57d`  
		Last Modified: Tue, 02 Jul 2024 03:47:42 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb2f0ec5cb7247294d752168d5a5b797fb6537cea5ac66e24d621443d87275`  
		Last Modified: Tue, 02 Jul 2024 03:47:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2aff5fcc937a8fb7c2e2e0beb85845426d7a74725548a9ca6cc19d49b31ce7`  
		Last Modified: Tue, 02 Jul 2024 03:47:42 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a423d7ffa2a8b0ae51fc662807a02e53a9986432ddaa99aefaf31e7f023a1f`  
		Last Modified: Tue, 02 Jul 2024 06:45:33 GMT  
		Size: 15.4 MB (15369774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5abb1fcd4c069e5ba524b012582f3f2e66c4222d4f89f460c6cb66e15e6eccb`  
		Last Modified: Tue, 02 Jul 2024 06:45:32 GMT  
		Size: 1.2 MB (1197193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaa91d839cba5f2818c268c97de9f22598609b6f89a03efe0b0b4c1302c0b8c`  
		Last Modified: Tue, 02 Jul 2024 06:45:32 GMT  
		Size: 16.5 MB (16541440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dd4420fefea791e00f2a5e7ca4df782879b1f61833d87645533b545c1c7498`  
		Last Modified: Tue, 02 Jul 2024 06:45:30 GMT  
		Size: 649.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ccba2f0c7b0144eade4d32f553165e4a3d43b4850d5d13397c5364d56b837`  
		Last Modified: Tue, 02 Jul 2024 06:47:04 GMT  
		Size: 17.2 MB (17204939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4b945c5669fa471d87c58742c2cc19be98da93bea62786e1a26e254258a61e`  
		Last Modified: Tue, 02 Jul 2024 06:47:02 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d061e6a07c9e1dea6701826161d66622823d97296c9e96babc7952f5d11bb3`  
		Last Modified: Tue, 02 Jul 2024 06:47:02 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; 386

```console
$ docker pull friendica@sha256:ad7749356f2b7fcd90c772babc30ca582866c8e3c3c739ce59f850b7452333e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217105259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d2a274230cb1ba77b0adb29e67725bdf3d70595de310aa573b3256111c7730`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:08:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:08:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:08:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:08:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:08:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 05:16:07 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 05:16:07 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 05:16:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 05:16:07 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 05:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 05:16:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 05:31:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:31:49 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 05:31:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 05:31:50 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 05:31:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 05:31:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 05:31:50 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 05:31:51 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 06:12:11 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 06:12:12 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 06:12:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 06:15:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:15:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 06:15:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 06:15:23 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 06:15:24 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 06:15:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 06:17:36 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 06:17:36 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 06:17:42 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 06:17:42 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 06:17:43 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 06:17:43 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 06:17:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ab6efef12df0de52bf9e83bb54eeb04b25e4bddee111bb8de64345305496a`  
		Last Modified: Tue, 02 Jul 2024 05:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90549434c6bff14f52cbc9958e76ddae4f172308e4aba9cdcc10c126accc3b94`  
		Last Modified: Tue, 02 Jul 2024 05:41:16 GMT  
		Size: 92.7 MB (92720434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e55f446fcc5301935ef2eed4717ce1921ca07f5b60bea264e88372cd08c54e8`  
		Last Modified: Tue, 02 Jul 2024 05:40:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde80b8650e1e00ff69b0d3f63377257c749a5a5489c71ffda250d151c4b1539`  
		Last Modified: Tue, 02 Jul 2024 05:51:49 GMT  
		Size: 12.1 MB (12143816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ca7aaf31715261ada50abb6057351749afcca8222f0ae1d0c1a69627d3ff4`  
		Last Modified: Tue, 02 Jul 2024 05:51:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a81ab8a7e9383a42d97538dd96f5cda5e07d27430e75b6aa56d9986fa8bf6`  
		Last Modified: Tue, 02 Jul 2024 05:52:23 GMT  
		Size: 26.8 MB (26751090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f17ea877dc9edb44b48dade74f11700c5bd5be76024635f0f506e67f4fd7dfe`  
		Last Modified: Tue, 02 Jul 2024 05:52:18 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662e0c1614c805ddaaf7a7777ca9bf85eb8ec0aae6224e663aa3d6dc24756050`  
		Last Modified: Tue, 02 Jul 2024 05:52:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04497c9348332751ee859b8e5d26d35029bb1bb38dc9d654d6555b9e8174b0d2`  
		Last Modified: Tue, 02 Jul 2024 05:52:18 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aa3d2a98a29a873874b6764f8351b7e3800af714ec3f586d2551d683a22b1b`  
		Last Modified: Tue, 02 Jul 2024 06:18:26 GMT  
		Size: 16.1 MB (16076781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8017ef491bfb961982b4c4b2cad7cb2d343cf19d8b7b696fdb7ace45ae3749`  
		Last Modified: Tue, 02 Jul 2024 06:18:24 GMT  
		Size: 1.2 MB (1236665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a7375a7d4e5c3266baeaa20fe50b7875a9650674612e620e253f1b90ff3356`  
		Last Modified: Tue, 02 Jul 2024 06:18:27 GMT  
		Size: 17.6 MB (17583748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6975def6883acb65742ad51e8bea803bc02de3b920a635b50d6629a3cd9ad2f5`  
		Last Modified: Tue, 02 Jul 2024 06:18:22 GMT  
		Size: 647.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3731053854f16edaf067fc6ca6af2f54a017c2a4769ac95c56a32a06415b5d`  
		Last Modified: Tue, 02 Jul 2024 06:20:17 GMT  
		Size: 18.2 MB (18166365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33bcae1f4c6c3cae301261a71d9833fb4e0af6b5a2ecd1c5f77dd28abddc9e7`  
		Last Modified: Tue, 02 Jul 2024 06:20:15 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6ce0bf63ec596c3fe2696f3c82b4e2ac8d940e0ab9b2978f60158755621f35`  
		Last Modified: Tue, 02 Jul 2024 06:20:15 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:221d1d1ca2b41af75c01af9c0a908361735eabba67ad0deabc73f871b716bbe5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187202896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c564c64745ee339d2babd215bf8fb4f8415bc7a28f1f148dea48b0e8eef2046d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Jun 2024 01:11:51 GMT
ADD file:008c77755df91bc808f2edbc05df1da6419d984abea862dbf73f345500433eb9 in / 
# Thu, 13 Jun 2024 01:11:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:46:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 05:46:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 05:48:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 05:48:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 05:48:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 05:48:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 05:48:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 05:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 09:56:48 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 13 Jun 2024 09:56:52 GMT
ENV PHP_VERSION=8.1.29
# Thu, 13 Jun 2024 09:56:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 13 Jun 2024 09:57:00 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 13 Jun 2024 09:57:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 09:57:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 10:39:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 10:39:59 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 13 Jun 2024 10:40:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 10:40:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 10:40:14 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 10:40:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 13 Jun 2024 10:40:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Jun 2024 10:40:29 GMT
EXPOSE 9000
# Thu, 13 Jun 2024 10:40:34 GMT
CMD ["php-fpm"]
# Thu, 13 Jun 2024 11:42:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Thu, 13 Jun 2024 11:42:42 GMT
ENV GOSU_VERSION=1.14
# Thu, 13 Jun 2024 11:43:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 13 Jun 2024 11:55:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 11:55:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 13 Jun 2024 11:55:22 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 13 Jun 2024 11:55:29 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 13 Jun 2024 11:55:33 GMT
VOLUME [/var/www/html]
# Thu, 13 Jun 2024 11:55:37 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 01 Jul 2024 18:30:36 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Mon, 01 Jul 2024 18:30:40 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Mon, 01 Jul 2024 18:31:13 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Mon, 01 Jul 2024 18:31:18 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Mon, 01 Jul 2024 18:31:22 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 01 Jul 2024 18:31:26 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 01 Jul 2024 18:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1b4876387959ae765d8f504e4352c8f85ce0ad5a78eee29be84300f85cfdf0a6`  
		Last Modified: Thu, 13 Jun 2024 01:23:19 GMT  
		Size: 29.7 MB (29651863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cd14a0602be197a130631abd6193db688c08cff687fd6159fce9c30a9ee18d`  
		Last Modified: Thu, 13 Jun 2024 10:59:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0e8cf4cac25cd6bce3fe4ed647b522db5ebb90f87e58a2de080506ee2c54a9`  
		Last Modified: Thu, 13 Jun 2024 11:00:29 GMT  
		Size: 71.8 MB (71817675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fc0d6906236331e4f9504ad6898fe912b9fe9526132c44bf5e1f0033de422a`  
		Last Modified: Thu, 13 Jun 2024 10:59:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5c1cf6190c2ec903270a337dbbdf9a51baf1afcc14d7c85ad5ebe8d69645e9`  
		Last Modified: Thu, 13 Jun 2024 11:08:56 GMT  
		Size: 11.9 MB (11926954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bac40718cff4eeddfdbba005eb3d39deb873b921f770ecfef1fa44325243a85`  
		Last Modified: Thu, 13 Jun 2024 11:08:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bbeb5e173de950fde267774a65916a84271283938574c3e82e21c075e99102`  
		Last Modified: Thu, 13 Jun 2024 11:10:01 GMT  
		Size: 25.3 MB (25271033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e7bbc3412dfacb53c479f4d672d5a5bfd91adb90d33a4d77951d39761aead8`  
		Last Modified: Thu, 13 Jun 2024 11:09:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad46f56294a585631ea71b51a5b525bc91f1b35a8a88d5a4b934eb1436c9f2a6`  
		Last Modified: Thu, 13 Jun 2024 11:09:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e02f8f5a95757cf10f06c65196d4b8d25494c5dac591627d0fecd729fa2f0`  
		Last Modified: Thu, 13 Jun 2024 11:09:45 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f27261f3c823348a95fb0bddf4f15416662bc33b11f6ca3ba2a2946508c3b63`  
		Last Modified: Thu, 13 Jun 2024 12:05:55 GMT  
		Size: 15.1 MB (15068630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30a951c997e38d85097059dc57bef97e39bb1a2c0e53398214a9810c60b486`  
		Last Modified: Thu, 13 Jun 2024 12:05:48 GMT  
		Size: 920.9 KB (920880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba13963e13b99249a1346a77eda11a18b89fb7423e203d0d0dd9fff051383ebe`  
		Last Modified: Thu, 13 Jun 2024 12:05:56 GMT  
		Size: 15.8 MB (15844481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ace99bc89c6fa5c673790fa68aadec921e351b277749fa987a9ab32141e7a48`  
		Last Modified: Thu, 13 Jun 2024 12:05:44 GMT  
		Size: 650.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4e7f02235b4100b965d5f68c5692cda222c13aefac051175570a4c93b289b9`  
		Last Modified: Mon, 01 Jul 2024 18:32:40 GMT  
		Size: 16.7 MB (16683462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7939ba88dee658dc6832725d01aabdd5bef29a99d5802263847ec5671aadae83`  
		Last Modified: Mon, 01 Jul 2024 18:32:33 GMT  
		Size: 3.8 KB (3815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b9474d78442665aeadcda4a417bb1415f0d0e910a999e0e7153f9a54833257`  
		Last Modified: Mon, 01 Jul 2024 18:32:33 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:c8078a6bde0575e124b85b2e65feb8b05463e2b68b120411d946d6c24b6fdbdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213632826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73a22ccd0199bba2891236a43a52dab2b2462f436d513b6ba4935c066038c7a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:03 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Tue, 02 Jul 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:24:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:24:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:24:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:24:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:24:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:24:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:24:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:24:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 04:01:19 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 04:01:19 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 04:01:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 04:01:20 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 04:01:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 04:01:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:09:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 04:09:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:09:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 04:09:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 04:09:53 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:09:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 04:09:54 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 04:09:55 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 04:09:55 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 05:15:26 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 05:15:27 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 05:15:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 05:18:57 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:18:58 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 05:18:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 05:19:00 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 05:19:00 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 05:19:00 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 05:21:49 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 05:21:49 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 05:21:58 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 05:21:59 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 05:21:59 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 05:22:00 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 05:22:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339f489d1e564c9c7d91a1bafdbd753bea976cf7d4e49aac09781b3a7179dffa`  
		Last Modified: Tue, 02 Jul 2024 04:16:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c23a5c69cce13d9ff3aa0ee9590ebb9a7850465f19d2721100e288312e7b9`  
		Last Modified: Tue, 02 Jul 2024 04:16:31 GMT  
		Size: 86.6 MB (86647997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4efbc073f0d2c267667e6f9fa4d3a5d430b0c9e921cd8823dc6cd7b4d22002d`  
		Last Modified: Tue, 02 Jul 2024 04:16:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f85cefbcfb0b27972af7851d51892f4ccfdfe799e7f1b7deb55d4ecd6f7544`  
		Last Modified: Tue, 02 Jul 2024 04:26:28 GMT  
		Size: 12.1 MB (12144473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6849d72f9d743706fde7f56714c296fede840e94ee51a3fffea659a84d7b3446`  
		Last Modified: Tue, 02 Jul 2024 04:26:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19d61c4740b4ad848e208588820fef25e4694eb5e4b711ec33236b107b37278`  
		Last Modified: Tue, 02 Jul 2024 04:26:59 GMT  
		Size: 27.3 MB (27300138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5055ee059199f1b050bdf0621b46079e03edd209a2556c5f926230676e761`  
		Last Modified: Tue, 02 Jul 2024 04:26:54 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f46afe08a91a51ba3ef32d13777ec8d40cb6b7405a5f020e5d9944ea9f8fc7a`  
		Last Modified: Tue, 02 Jul 2024 04:26:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07784a8561236883d5e57663bc65c3e5ef5662a28e9c3c7f42c6543b24b12b55`  
		Last Modified: Tue, 02 Jul 2024 04:26:54 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3725db6d7c157bc51b6bbf3bbcf0d1b8337899e2dc829b7c4df9696a433c83e7`  
		Last Modified: Tue, 02 Jul 2024 05:22:37 GMT  
		Size: 15.5 MB (15498591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1771831504ce50bb90b1c330d0477ceb1724f9a783b1da049df1877b17194fed`  
		Last Modified: Tue, 02 Jul 2024 05:22:36 GMT  
		Size: 1.2 MB (1169069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0151779c03bf3abd1e1536e588809351def46dadc4124296261add2fc7e65`  
		Last Modified: Tue, 02 Jul 2024 05:22:36 GMT  
		Size: 17.8 MB (17806683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f83bad5c6e5e1a8976b0afa8ec656813e4950eb2d72f64f7ba8f95e045a21`  
		Last Modified: Tue, 02 Jul 2024 05:22:33 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a150073095ac47fe1dc649ac0f2226ae3a1b6740770037e440dc46dc90d39ad`  
		Last Modified: Tue, 02 Jul 2024 05:24:12 GMT  
		Size: 17.7 MB (17748770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcccdb0691cf752c1b980424bc2c4fb15c11a5546c73db60f6b94d4710ea410a`  
		Last Modified: Tue, 02 Jul 2024 05:24:10 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6aa9f5d4ec7ee71fb9d83b8ebd10b5562e89fe2a6af1ca5e5b68d08c4be0a9`  
		Last Modified: Tue, 02 Jul 2024 05:24:10 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:4fa2951eedf6783d8b9823f3a456f4412a736c4f8c184b06e8897f397b922a66
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187847809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea114516f7a6fd28a1f6fd4b1f7a0828027d1a6dcd73ea351bab8efa623a882`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:26:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:26:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:26:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:26:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:26:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:52:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 02:52:51 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 02:52:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 02:52:51 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 02:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:52:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:59:40 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:59:41 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:59:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:59:41 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 02:59:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 02:59:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 02:59:42 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 02:59:42 GMT
CMD ["php-fpm"]
# Tue, 02 Jul 2024 04:38:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Tue, 02 Jul 2024 04:38:32 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Jul 2024 04:38:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Jul 2024 04:40:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 02 Jul 2024 04:40:11 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 02 Jul 2024 04:40:11 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jul 2024 04:40:11 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 04:40:11 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 02 Jul 2024 04:42:39 GMT
ENV FRIENDICA_VERSION=2024.06-rc
# Tue, 02 Jul 2024 04:42:39 GMT
ENV FRIENDICA_ADDONS=2024.06-rc
# Tue, 02 Jul 2024 04:42:44 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Tue, 02 Jul 2024 04:42:44 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Tue, 02 Jul 2024 04:42:44 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Tue, 02 Jul 2024 04:42:44 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jul 2024 04:42:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17d7bf4982e21c3386b6bdf8634c3d59503cac65f62f788141a1b7410b7dae4`  
		Last Modified: Tue, 02 Jul 2024 03:06:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f9558ba7962aecc1f4c8fdf9a69dc59140624ff107a83d97ca9b2f2ea5f64`  
		Last Modified: Tue, 02 Jul 2024 03:06:19 GMT  
		Size: 71.6 MB (71641635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740b856ce936618b60f15e78d2808c90765f0df4fce2766a82eea320ba3d832f`  
		Last Modified: Tue, 02 Jul 2024 03:06:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca83ab7fa72080a19e9d28835daad086766515b54ec0fb988da389329701dd6`  
		Last Modified: Tue, 02 Jul 2024 03:13:57 GMT  
		Size: 12.1 MB (12143357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5e640371c9ba5b049a8c1907ab779a564b046d051c56d8ae9ee36c5e1f2f9b`  
		Last Modified: Tue, 02 Jul 2024 03:13:56 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f24a430727d4f150e401895f613da9821c149a0cc5f0b992a92cb95a7039a2`  
		Last Modified: Tue, 02 Jul 2024 03:14:22 GMT  
		Size: 25.5 MB (25494032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c377b214bba51835bfe09a7b2fd61a4261956a5e678f6ea33b6644c07b24eccc`  
		Last Modified: Tue, 02 Jul 2024 03:14:18 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5696806241ea3ab65ba9dad95a3a26033b688174b82b536891e6790702caa94`  
		Last Modified: Tue, 02 Jul 2024 03:14:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d787499947daa3ee26ee2edaa7b6f1426162d0cffb891dd4cdf5fe1f6046748`  
		Last Modified: Tue, 02 Jul 2024 03:14:18 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71251697b26cd893036616f2b5acb010651f227e7ce6215fa939bbb9f1d0bbf5`  
		Last Modified: Tue, 02 Jul 2024 04:43:24 GMT  
		Size: 15.0 MB (15005209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3c1d260d04758287613a74eb627b94afecff5332de7cd40e4cd41c60935568`  
		Last Modified: Tue, 02 Jul 2024 04:43:23 GMT  
		Size: 1.2 MB (1232193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78e3dbf27889ef1a9dc51cac3d51c4fb6d08916d234cd0565a2e88db58a2321`  
		Last Modified: Tue, 02 Jul 2024 04:43:24 GMT  
		Size: 15.9 MB (15884555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd64456900f7b1de41517094e27530909a33b3de62aecb99e248b649e2af42e`  
		Last Modified: Tue, 02 Jul 2024 04:43:22 GMT  
		Size: 649.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e255330ff10a04c1a3b6cdbdd7b157523dc9d3c0b86e53893b6554376091595`  
		Last Modified: Tue, 02 Jul 2024 04:44:35 GMT  
		Size: 16.8 MB (16766573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee86681e93fb595021657ec98a913872dd64ea682ef82dd73826d3b43d05ca`  
		Last Modified: Tue, 02 Jul 2024 04:44:33 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e3f918036faab7b3703ac80ed8dd171187dc0989e5a540944f466e238487d6`  
		Last Modified: Tue, 02 Jul 2024 04:44:33 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
