## `nextcloud:production`

```console
$ docker pull nextcloud@sha256:fedded19da658d93d71de7e0839644c3078ddd823f5eb80fdc3c5f336914b1e1
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

### `nextcloud:production` - linux; amd64

```console
$ docker pull nextcloud@sha256:d31c88c7c8200bead0c11d10cff2210bef9b39a79f35b7fc0989eb07173b33ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329609862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00110ecf7953ca3c3dfc8463b3119d40a41020cfaf7c8b9fbaf2c753e56137ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:39:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 17 Nov 2021 18:39:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 17 Nov 2021 18:39:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:39:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Nov 2021 18:39:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Nov 2021 18:48:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 17 Nov 2021 18:48:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 17 Nov 2021 18:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 17 Nov 2021 18:48:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 17 Nov 2021 18:48:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 17 Nov 2021 18:48:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 18:48:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 18:48:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Nov 2021 19:43:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Nov 2021 19:43:08 GMT
ENV PHP_VERSION=8.0.12
# Wed, 17 Nov 2021 19:43:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Wed, 17 Nov 2021 19:43:09 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Wed, 17 Nov 2021 19:43:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:43:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Nov 2021 19:49:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Nov 2021 19:49:10 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Wed, 17 Nov 2021 19:49:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Nov 2021 19:49:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Nov 2021 19:49:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Nov 2021 19:49:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Nov 2021 19:49:12 GMT
WORKDIR /var/www/html
# Wed, 17 Nov 2021 19:49:12 GMT
EXPOSE 80
# Wed, 17 Nov 2021 19:49:12 GMT
CMD ["apache2-foreground"]
# Thu, 18 Nov 2021 22:51:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 18 Nov 2021 22:51:53 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Nov 2021 22:51:53 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Nov 2021 22:54:53 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 22:54:54 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 18 Nov 2021 22:54:55 GMT
VOLUME [/var/www/html]
# Thu, 18 Nov 2021 22:54:55 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 18 Nov 2021 22:54:56 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Thu, 18 Nov 2021 22:55:50 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 22:55:51 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Thu, 18 Nov 2021 22:55:52 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Thu, 18 Nov 2021 22:55:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 22:55:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933427dc39f71a5496e5f77f11d4d79eafada8f53e64652a2f932bf6d7bc3286`  
		Last Modified: Wed, 17 Nov 2021 21:37:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bb08dc7ee2f0e608b21692ff6962430b894a5f1e055fd797af09251fd0b3e6`  
		Last Modified: Wed, 17 Nov 2021 21:37:55 GMT  
		Size: 91.6 MB (91604381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a3f26800d72c5796c9ae5d9b70c5192d98e4ec6a17f16d295f02d01d111d38`  
		Last Modified: Wed, 17 Nov 2021 21:37:38 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba5c0e912ac9d90c132b31df7c37c80394a04cc6b7dafd46e1c22fa65264a35`  
		Last Modified: Wed, 17 Nov 2021 21:38:26 GMT  
		Size: 19.2 MB (19235814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e5c0d120c5e221ae3351a219f948c634c04107bbb9372caf81d5cde5139a9a`  
		Last Modified: Wed, 17 Nov 2021 21:38:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410a26230a3bce920b854517e56481fa15f5647135ec074c9ad83d7895c4845a`  
		Last Modified: Wed, 17 Nov 2021 21:38:23 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ffa4f6616c6a0bd98c926ad2846d40761b590e5d1a605a608d15e90c11a0cd`  
		Last Modified: Wed, 17 Nov 2021 21:41:52 GMT  
		Size: 11.1 MB (11053718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9661660eba7e5ac9474d41f0d4d4c77f185076dac7bde6a9e09ae1c0265c68`  
		Last Modified: Wed, 17 Nov 2021 21:41:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05167cc4a9c5a19c17739820cdf31c62b5197312c0fcd2b3f83f6a98d5f675ff`  
		Last Modified: Wed, 17 Nov 2021 21:41:52 GMT  
		Size: 14.5 MB (14546790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec8d188a32166901c149bf1d09839badf7b971040fde5f035a16560e287cc1`  
		Last Modified: Wed, 17 Nov 2021 21:41:49 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967573af4e77debb4eddd4b48cc9c1d5a0aa4aeb858de41c1313c86bb909ba9b`  
		Last Modified: Wed, 17 Nov 2021 21:41:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d2474097f53e65f1cb0e8875e41eac4c608d70e2fd197b942067bccc6da564`  
		Last Modified: Wed, 17 Nov 2021 21:41:49 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe060c9fa259ad4768672e1769fdbd5817ce0f8ec068d8a66a329b2a0ef1d02`  
		Last Modified: Thu, 18 Nov 2021 23:02:29 GMT  
		Size: 1.7 MB (1700428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7917d7305be7adc10022f270c4e5d981c3f8c7651326329e44515ce507924367`  
		Last Modified: Thu, 18 Nov 2021 23:02:31 GMT  
		Size: 17.4 MB (17386420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ab532e08fc78b5832f1c95b069fde9eec501af6cfe0a4fae89bd81d57c87d5`  
		Last Modified: Thu, 18 Nov 2021 23:02:26 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b02337d323df0867049e591e983381bdd957b571ebabb3ddaf9e54bf705c91`  
		Last Modified: Thu, 18 Nov 2021 23:02:26 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde2b37e1f7cfdd00a72bf6ed6ee467427890790d9a892919575dd7f6e931d97`  
		Last Modified: Thu, 18 Nov 2021 23:02:44 GMT  
		Size: 142.7 MB (142700688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87275776a1a50f7a5d90fbc94b4115b56a9b9432b5361ffa2da3e1eddbebbdf2`  
		Last Modified: Thu, 18 Nov 2021 23:02:26 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998d89bad5715018634f0815abb8ca350e9870a9edb0b9c8b06a85dd961bee9d`  
		Last Modified: Thu, 18 Nov 2021 23:02:26 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:a2c5001568e1197b014add63ebe576ab1b5b0ab7051fb5c84cb43156e4dc850b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304888753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6074904d7f530e78c3aaf7bbc32f4da0c7a68d7b505fd76256e1fd29556b6bfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 17 Nov 2021 02:50:37 GMT
ADD file:738a04a17bdb9077594ad9a847333abe28216a7f04d3058718a5e21c236c24bb in / 
# Wed, 17 Nov 2021 02:50:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 11:47:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 17 Nov 2021 11:47:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 17 Nov 2021 11:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 11:48:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Nov 2021 11:48:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Nov 2021 11:54:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 17 Nov 2021 11:54:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 17 Nov 2021 11:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 17 Nov 2021 11:55:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 17 Nov 2021 11:55:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 17 Nov 2021 11:55:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 11:55:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 11:55:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Nov 2021 12:40:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Nov 2021 12:40:55 GMT
ENV PHP_VERSION=8.0.12
# Wed, 17 Nov 2021 12:40:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Wed, 17 Nov 2021 12:40:55 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Wed, 17 Nov 2021 12:41:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 12:41:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Nov 2021 12:46:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Nov 2021 12:46:21 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Wed, 17 Nov 2021 12:46:23 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Nov 2021 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Nov 2021 12:46:24 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Nov 2021 12:46:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Nov 2021 12:46:25 GMT
WORKDIR /var/www/html
# Wed, 17 Nov 2021 12:46:26 GMT
EXPOSE 80
# Wed, 17 Nov 2021 12:46:26 GMT
CMD ["apache2-foreground"]
# Thu, 18 Nov 2021 00:14:37 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 18 Nov 2021 00:14:37 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Nov 2021 00:14:38 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Nov 2021 00:21:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:21:37 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 18 Nov 2021 00:21:37 GMT
VOLUME [/var/www/html]
# Thu, 18 Nov 2021 00:21:39 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 18 Nov 2021 00:21:39 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Thu, 18 Nov 2021 00:23:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:23:21 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Thu, 18 Nov 2021 00:23:23 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Thu, 18 Nov 2021 00:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 00:23:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a960a56baa1baffbe2aa1e0c1fb02f9ee4816337d02fec259b312c409d77fafc`  
		Last Modified: Wed, 17 Nov 2021 03:06:09 GMT  
		Size: 28.9 MB (28911006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d62576d1f6422c12c501987232cd6f109fa674dc90280a6e5f6df8a00ae06e`  
		Last Modified: Wed, 17 Nov 2021 14:52:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0656b9bd7ea73f5f220dc0afd21463ece375910ea9be93642df3ebe82adb6dfe`  
		Last Modified: Wed, 17 Nov 2021 14:53:02 GMT  
		Size: 73.7 MB (73684261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8f131fa288cff4e5199651721306dde0c83007d84f312a29e3b52dc74ce94e`  
		Last Modified: Wed, 17 Nov 2021 14:52:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d6c1536456cc545cb407c3b891f7080543b47eb4148d28998c839d79d18c36`  
		Last Modified: Wed, 17 Nov 2021 14:53:53 GMT  
		Size: 18.5 MB (18525659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5cf7cbd672acd1680272f57a540436ba2906de5a1a7347128ddc8071ed033e`  
		Last Modified: Wed, 17 Nov 2021 14:53:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0366e9bd9df4f3876ff7dcd3089019696af4de6ad3003aab4e1515e32cb0f2`  
		Last Modified: Wed, 17 Nov 2021 14:53:42 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fe764286e9f8e3c7e1e52ea274c979fe160c1ec6d02079860e40730da454f0`  
		Last Modified: Wed, 17 Nov 2021 14:59:30 GMT  
		Size: 11.1 MB (11052347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f5ffbcd6032acd223c524a12624768c4d4a72fb3c3df6a3e775c4dab451d6`  
		Last Modified: Wed, 17 Nov 2021 14:59:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5953d2f9734338b40652258a82d941668b7b435d8d2064e6397adeadea1deb`  
		Last Modified: Wed, 17 Nov 2021 14:59:36 GMT  
		Size: 13.3 MB (13259903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1894a306fc736c205c710b2d8c08a381b04e926b2d741b3f2855567f9b0ac9c6`  
		Last Modified: Wed, 17 Nov 2021 14:59:25 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e4b82998ac2ecd6b557c18dccbd2278dd69439eb803b872e35e5307bdb8b0b`  
		Last Modified: Wed, 17 Nov 2021 14:59:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de76b15e7b17854aa0389101a019797b703de2ce75a3f91d62e1448c1299dd3`  
		Last Modified: Wed, 17 Nov 2021 14:59:25 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2429026f75e48ba0aa8cbbde41113e3fabce5cf1233d263427cf05808b584ed`  
		Last Modified: Thu, 18 Nov 2021 00:34:52 GMT  
		Size: 1.7 MB (1656145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941ab174e8a4c15301a0264ad47cb1ca5aa2f4f0369b1584ce0d5b54f0239d51`  
		Last Modified: Thu, 18 Nov 2021 00:35:00 GMT  
		Size: 15.1 MB (15088869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25063344bcb517e5d670aef0bc1bafe87631242aea64aee08376607cd4681691`  
		Last Modified: Thu, 18 Nov 2021 00:34:49 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b7a25a6e6fc238760692dccaa28dc57cf647e2aa57cb47b9e927323f0b38f0`  
		Last Modified: Thu, 18 Nov 2021 00:34:49 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558813b7c1223b511bc88483418ee683e92b0dd4b3b43a4268f255c41a8a5464`  
		Last Modified: Thu, 18 Nov 2021 00:36:26 GMT  
		Size: 142.7 MB (142699197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f235d18e7fe0601d45d1e15a39f091cf98e49f49410293d4abe9de1efe559a`  
		Last Modified: Thu, 18 Nov 2021 00:34:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a152eaf70397db43d5cc325fc3ef55d8ea744e5e2c402d1da8c0d12b40c46a5`  
		Last Modified: Thu, 18 Nov 2021 00:34:49 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:15f3dc004e6325ae2bd389382e575993fac84fd6d954b2ada59dbb2c3f898613
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295659506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba3a0c6f3d1c6f32e36d53931a287ad47543c7df02d1a4a6f7e9b4a37c5bc1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 14:32:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 17 Nov 2021 14:32:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 17 Nov 2021 14:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 14:32:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Nov 2021 14:32:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Nov 2021 14:38:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 17 Nov 2021 14:38:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 17 Nov 2021 14:38:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 17 Nov 2021 14:38:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 17 Nov 2021 14:38:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 17 Nov 2021 14:38:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 14:38:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 14:38:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Nov 2021 15:21:16 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Nov 2021 15:21:16 GMT
ENV PHP_VERSION=8.0.12
# Wed, 17 Nov 2021 15:21:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Wed, 17 Nov 2021 15:21:17 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Wed, 17 Nov 2021 15:21:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 15:21:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Nov 2021 15:26:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Nov 2021 15:26:10 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Wed, 17 Nov 2021 15:26:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Nov 2021 15:26:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Nov 2021 15:26:13 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Nov 2021 15:26:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Nov 2021 15:26:14 GMT
WORKDIR /var/www/html
# Wed, 17 Nov 2021 15:26:14 GMT
EXPOSE 80
# Wed, 17 Nov 2021 15:26:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Nov 2021 22:14:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 18 Nov 2021 22:14:32 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Nov 2021 22:14:33 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Nov 2021 22:21:07 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 22:21:09 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 18 Nov 2021 22:21:09 GMT
VOLUME [/var/www/html]
# Thu, 18 Nov 2021 22:21:11 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 18 Nov 2021 22:21:11 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Thu, 18 Nov 2021 22:22:40 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 22:22:43 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Thu, 18 Nov 2021 22:22:45 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Thu, 18 Nov 2021 22:22:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 22:22:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee38362a3159843b7af9c8fbec3c2e700c3aa7a23b75266775cf694f7ea72538`  
		Last Modified: Wed, 17 Nov 2021 17:36:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585c04fe561e3a9fb7943e2ed378e700d3fd1276e171975f11a6a5f097386102`  
		Last Modified: Wed, 17 Nov 2021 17:36:48 GMT  
		Size: 69.3 MB (69314801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097d5ecc54062515e3f42674fad22b94112041a69d148d4d43f8febaab35921e`  
		Last Modified: Wed, 17 Nov 2021 17:36:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567a3462d460290b44667655abc460ca1b2b8af93ae717a97718e253c0a14fff`  
		Last Modified: Wed, 17 Nov 2021 17:37:39 GMT  
		Size: 18.0 MB (17987460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e870e68d221444a118d0eaaf89c08ce60f0cc0e5c91feb821b150dbfa38d3d4`  
		Last Modified: Wed, 17 Nov 2021 17:37:31 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae437a68bd98d95ae0d2941af99903d6c5d2d1eaf7f71af3683d9d63d2c05738`  
		Last Modified: Wed, 17 Nov 2021 17:37:31 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a7b1b9ebea041260928a784cd63e2711e252ec6eaa18b7f59e098bf9303ee9`  
		Last Modified: Wed, 17 Nov 2021 17:43:49 GMT  
		Size: 11.1 MB (11052328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff53808b09cf3244b327ffe6d9d0be81486d3629c1af19a4e746093cb31a258`  
		Last Modified: Wed, 17 Nov 2021 17:43:44 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef47351bbd4ee4a34a52da27eb4ad37b742e208aaf77ad9ff5de158599c0d4d3`  
		Last Modified: Wed, 17 Nov 2021 17:43:53 GMT  
		Size: 12.6 MB (12555576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603121a702bf57f8acd59a98231a8e34fb7b799da4e6702155fdab8f23405951`  
		Last Modified: Wed, 17 Nov 2021 17:43:44 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870761ff79da359454dd6d6cc05f813fef7cbb24e3b6d385db9718f84952e054`  
		Last Modified: Wed, 17 Nov 2021 17:43:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750d246261d1d207e473cb2babd99fbcdd7fbecc8a2df2c4c46df98bba0c13de`  
		Last Modified: Wed, 17 Nov 2021 17:43:44 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f6e07ac05ca3fa7bbbabf306ffbb7367d95cab4eeaaf4929995c1cd943f794`  
		Last Modified: Thu, 18 Nov 2021 22:36:35 GMT  
		Size: 1.5 MB (1510114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4affb998fe077f159b9e04300855723666a57fe4c3ff0ec94bc2264be380168d`  
		Last Modified: Thu, 18 Nov 2021 22:36:42 GMT  
		Size: 14.0 MB (13955416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010cc90c8be493f0298d65a6233e6c0e933d1956428bc293e8f1da2715448e65`  
		Last Modified: Thu, 18 Nov 2021 22:36:32 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8e5c33cf55a4af80bf7f2187849789485fa59d920ca2d7663580010382efb`  
		Last Modified: Thu, 18 Nov 2021 22:36:32 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717f891c07d1d720f9112087673059440380ff60acf3f11eea534948f9bd875b`  
		Last Modified: Thu, 18 Nov 2021 22:38:08 GMT  
		Size: 142.7 MB (142699290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1042949a310f81249dda6778858e89da55e0569f9ab7fc63eba5f7f208befa4f`  
		Last Modified: Thu, 18 Nov 2021 22:36:32 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a284e510205df6b7c74c4b6edb79518dde3819d9a915e1fba3bb3684797d29`  
		Last Modified: Thu, 18 Nov 2021 22:36:32 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:df65df6c2c2d751d8a8f278bdc2734f2de4edb22a575a89d2c7a4467e0249e8d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319556671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4c5d5b7ae968db5c11c3c4eb247bc35bc6ef2a876fa149e5c3e7f83a623f82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Thu, 14 Oct 2021 20:01:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 14 Oct 2021 20:01:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 14 Oct 2021 20:01:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 20:01:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:01:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:06:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 14 Oct 2021 20:06:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 14 Oct 2021 20:06:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 14 Oct 2021 20:06:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 14 Oct 2021 20:06:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 14 Oct 2021 20:06:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:06:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:06:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:03:23 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 21 Oct 2021 15:48:13 GMT
ENV PHP_VERSION=8.0.12
# Thu, 21 Oct 2021 15:48:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Thu, 21 Oct 2021 15:48:15 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Thu, 21 Oct 2021 15:48:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Oct 2021 15:48:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:51:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Oct 2021 15:51:02 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:51:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Oct 2021 15:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Oct 2021 15:51:04 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Oct 2021 15:51:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:51:06 GMT
WORKDIR /var/www/html
# Thu, 21 Oct 2021 15:51:07 GMT
EXPOSE 80
# Thu, 21 Oct 2021 15:51:08 GMT
CMD ["apache2-foreground"]
# Thu, 21 Oct 2021 18:51:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 21 Oct 2021 18:51:52 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 Oct 2021 18:51:53 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 Oct 2021 18:54:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 18:54:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 21 Oct 2021 18:54:18 GMT
VOLUME [/var/www/html]
# Thu, 21 Oct 2021 18:54:19 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 17 Nov 2021 00:55:35 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Wed, 17 Nov 2021 00:58:32 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 00:58:35 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Wed, 17 Nov 2021 00:58:37 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Wed, 17 Nov 2021 00:58:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 00:58:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e8dc602726d99b28b5686afda874ade5e865d91b658bc68dff4a02c3062f7a`  
		Last Modified: Thu, 14 Oct 2021 23:07:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f1ee1d0d511e2f20f2114a9991e2f3cf25a91cae9d6662a65cf2b4f53dc01`  
		Last Modified: Thu, 14 Oct 2021 23:07:30 GMT  
		Size: 86.9 MB (86920409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a167ae8f3a912487645dcb4aef47f14d63f29d7a1c2ea4ae26bdd531f2f8f`  
		Last Modified: Thu, 14 Oct 2021 23:07:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566731d744b22af202f1c1f1cb5af9f295596e83869b10e07397c7bd085908ae`  
		Last Modified: Thu, 14 Oct 2021 23:08:04 GMT  
		Size: 18.9 MB (18939819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512a0e300c292015b8f6716bc5d9f3469fa6a7f958a487a002ab1da01938573c`  
		Last Modified: Thu, 14 Oct 2021 23:08:01 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe39677b5f5deed457115099f2a19558013a51d7679a6c702d90b9cc72b0d4b1`  
		Last Modified: Thu, 14 Oct 2021 23:08:01 GMT  
		Size: 483.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f342b05b16b92fd0dbb0684f2b72149c36f91b6bac6eabd9bb96f3804aeb9e28`  
		Last Modified: Thu, 21 Oct 2021 16:35:15 GMT  
		Size: 10.8 MB (10838030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca11ff823ba8ecf066aa9da088b7935bedf7737ef37c2d9bcfbd0be50075157c`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e493dedba1779aadb5c529ecbcd0b979ce00896c951e59deb359ecdb7311d`  
		Last Modified: Thu, 21 Oct 2021 16:35:14 GMT  
		Size: 13.9 MB (13937758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d071bd54c6be3add80775fd977292f1b5b91c7219ae4adc417408a8398c6244`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffc2387bd5a90f3b0f9f193f4241821536278cc19c10b4144b6c4ff02030a6b`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055168e083aa246fba5dbfa702243e140964958d13962ea3a42b9f67fe1088dd`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed48a1ff85634c0d282fdf2529ab7d26b665ea5acefc27fec494f218cc50db02`  
		Last Modified: Thu, 21 Oct 2021 19:06:22 GMT  
		Size: 1.4 MB (1431542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4bb0d395de13787c5cf31724b06b1041d0b8b9849b153630ebabb0c111c48d`  
		Last Modified: Thu, 21 Oct 2021 19:06:24 GMT  
		Size: 15.0 MB (14970334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd64e0a98724e3cfe2d8c666aaa3f39d64c744444d8ac863fc6463e1e6ec7b9`  
		Last Modified: Thu, 21 Oct 2021 19:06:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd51fa28e1b2b7e4a52b9632ac14103f2e30f268555381effae30d46f3680a6`  
		Last Modified: Thu, 21 Oct 2021 19:06:19 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02201200bfa2b94ad7b85e7aebe2887ee63dffcd0d75b9cfd47ec55efa615e01`  
		Last Modified: Wed, 17 Nov 2021 01:09:24 GMT  
		Size: 142.5 MB (142463685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73e0533f1c83bd540ffeb538df83e3e5e82c7579b759bcd4f4abd12439147e`  
		Last Modified: Wed, 17 Nov 2021 01:09:03 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a84a6ef004d8d0bbb6b8ae8fd74cf442cec6c2069447074c6587d0fece002f`  
		Last Modified: Wed, 17 Nov 2021 01:09:02 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; 386

```console
$ docker pull nextcloud@sha256:5ead671228cac1eb7e8deb6db551ba3224a5bee51c9871946ac98ecdd35f9f3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331813304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf0b912f29c84e30e1aab48e8420f6a1ee557c441e651499c35b7f79149d84d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:16:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 17 Nov 2021 09:16:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 17 Nov 2021 09:16:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:16:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Nov 2021 09:16:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Nov 2021 09:23:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 17 Nov 2021 09:23:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 17 Nov 2021 09:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 17 Nov 2021 09:23:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 17 Nov 2021 09:23:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 17 Nov 2021 09:23:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 09:23:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 09:23:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Nov 2021 10:12:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Nov 2021 10:12:55 GMT
ENV PHP_VERSION=8.0.12
# Wed, 17 Nov 2021 10:12:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Wed, 17 Nov 2021 10:12:55 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Wed, 17 Nov 2021 10:13:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 10:13:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Nov 2021 10:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Nov 2021 10:18:47 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Wed, 17 Nov 2021 10:18:48 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Nov 2021 10:18:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Nov 2021 10:18:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Nov 2021 10:18:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Nov 2021 10:18:49 GMT
WORKDIR /var/www/html
# Wed, 17 Nov 2021 10:18:49 GMT
EXPOSE 80
# Wed, 17 Nov 2021 10:18:49 GMT
CMD ["apache2-foreground"]
# Wed, 17 Nov 2021 23:08:26 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 17 Nov 2021 23:08:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 17 Nov 2021 23:08:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 17 Nov 2021 23:13:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:13:10 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 17 Nov 2021 23:13:10 GMT
VOLUME [/var/www/html]
# Wed, 17 Nov 2021 23:13:11 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 17 Nov 2021 23:13:11 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Wed, 17 Nov 2021 23:14:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:14:40 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Wed, 17 Nov 2021 23:14:43 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Wed, 17 Nov 2021 23:14:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 23:14:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9208767da7df5fdb2170d7142de5a0e92c17b08c9c8b0b50d31d314fabe72`  
		Last Modified: Wed, 17 Nov 2021 12:48:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fea35b73840adac94518cb2d327d4e6d709abf3c5590ba808169ec172b7eb1`  
		Last Modified: Wed, 17 Nov 2021 12:48:47 GMT  
		Size: 92.7 MB (92716817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769bb36e0e1016e5c697903187baaa41d7173041322430b61e0cf51383eafb94`  
		Last Modified: Wed, 17 Nov 2021 12:48:10 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe854d5cfdf4190168816bb74032faeccfa17cee11274c09e4914583c508da6`  
		Last Modified: Wed, 17 Nov 2021 12:49:27 GMT  
		Size: 19.7 MB (19713910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce16058c1902813c444604c212a40e1f7fbbfdb4e499392d29e2d7a0e82fcd`  
		Last Modified: Wed, 17 Nov 2021 12:49:22 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e8844955045ee8d74f7480cc227291bd4329160fe22bc170ef5c26292d4a85`  
		Last Modified: Wed, 17 Nov 2021 12:49:22 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef5018ce8dc541c68f50e6d2f999dbd28d55cf655c007570f2b3c7647445218`  
		Last Modified: Wed, 17 Nov 2021 12:54:33 GMT  
		Size: 11.1 MB (11053048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716228d15dcfc5e93960cc3c3a125d9097af68ff1276813421c3453bd8223c4f`  
		Last Modified: Wed, 17 Nov 2021 12:54:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c43ce05ee41945b079439e7b4e49b15ed92a3fd89bb6682a3754196632b56`  
		Last Modified: Wed, 17 Nov 2021 12:54:36 GMT  
		Size: 14.8 MB (14832518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aaab348aaa15e6d92adf65f670268f58d836439243441707e43d6d03a554f80`  
		Last Modified: Wed, 17 Nov 2021 12:54:29 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eabb57d42e4f13f7a29980b2bb61eff4da3e2b05efd99fc9154cec6f46bfb59`  
		Last Modified: Wed, 17 Nov 2021 12:54:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b45e239aa1d2fa07085ae18309146c7cf7f551b6259613ab0461a89efd14d`  
		Last Modified: Wed, 17 Nov 2021 12:54:29 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e558afc0fb2ca25e936b69233ef14e46b6a15e1042758205dfe37261aebd95db`  
		Last Modified: Wed, 17 Nov 2021 23:28:27 GMT  
		Size: 1.7 MB (1731286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a204e5352b0c9cbafc4d2894a89e8d1efb5076a3404c56945267f214c35fc7`  
		Last Modified: Wed, 17 Nov 2021 23:28:33 GMT  
		Size: 16.7 MB (16673414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0000809df474091edd6d968548d1622fcdd0eabf1ea6cd4ef3a83d476956a9dc`  
		Last Modified: Wed, 17 Nov 2021 23:28:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd74d4961ecf7a1f7e3aa5753937de2352f7f651361a2f1bf97b2b6e41ec4d8a`  
		Last Modified: Wed, 17 Nov 2021 23:28:23 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594cc988c951d37b12760bfb0eed5a304df2637a5b9f5c14c1f85e28b49659a0`  
		Last Modified: Wed, 17 Nov 2021 23:29:09 GMT  
		Size: 142.7 MB (142700273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fce56ea6e72d7a49dbffe6aeadf2d29383fcd395f5939c05261305089b84e98`  
		Last Modified: Wed, 17 Nov 2021 23:28:23 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95487187b7c5c83c46a2d662237a7ebfeeefa8e8d86e140fa85580f45d186a50`  
		Last Modified: Wed, 17 Nov 2021 23:28:23 GMT  
		Size: 2.1 KB (2117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; mips64le

```console
$ docker pull nextcloud@sha256:b9adc54d99de5194d5534b6b238a2c02286897720f61d77c3e1844393e74d8d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304730632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4157f4c4679ac6e25783a117fa0721cbee0e5b054dce9ce3b53e83b3978467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 17 Nov 2021 02:10:13 GMT
ADD file:10bc783d286d0a800f59d5009e87ecb4651659c82cae1325132756c7c8b1dec0 in / 
# Wed, 17 Nov 2021 02:10:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:30:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 17 Nov 2021 09:30:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 17 Nov 2021 09:31:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Nov 2021 09:31:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Nov 2021 09:44:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 17 Nov 2021 09:44:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 17 Nov 2021 09:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 17 Nov 2021 09:44:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 17 Nov 2021 09:45:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 17 Nov 2021 09:45:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 09:45:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Nov 2021 09:45:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Nov 2021 11:31:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Nov 2021 11:31:34 GMT
ENV PHP_VERSION=8.0.12
# Wed, 17 Nov 2021 11:31:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Wed, 17 Nov 2021 11:31:35 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Wed, 17 Nov 2021 11:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 11:32:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Nov 2021 11:44:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Nov 2021 11:44:22 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Wed, 17 Nov 2021 11:44:24 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Nov 2021 11:44:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Nov 2021 11:44:24 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Nov 2021 11:44:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Nov 2021 11:44:25 GMT
WORKDIR /var/www/html
# Wed, 17 Nov 2021 11:44:25 GMT
EXPOSE 80
# Wed, 17 Nov 2021 11:44:26 GMT
CMD ["apache2-foreground"]
# Thu, 18 Nov 2021 22:27:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 18 Nov 2021 22:27:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Nov 2021 22:27:22 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Nov 2021 22:35:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 22:35:22 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 18 Nov 2021 22:35:23 GMT
VOLUME [/var/www/html]
# Thu, 18 Nov 2021 22:35:25 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 18 Nov 2021 22:35:25 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Thu, 18 Nov 2021 22:37:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 22:37:32 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Thu, 18 Nov 2021 22:37:34 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Thu, 18 Nov 2021 22:37:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 22:37:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:08bca22fbffb4e58224e9e4f6a56f1ca5099c002b1aeb6181df63af308a3da58`  
		Last Modified: Wed, 17 Nov 2021 02:19:09 GMT  
		Size: 29.6 MB (29630388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90252f0095ebb6a4d47ace88769fae84fb709eda4584fd6bd2937d1ca0f23013`  
		Last Modified: Wed, 17 Nov 2021 15:39:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfac52f341812c21aad8741b50071fe37a21fd051d94b1f43bbfa30f8a88b0e`  
		Last Modified: Wed, 17 Nov 2021 15:40:12 GMT  
		Size: 72.0 MB (72013638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f77b3771cac3402c4ac0c013fc9d0117b7377a6147971d46a546bd2b2f57829`  
		Last Modified: Wed, 17 Nov 2021 15:39:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f8b05868db99b03cb7b4505db1b23e9f80370922e0cc9503f1fc5ce94f1b03`  
		Last Modified: Wed, 17 Nov 2021 15:40:59 GMT  
		Size: 19.1 MB (19143641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e577af29206c51c8b744b486d5052423c4b3673c6386452b61a5c1ff3722af17`  
		Last Modified: Wed, 17 Nov 2021 15:40:46 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9ebb2ba5947b239cf08b9f8164ef1dd66a970420de471c04d8319012b609ca`  
		Last Modified: Wed, 17 Nov 2021 15:40:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b400cedbdf98a32a4f7e91cc0b19b9964736bc5584c78cf832fcd047eaba0d57`  
		Last Modified: Wed, 17 Nov 2021 15:46:44 GMT  
		Size: 11.1 MB (11051693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac066f29fc565be447538c40269ffea7716a13c01f20959ccfd2d564e9fb2ca9`  
		Last Modified: Wed, 17 Nov 2021 15:46:38 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce507dca255ba5f11c6c0855f0350db5a1ec48508f12a9dc7f0a666e6494da55`  
		Last Modified: Wed, 17 Nov 2021 15:46:50 GMT  
		Size: 13.5 MB (13484834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a001b9924ceb22e3561ffa8ced908275923125613d5afd2722a8c9fd4c2b93`  
		Last Modified: Wed, 17 Nov 2021 15:46:38 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e6df3ad6264b4af138913c7ceffa054ab0088c1b51ca7657be779e70fd922`  
		Last Modified: Wed, 17 Nov 2021 15:46:38 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d72f6f8df999d703dd3fe5ee263ea0e56dfe3a88af7b3270ff1a64a37815a`  
		Last Modified: Wed, 17 Nov 2021 15:46:38 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971aeb919551586e7e5e18a1ead203ab0dc18b358ac9d3e47ba6dc2546e9c383`  
		Last Modified: Thu, 18 Nov 2021 22:55:53 GMT  
		Size: 1.8 MB (1783559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694cc64eb8ee70c221b6eaf5d9d701a7eb5723bd595db66a63118525d3f9ed3c`  
		Last Modified: Thu, 18 Nov 2021 22:56:03 GMT  
		Size: 14.9 MB (14912166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b231a8ad9334f121572221ad4f6c7be66fb81df0b3f5ec6df42bfcbe3eb1f`  
		Last Modified: Thu, 18 Nov 2021 22:55:49 GMT  
		Size: 568.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215dcf96449275360210dcc96f9f5e5594f334988fb09c7711a9e34fe843b8fd`  
		Last Modified: Thu, 18 Nov 2021 22:55:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcedd4a61ff4867cec634203a113ef4d36e1e6dd6fa7e4c552fd923acdc3f81`  
		Last Modified: Thu, 18 Nov 2021 22:57:24 GMT  
		Size: 142.7 MB (142699487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4c09cba74fe349b92d9fe7972b02cf1c419cbf37ea1379369866f717417e34`  
		Last Modified: Thu, 18 Nov 2021 22:55:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bcbc74e054a4c253f93b3ceefd2a758ba3767bcb89e3a46f5f71eee973ef48`  
		Last Modified: Thu, 18 Nov 2021 22:55:49 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:4c2eeef948fa5d9b2f27aeda20b60bb3833ea2fb9329a08f64b272bbc655d4bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330111626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72de44c5a742c4eb9ffec21daeafc78f2f4c80d1b4a5b497d33d817e0903f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:45 GMT
ADD file:d8794fadf16c9948c3574ba28740d08393eca57766340333ad91f9c2a33eb719 in / 
# Tue, 12 Oct 2021 01:25:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 10:23:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Oct 2021 10:23:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Oct 2021 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 10:26:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Oct 2021 10:26:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 12 Oct 2021 10:33:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Oct 2021 10:33:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Oct 2021 10:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Oct 2021 10:34:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Oct 2021 10:34:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 14 Oct 2021 19:29:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 19:29:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 19:29:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 20:42:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 21 Oct 2021 15:24:58 GMT
ENV PHP_VERSION=8.0.12
# Thu, 21 Oct 2021 15:25:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Thu, 21 Oct 2021 15:25:02 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Thu, 21 Oct 2021 15:26:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Oct 2021 15:26:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Oct 2021 15:32:37 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:32:43 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Oct 2021 15:32:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Oct 2021 15:32:47 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Oct 2021 15:32:47 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:32:49 GMT
WORKDIR /var/www/html
# Thu, 21 Oct 2021 15:32:52 GMT
EXPOSE 80
# Thu, 21 Oct 2021 15:32:55 GMT
CMD ["apache2-foreground"]
# Thu, 21 Oct 2021 21:52:19 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 21 Oct 2021 21:52:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 Oct 2021 21:52:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 Oct 2021 22:02:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 22:03:11 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 21 Oct 2021 22:03:15 GMT
VOLUME [/var/www/html]
# Thu, 21 Oct 2021 22:03:22 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 17 Nov 2021 00:59:19 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Wed, 17 Nov 2021 01:02:31 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 01:02:37 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Wed, 17 Nov 2021 01:02:41 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Wed, 17 Nov 2021 01:02:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 01:02:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6c28c1405c677dd809094d06190225b38cee3d24f18da38d287ef5bcc67884d6`  
		Last Modified: Tue, 12 Oct 2021 01:37:00 GMT  
		Size: 35.3 MB (35258729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007cbc0c1bbccf469e9d9fc6e98e3d4ad1e4469d5f23cc0d263aa3bdc8f9c5`  
		Last Modified: Tue, 12 Oct 2021 14:32:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6750fd2121e14e6e55c726ed712f7b485e03363824dd42e9fa37ca714848f4c6`  
		Last Modified: Tue, 12 Oct 2021 14:33:23 GMT  
		Size: 86.6 MB (86624771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6280509c1db590ff214716adca9daabd1ac3c060c29e70cf6ed8dc17061d64db`  
		Last Modified: Tue, 12 Oct 2021 14:32:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dfb045a88eef5b0550b8548fbf2106468aac82881db516e679b9d5811ab750`  
		Last Modified: Tue, 12 Oct 2021 14:34:14 GMT  
		Size: 20.4 MB (20441245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b153f7d4d58c38f56768aadaefa599fdeb615c6c4940ce33f129d7df3c44d8a`  
		Last Modified: Tue, 12 Oct 2021 14:33:57 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed81b8cad279c736a63388220d89e0dc436c6f8586239e6e9c3b975efaf6c1f`  
		Last Modified: Tue, 12 Oct 2021 14:33:57 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c4cdabdb71acd8df1784e65672e49a2a186999839ebd97a7cf3c91b2c319b4`  
		Last Modified: Thu, 21 Oct 2021 16:40:22 GMT  
		Size: 11.1 MB (11054109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e46dee9749281c9799843fb42dc46d3bc20647d3d9ecdb57b777f20d2e0544d`  
		Last Modified: Thu, 21 Oct 2021 16:40:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e624eae98e2a55659c9aa35d79eb4f0fee861d12d61953c9112f01364fd8a03d`  
		Last Modified: Thu, 21 Oct 2021 16:40:21 GMT  
		Size: 15.2 MB (15245532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc41c26588d673f40679d98608d6af5b37e494a4a448061b9c51da404fc1492`  
		Last Modified: Thu, 21 Oct 2021 16:40:17 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488908e1176668a4dadad66f084e023b4746da1589803321cf7599d533269a2a`  
		Last Modified: Thu, 21 Oct 2021 16:40:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078f8d7f455999a75adb8853cfac2d83292260b3d60af8a9844afed02ea61e6c`  
		Last Modified: Thu, 21 Oct 2021 16:40:17 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2923ae57dbb7b8b5a612e84deb07bd66bf494b551400167fdcf38a52a90025b3`  
		Last Modified: Thu, 21 Oct 2021 22:15:19 GMT  
		Size: 1.9 MB (1870720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee3bd44d047b79fc1caf2d0d6ca102c5fc2922979e5cf0f3a1a123531a14ec`  
		Last Modified: Thu, 21 Oct 2021 22:15:21 GMT  
		Size: 16.9 MB (16901878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ea35436077d19743cb4a5a0419b15f46b14cb068a4b40aed91c12230ab5b7f`  
		Last Modified: Thu, 21 Oct 2021 22:15:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f39c86e2c306ed18fb00a5fd83a4124fc50c470ef110c5115d25f4245cc976`  
		Last Modified: Thu, 21 Oct 2021 22:15:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a456ac48e2ca1123980e989c31fe5b540ff1b952fbb58dd31b06dc03257e6675`  
		Last Modified: Wed, 17 Nov 2021 01:17:59 GMT  
		Size: 142.7 MB (142703276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b3d0c3ee757860ab627028ba76b0c05731ca1a9be31cdf6a3aceb0c99aac71`  
		Last Modified: Wed, 17 Nov 2021 01:16:04 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7830aecd6bc74d5e668fec73426b77fd5e4ba5fd43f1f03a34b28dd1125cff21`  
		Last Modified: Wed, 17 Nov 2021 01:16:04 GMT  
		Size: 2.1 KB (2117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; s390x

```console
$ docker pull nextcloud@sha256:e41be086f9bf3481dc548f5f12c78ea833a15955b510f24766535bf7cddf3f77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304140174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85abb34cb72873a40b8f89d887128be9f029965731143f0ffd3af6b702b77f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:42:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Oct 2021 01:42:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Oct 2021 01:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 01:42:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Oct 2021 01:42:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 12 Oct 2021 01:46:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Oct 2021 01:46:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Oct 2021 01:47:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Oct 2021 01:47:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Oct 2021 01:47:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 14 Oct 2021 19:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 19:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 19:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 20:20:15 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 21 Oct 2021 15:48:26 GMT
ENV PHP_VERSION=8.0.12
# Thu, 21 Oct 2021 15:48:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Thu, 21 Oct 2021 15:48:26 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Thu, 21 Oct 2021 15:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 21 Oct 2021 15:48:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:51:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Oct 2021 15:51:20 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:51:20 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Oct 2021 15:51:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Oct 2021 15:51:20 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Oct 2021 15:51:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 21 Oct 2021 15:51:21 GMT
WORKDIR /var/www/html
# Thu, 21 Oct 2021 15:51:21 GMT
EXPOSE 80
# Thu, 21 Oct 2021 15:51:21 GMT
CMD ["apache2-foreground"]
# Thu, 21 Oct 2021 17:43:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 21 Oct 2021 17:43:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 Oct 2021 17:43:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 Oct 2021 17:44:44 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 17:44:45 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 21 Oct 2021 17:44:45 GMT
VOLUME [/var/www/html]
# Thu, 21 Oct 2021 17:44:46 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 16 Nov 2021 23:45:17 GMT
ENV NEXTCLOUD_VERSION=22.2.3
# Tue, 16 Nov 2021 23:45:47 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 16 Nov 2021 23:45:54 GMT
COPY multi:5c7d3e21c40c6f3326b9c24bb148355014771883d3bc821f8ada4fed6795cbb4 in / 
# Tue, 16 Nov 2021 23:45:55 GMT
COPY multi:f5bf72b2753669604b49ffdbd465aed9c49b21bdbd491f0b0d1cff5d5260de8c in /usr/src/nextcloud/config/ 
# Tue, 16 Nov 2021 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Nov 2021 23:45:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e93f54c1a4ac2c0a445018626dbf2035ae9fff49f85693b56f619e876603022`  
		Last Modified: Tue, 12 Oct 2021 03:44:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a448f945ae4e9abe53c27b72c40f075c61a2ff21977f7b57567f443ad7dee68b`  
		Last Modified: Tue, 12 Oct 2021 03:44:34 GMT  
		Size: 71.6 MB (71618360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3bf3e5f5ecd4bafce85def29ee5490f29b810e95829c3702cc4157280350e6`  
		Last Modified: Tue, 12 Oct 2021 03:44:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fa8915dfded42c17fc2ad80a47a873711c8d6200aebee325a829c59c4f6d62`  
		Last Modified: Tue, 12 Oct 2021 03:44:55 GMT  
		Size: 19.1 MB (19052069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed0ccfb17f6bd74cac8f31177eeda092942c5553a73e2168a9dd660804dce37`  
		Last Modified: Tue, 12 Oct 2021 03:44:53 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25b2206fa558b0b5f7444116a8a5f096797010e47f17c377157fdbcd748edab`  
		Last Modified: Tue, 12 Oct 2021 03:44:53 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e762c28f3d4972617f6567a866a41ebc3138a8f5e529bcbfc6895ae393de1e`  
		Last Modified: Thu, 21 Oct 2021 16:35:14 GMT  
		Size: 11.1 MB (11052645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ffabd5194bf6af7acb64636b4222681b3539db37b237ff14888c2ad13d2fe5`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0725bb937831d552ed9a1c43445518e3c84610967d8ee4b9b052adca4bebf16f`  
		Last Modified: Thu, 21 Oct 2021 16:35:14 GMT  
		Size: 13.4 MB (13449698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2c987ba1b5c5e5b452700b94cc987768eea52a14eba1253d0885c8859a7e49`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36af39b1f787efafb536b92efac04d4d6e1df9a2a8646b8edc5447efcd430e4`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d490b03075820f7a74ffd18e11c710dbd6b4ef8428e106231c969385b0d908`  
		Last Modified: Thu, 21 Oct 2021 16:35:12 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7fa481a2be242f907cde82d973d30b5bb44b3c5357780cc96c21abbfd2b20`  
		Last Modified: Thu, 21 Oct 2021 17:51:56 GMT  
		Size: 1.7 MB (1658889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9753405bf57cbcba2d611b407c6aee7d876bb99c534ec98ea2d9b2b6db62bb`  
		Last Modified: Thu, 21 Oct 2021 17:51:58 GMT  
		Size: 15.0 MB (14956528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb1a8bdfa2388019eba62546cc29d66010cfc588c315c6a996b8c656a02f843`  
		Last Modified: Thu, 21 Oct 2021 17:51:55 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5878eacbc66f33155a04e60bb7cb21ecad44cc6bf4330f12422b7fb2b6910f27`  
		Last Modified: Thu, 21 Oct 2021 17:51:55 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919cf1d094255eafad1cd8cc00a99a0d61f9652403e38fc263ff2bb1dcf1144`  
		Last Modified: Tue, 16 Nov 2021 23:51:08 GMT  
		Size: 142.7 MB (142699429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846f323a75d3befec99c141961984b4800c622147a86b1350a80253686899d9a`  
		Last Modified: Tue, 16 Nov 2021 23:50:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ff813ad838d4888e089c261e514ec3c13c9156f620ac432c32ce58c7c15f53`  
		Last Modified: Tue, 16 Nov 2021 23:50:52 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
