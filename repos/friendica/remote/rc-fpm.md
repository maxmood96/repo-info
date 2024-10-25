## `friendica:rc-fpm`

```console
$ docker pull friendica@sha256:9d884af9ab7d509257e9748a49f49ddc1f82ae8da4b5c787a3a5fbc175f6967f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `friendica:rc-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:57bb103497bee7102c8e5cb36b28d7198501a4951cff27657b6edd8720a190c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215252126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e23621204226b2dc706e12f7374f98917a082fabdc73996fd57f672ce2fdf92`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:33:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:34:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:34:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:34:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:34:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:34:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:04:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:28:35 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:28:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:28:35 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:28:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:28:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:38:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:38:29 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:38:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:38:30 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:38:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 01:38:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 01:38:31 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 01:38:31 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 04:13:28 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 25 Oct 2024 04:13:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:13:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Oct 2024 04:16:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:16:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 25 Oct 2024 04:16:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 04:16:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 25 Oct 2024 04:16:21 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 04:16:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 25 Oct 2024 04:19:35 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Fri, 25 Oct 2024 04:19:36 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Fri, 25 Oct 2024 04:19:41 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 25 Oct 2024 04:19:41 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 25 Oct 2024 04:19:41 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 25 Oct 2024 04:19:41 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 25 Oct 2024 04:19:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbbd15f347bcdafcf64d35ef1d5188d26e93dbd1a9f6c597aadb9d73c5e4bf1`  
		Last Modified: Thu, 17 Oct 2024 04:20:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf5a80d2887f3525d056883d0933bb421e308d260def97abcc7866e92b74fef`  
		Last Modified: Thu, 17 Oct 2024 04:20:33 GMT  
		Size: 91.6 MB (91648779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e1925177bb647010bddc6c584e5d4a7ff00063fdc8b64ed1bb82c45aa4fc74`  
		Last Modified: Thu, 17 Oct 2024 04:20:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6055f17a9cccd1f1796a14b107b2e33b11ee5e722dadfcb7fb52e9f76a766152`  
		Last Modified: Fri, 25 Oct 2024 02:20:07 GMT  
		Size: 12.4 MB (12444816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c380f63c6af64d2d0774db115324fdc711206d4cefb41b15b242c3bec91b9ed7`  
		Last Modified: Fri, 25 Oct 2024 02:20:06 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea4bebd6c024e3d9a093f8c776e485c97b94831ff8693a5c79b415e7a3c5edc`  
		Last Modified: Fri, 25 Oct 2024 02:20:41 GMT  
		Size: 26.5 MB (26528075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b9c11d56535776eb1882b5f69237371358b51640c8026cd317acfd65d43664`  
		Last Modified: Fri, 25 Oct 2024 02:20:37 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dbdd44cd37bd53681a1e47e51b49535f744e28f8802b8cfec7c5b08b49caec`  
		Last Modified: Fri, 25 Oct 2024 02:20:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c47a86d15a2565898043b4b85c72cecbca3cdffca2b6b7d4f889bdfe2eb7c7`  
		Last Modified: Fri, 25 Oct 2024 02:20:37 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c177cf82d7bf3fd052ce9c210ea1e04e51f3c72c708e2efa4f326a708fafeb3a`  
		Last Modified: Fri, 25 Oct 2024 04:20:24 GMT  
		Size: 15.7 MB (15650803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ada2dd368515b845ac21e7be95c86269401d2baab6ab1adeffc655bab14e5d2`  
		Last Modified: Fri, 25 Oct 2024 04:20:23 GMT  
		Size: 1.3 MB (1323179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0eee669ea252ebb724024c61623bc9d6258d74ea9371f23362fae6f5a42221`  
		Last Modified: Fri, 25 Oct 2024 04:20:24 GMT  
		Size: 18.8 MB (18751118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb98f798315075ecf6c29d9a0dfbfd544da35f8fa282c3e5cddd4923454fcd`  
		Last Modified: Fri, 25 Oct 2024 04:20:21 GMT  
		Size: 646.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f3b2f2fe05f576a4763b76e44b59955e7ece4b347efedab7c179ea73e801b8`  
		Last Modified: Fri, 25 Oct 2024 04:21:00 GMT  
		Size: 17.5 MB (17458355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751f92549ff2a663d0255bb0a5e9e0e7909092ceccbe678cb1e92b9aa446633c`  
		Last Modified: Fri, 25 Oct 2024 04:20:59 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aa667aa4e2e64db817d64ec973b6dfcaed7e258c42fd85230c2084e62999ad`  
		Last Modified: Fri, 25 Oct 2024 04:20:59 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:bfa5a382ade98a78f6fbcd51a6408504cca8bf246b2d91501c57efbe4a42073a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181874618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165de69ebd061f0251ffe72589d1a5ce57a8808c51fcc09849fd2c3b5b9aa14e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:45 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 17 Oct 2024 03:03:46 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:56:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 03:56:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 03:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:57:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 03:57:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 03:57:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:57:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:57:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 05:04:11 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:58:56 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:58:56 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:59:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:06:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 02:06:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:06:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 02:06:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 02:06:52 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 02:06:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 02:06:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 02:06:53 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 02:06:53 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 04:01:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 25 Oct 2024 04:01:16 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:01:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Oct 2024 04:03:42 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:03:43 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 25 Oct 2024 04:03:43 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 04:03:43 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 25 Oct 2024 04:03:43 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 04:03:43 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 25 Oct 2024 04:06:50 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Fri, 25 Oct 2024 04:06:51 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Fri, 25 Oct 2024 04:06:56 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 25 Oct 2024 04:06:56 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 25 Oct 2024 04:06:56 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 25 Oct 2024 04:06:56 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 25 Oct 2024 04:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0606d2c81db30773bad8bfc0fe9de13c273ca378969df520e2bcc097e2b1c968`  
		Last Modified: Thu, 17 Oct 2024 06:01:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0bc221353bad7dcb9a35d25b7e0366d8b7ad0b5800ee681486a49f010ab9b6`  
		Last Modified: Thu, 17 Oct 2024 06:02:00 GMT  
		Size: 69.3 MB (69327127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ec6f0f820288d353259f98dd4661bcfda8c6acdfb31275dde353487d6e9e3`  
		Last Modified: Thu, 17 Oct 2024 06:01:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b3c97a57fddb8d8753b4c3a370822f59d0137220b431e81553dc14a5590bd`  
		Last Modified: Fri, 25 Oct 2024 02:41:00 GMT  
		Size: 12.4 MB (12443221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f965a3451c7d88e27ee5757899207a9bd0d4a92af5786df4123ea4a77dd482`  
		Last Modified: Fri, 25 Oct 2024 02:40:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6019ef74fee4eb461e5a7a8f25c9c77e5ab2f717a00c4ac9e77b4d0d1b13f643`  
		Last Modified: Fri, 25 Oct 2024 02:41:32 GMT  
		Size: 24.2 MB (24247477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740388c0a246c776e1abb4b41d5881c8f19722d96539b86603474997be39bc48`  
		Last Modified: Fri, 25 Oct 2024 02:41:27 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2be12fc16a45fa4fed8a1306f380dff66e5c1f2c58eedc7201132a67ccb544c`  
		Last Modified: Fri, 25 Oct 2024 02:41:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adca13fdd70096a09f9417cc5ccf5d6d106d9705a1e673e6e8fce6a838cbb85d`  
		Last Modified: Fri, 25 Oct 2024 02:41:27 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac9d347757824bdd9b34c742895c318f3419a819c89c25af4c41304e179a8f1`  
		Last Modified: Fri, 25 Oct 2024 04:07:40 GMT  
		Size: 15.6 MB (15610126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b37128793036cf7f21da09333a99b7b06dae9c01e42d4e5ae86129b3b3f1e9`  
		Last Modified: Fri, 25 Oct 2024 04:07:39 GMT  
		Size: 1.3 MB (1289672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7494882e3663427e76704e4a9a308502a7bc3692417b42688c47a34a2f1dc813`  
		Last Modified: Fri, 25 Oct 2024 04:07:39 GMT  
		Size: 15.3 MB (15265305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c30894aab41b3c4ceba8f6b9fb764bf7b3110f3e54de47f53022fb2d289a5d4`  
		Last Modified: Fri, 25 Oct 2024 04:07:36 GMT  
		Size: 652.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6b91ce2b4b373465b5881f3383e836992da2cbcd1b4d67e24f0218ef1d14b6`  
		Last Modified: Fri, 25 Oct 2024 04:08:16 GMT  
		Size: 17.1 MB (17083921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28d3a0752d81922e06015145116e6a6d39793515e87aece2f7471f81f1afb02`  
		Last Modified: Fri, 25 Oct 2024 04:08:15 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c97c81c21023e0e0d32a9ebcdd18e373d52355c7502a7694138525bc3eb31f3`  
		Last Modified: Fri, 25 Oct 2024 04:08:15 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:51be8bee694edf23284bfe97801170a15b8ddd5b5f3caf553a94eb51ac0657f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206959896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40d9295156760597fd6b59d7799021fb1e212983a3820a7c4902317b43a8892`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:48:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:48:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:48:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:48:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:10:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:34:11 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:34:11 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:34:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:43:13 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:43:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:43:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:43:14 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:43:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 01:43:14 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 01:43:14 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 01:43:15 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 02:44:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 25 Oct 2024 02:44:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 02:44:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Oct 2024 02:46:50 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 02:46:50 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 25 Oct 2024 02:46:50 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 02:46:50 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 25 Oct 2024 02:46:50 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 02:46:51 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 25 Oct 2024 02:50:38 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Fri, 25 Oct 2024 02:50:38 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Fri, 25 Oct 2024 02:50:42 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 25 Oct 2024 02:50:42 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 25 Oct 2024 02:50:42 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 25 Oct 2024 02:50:42 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 25 Oct 2024 02:50:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace9636e6938c06012e872f575501cde8bf2eca9acb98f854f4751aa1514dd9`  
		Last Modified: Thu, 17 Oct 2024 04:18:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7171c8bb99efea9002d518bf04cebb687c75638eefbe3666e14777dc886ef464`  
		Last Modified: Thu, 17 Oct 2024 04:18:41 GMT  
		Size: 86.9 MB (86938384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b149e2ef200eac8e6802701c011653731e4d39d82222744d140dc44a7887836e`  
		Last Modified: Thu, 17 Oct 2024 04:18:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d2b7c2372c36fc72653107301cac43eb002d03f03d53fbc1066239d830b1ee`  
		Last Modified: Fri, 25 Oct 2024 02:22:56 GMT  
		Size: 12.4 MB (12444012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16ee8312616c4172b6dcdf8512a7a0c4d6e599174e41db908043520dab8d5a7`  
		Last Modified: Fri, 25 Oct 2024 02:22:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3ae20e12a9f19b7eb871a8afd3397bfc6de2e71b1efda8604ca3e023d30d0`  
		Last Modified: Fri, 25 Oct 2024 02:23:25 GMT  
		Size: 26.6 MB (26584581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e8463ac3d43dcb14d79583b38028cb50def789d4381af85abac01b676b637`  
		Last Modified: Fri, 25 Oct 2024 02:23:22 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55358f8cda3524b55f452fe9dc8724dddcc31412e25e648e2a4f5864b94639e3`  
		Last Modified: Fri, 25 Oct 2024 02:23:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98ae2dbeee567ebf2e37bab5d55e2510dd9b5dba579983785496886513b06b7`  
		Last Modified: Fri, 25 Oct 2024 02:23:22 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c67c5716a1d096bf861c6da46df87f470e8551d1d133164f91b165d60d463fd`  
		Last Modified: Fri, 25 Oct 2024 02:51:23 GMT  
		Size: 15.4 MB (15412160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d0f8ea363d7bad64e32f93332322d04f26b1d398b50eaaca5d6bfcfa80c58a`  
		Last Modified: Fri, 25 Oct 2024 02:51:22 GMT  
		Size: 1.3 MB (1254476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9f3749100a462631fc7247f629ba2e95db524e1c86c7d694240150f021a05`  
		Last Modified: Fri, 25 Oct 2024 02:51:22 GMT  
		Size: 17.0 MB (16984159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7daeb78fb3848c5959dab4fab0607320009878b54a18f56fed05f32095cf9a8`  
		Last Modified: Fri, 25 Oct 2024 02:51:20 GMT  
		Size: 651.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be975476211676743ccae31ad804b8ecdd5c3e1109f5e3d0b1d1f9a0410b1a7e`  
		Last Modified: Fri, 25 Oct 2024 02:52:01 GMT  
		Size: 17.2 MB (17248152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62d2b65beafa73b2f874a519faa301be44729bca2f4df0cde77c83418496dc4`  
		Last Modified: Fri, 25 Oct 2024 02:52:00 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e16691ddd56bb238b917a0db0cdd6fe4d5b18a7d8784c4f9bd02883e03bc8a8`  
		Last Modified: Fri, 25 Oct 2024 02:52:00 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm` - linux; 386

```console
$ docker pull friendica@sha256:f9a6bd2b75f6fe947ad596c0b3f5bc13f4d2fe3b4ca3379ae56701b40bdc727d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217922444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553ebe5988ca4d16044f89b169c2c42a8ee26b98ba0b83c1bc411909cf4564f7`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:19 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 17 Oct 2024 00:39:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:43:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:43:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:43:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:43:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:43:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:43:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:43:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 04:10:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 04:56:59 GMT
ENV PHP_VERSION=8.2.24
# Thu, 17 Oct 2024 04:56:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 17 Oct 2024 04:56:59 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 17 Oct 2024 04:57:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 04:57:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:12:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 05:12:50 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:12:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 05:12:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 05:12:51 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 05:12:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 17 Oct 2024 05:12:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Oct 2024 05:12:52 GMT
EXPOSE 9000
# Thu, 17 Oct 2024 05:12:52 GMT
CMD ["php-fpm"]
# Thu, 17 Oct 2024 08:23:49 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 18 Oct 2024 18:42:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 18 Oct 2024 18:42:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Oct 2024 18:45:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 18 Oct 2024 18:45:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Oct 2024 18:45:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Oct 2024 18:45:18 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 18 Oct 2024 18:45:18 GMT
VOLUME [/var/www/html]
# Fri, 18 Oct 2024 18:45:18 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 18 Oct 2024 18:49:03 GMT
ENV FRIENDICA_VERSION=2024.09-rc
# Fri, 18 Oct 2024 18:49:03 GMT
ENV FRIENDICA_ADDONS=2024.09-rc
# Fri, 18 Oct 2024 18:49:10 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 18 Oct 2024 18:49:10 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 18 Oct 2024 18:49:11 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 18 Oct 2024 18:49:11 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 18 Oct 2024 18:49:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43260051671f41da7ac3074533520d1adf3836622787931130d47b36ccc9c71`  
		Last Modified: Thu, 17 Oct 2024 06:08:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2d6fb54fdb4ca9247c69c301328a0648364b4ce3458fcc483de830da5d8ae`  
		Last Modified: Thu, 17 Oct 2024 06:09:18 GMT  
		Size: 92.7 MB (92720839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f93045a988ea98d726109dd89f4e5a35696e290cd4b976ceb78578f11d12fa`  
		Last Modified: Thu, 17 Oct 2024 06:08:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb77d1075f3a197c67c7eadac248ab87b6c2b7270e93106cfe36248d522f6b54`  
		Last Modified: Thu, 17 Oct 2024 06:19:31 GMT  
		Size: 12.4 MB (12428172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2446a83e35347115d9dd33c5a70b14fbb6fd866983c83da8a81ddcc8fd03c08`  
		Last Modified: Thu, 17 Oct 2024 06:19:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1655f78455ce7043769639706099454a1cc78336a7066b1a6756dedba3fdd46`  
		Last Modified: Thu, 17 Oct 2024 06:20:04 GMT  
		Size: 27.0 MB (27025842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff22b44cb0f6ed66bba3ab8ae9124caddbf0e253be48b6fdfc0852ba98bd5b1b`  
		Last Modified: Thu, 17 Oct 2024 06:19:58 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5150e7cae1db8637de4a3be9a6f46a8bcb750f11336a436229ff0d1db3e93cdf`  
		Last Modified: Thu, 17 Oct 2024 06:19:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb289970f9daf54a8a073dd082de51c09a16dfbf385c8070aaf295505e01ea91`  
		Last Modified: Thu, 17 Oct 2024 06:19:58 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32665b8ae756439e20e19fa729b0d4d3f2fb004196f8b600c28069acec7c8e1f`  
		Last Modified: Thu, 17 Oct 2024 08:29:15 GMT  
		Size: 16.1 MB (16115196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053438fd731a9ea0966b5e7ceeff8628b2d336a0e378b4a12c7d959b8496e401`  
		Last Modified: Fri, 18 Oct 2024 18:49:56 GMT  
		Size: 1.3 MB (1297619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df77c73431045c5ab99cae2183c8426c10ab43c1adbe8a645eeb070c42b0d95a`  
		Last Modified: Fri, 18 Oct 2024 18:49:58 GMT  
		Size: 17.7 MB (17698123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abb2f4797050b481cd74785d796ef3f9431d7081b7d7a37f87b1379693aaee`  
		Last Modified: Fri, 18 Oct 2024 18:49:54 GMT  
		Size: 648.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b473734a16411d4c6e3bbe3f56bc0626fa32f355c4e8f3af2d7540c84ec14`  
		Last Modified: Fri, 18 Oct 2024 18:50:35 GMT  
		Size: 18.2 MB (18204624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e347e988618024aa569bab449da6663b0865408cd17f451781bdaf04eda121`  
		Last Modified: Fri, 18 Oct 2024 18:50:33 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feda42e789abf5bc49dd84e9118934ddb1bce488c423667979d196b709041334`  
		Last Modified: Fri, 18 Oct 2024 18:50:33 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
