## `monica:4-apache`

```console
$ docker pull monica@sha256:54f92793b3ba19e87840c60ddeea67d4b2a4e3c1e00b66dbed7408594c2cd0f9
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

### `monica:4-apache` - linux; amd64

```console
$ docker pull monica@sha256:d261b510a7ae343f226159df3e0676b2e320a5653b245737f24d70f21121fbae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198484354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926e6860e9b25983f064776f50ca56533d701a72d9e128ea7d648fb782129234`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:37:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:37:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:37:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:37:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:41:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 04:41:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 04:41:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 04:41:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 04:41:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 04:41:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:41:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:41:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 05:34:17 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 06:00:47 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 06:00:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 06:00:47 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 06:00:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 06:00:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 06:04:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 06:04:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 06:04:04 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 06:04:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 06:04:04 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 06:04:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 06:04:04 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 06:04:04 GMT
EXPOSE 80
# Wed, 03 May 2023 06:04:04 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 03:48:01 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Thu, 04 May 2023 03:48:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:49:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:49:28 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Thu, 04 May 2023 03:49:28 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Thu, 04 May 2023 03:49:28 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Thu, 04 May 2023 03:49:29 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Thu, 04 May 2023 03:49:29 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Thu, 04 May 2023 03:49:29 GMT
WORKDIR /var/www/html
# Thu, 04 May 2023 03:49:30 GMT
ENV MONICA_VERSION=v4.0.0
# Thu, 04 May 2023 03:49:30 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Thu, 04 May 2023 03:49:45 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:49:46 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Thu, 04 May 2023 03:49:46 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Thu, 04 May 2023 03:49:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07353b772b5e325bf0abf03512cfaebe590a14a0858cf0ec2740b5ab055a31a7`  
		Last Modified: Wed, 03 May 2023 06:50:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5908153120ba6d8988feadd5f6a8c68a281970ad001ac3be0f5bc9dc030b5c4d`  
		Last Modified: Wed, 03 May 2023 06:51:01 GMT  
		Size: 91.6 MB (91635527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8681ad2eeea6fa7d3aed97bcd471bddff6b4932f405ecb84452c3d2522390e2a`  
		Last Modified: Wed, 03 May 2023 06:50:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92711ce78973323920b717b53e3a3e197c7b958c6e1a1be2a69b72718519c96a`  
		Last Modified: Wed, 03 May 2023 06:51:31 GMT  
		Size: 19.2 MB (19248134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1c5be6427ed0108e9859238ab41d37f43b792c65758e165f1cb957e7c4ab45`  
		Last Modified: Wed, 03 May 2023 06:51:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d02a81768ed9803772d4654c2b55b24c54d1200a872fccc3b689b8dd84cebd9`  
		Last Modified: Wed, 03 May 2023 06:51:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8420254580a520be8b0663de18936c453fafd971fc4704648e8eb110ffdc8f2`  
		Last Modified: Wed, 03 May 2023 06:59:20 GMT  
		Size: 12.1 MB (12123147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd27a4d09cf13bc7195acae19e654123f849c057c9f2f81743243541bed0f67`  
		Last Modified: Wed, 03 May 2023 06:59:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c35a490e4ffc0bde9cfa46e8ef5d6613f2aca5e586badfca9cba507a5dede`  
		Last Modified: Wed, 03 May 2023 06:59:19 GMT  
		Size: 11.1 MB (11059178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a85b880f671df5ae95d09b77a89e1498ba3ba7c14310f2f9547b351ca8a1f7`  
		Last Modified: Wed, 03 May 2023 06:59:17 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824952b7d7d797048bebe70730e7727f12f08c940273e0b5ff8376f45d333753`  
		Last Modified: Wed, 03 May 2023 06:59:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a39856c44f2dc0cfb9744bc050d0ec79be9166f3703659d25aac3ce301aaf5a`  
		Last Modified: Wed, 03 May 2023 06:59:17 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2130350c78120f6b5bb8a0f76b9d9fa2da0166e3767d294256160676eab19a2b`  
		Last Modified: Thu, 04 May 2023 03:52:00 GMT  
		Size: 1.4 MB (1386325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506103498bcb435f20888fdb7b5fffb6b5fb3bcc9faa59fb0190acae48939b3b`  
		Last Modified: Thu, 04 May 2023 03:52:00 GMT  
		Size: 4.2 MB (4151730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5b5d9d616f3423702ff3c011cab32d1664e7d8a89346a0814c0682cae7ea4`  
		Last Modified: Thu, 04 May 2023 03:51:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66d01ab1af73f0ae11298a6fede43097b6d859b8392ed4e3f47e21cb44a4ff6`  
		Last Modified: Thu, 04 May 2023 03:51:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96fd091cd4d1c1bdadcd6f45d91ecea9d53e98eff395298f812ba7fb130aa7e`  
		Last Modified: Thu, 04 May 2023 03:51:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ca964868b67ecd06718d10450b20f2c4635950812ce326dad6d62c0286bc4f`  
		Last Modified: Thu, 04 May 2023 03:51:58 GMT  
		Size: 8.3 KB (8303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6921fd8c9ee0d7bab99a5437d3460692a58caefd40fc54ac914520e1370dedd`  
		Last Modified: Thu, 04 May 2023 03:52:04 GMT  
		Size: 27.5 MB (27459420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77328c9e0845ac5be6ff14d8ec35ee16d53d0fbaf7f274419a3b05a18dd81075`  
		Last Modified: Thu, 04 May 2023 03:51:57 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; arm variant v5

```console
$ docker pull monica@sha256:eafa758af3eb9ec41e1257a454698bcee2c9c0152991f5e813e171fb4f108953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (176030022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a2fb968f7aaac179c8bb5af623f2f449c364b0d83156aab16cc5104c3720f9`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 22:48:53 GMT
ADD file:ca82c0d9094c1022a00b5f2157a02e1a9032aafc357a41c76c6b60bd74d25395 in / 
# Tue, 02 May 2023 22:48:53 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:52:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:52:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:53:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:57:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 04:57:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 04:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 04:57:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 04:57:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 04:57:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:57:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:57:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 05:30:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 05:40:07 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 05:40:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 05:40:08 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 05:40:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 05:40:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 05:42:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 05:42:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 05:42:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 05:42:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 05:42:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 05:42:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 05:42:44 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 05:42:44 GMT
EXPOSE 80
# Wed, 03 May 2023 05:42:44 GMT
CMD ["apache2-foreground"]
# Wed, 03 May 2023 12:53:27 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Wed, 03 May 2023 12:53:33 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:55:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:55:04 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Wed, 03 May 2023 12:55:04 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Wed, 03 May 2023 12:55:05 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Wed, 03 May 2023 12:55:05 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Wed, 03 May 2023 12:55:06 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Wed, 03 May 2023 12:55:06 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 12:55:06 GMT
ENV MONICA_VERSION=v4.0.0
# Wed, 03 May 2023 12:55:06 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Wed, 03 May 2023 12:55:25 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:55:26 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Wed, 03 May 2023 12:55:26 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Wed, 03 May 2023 12:55:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eb6ee5d3f82142e70aca665cea92048b1a46ff1aa5c5be47a04c27a471470c07`  
		Last Modified: Tue, 02 May 2023 22:51:25 GMT  
		Size: 28.9 MB (28903418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85385d8a3476710ef72295538768f9c56689b7564ab9659e81ba54b2c44cd6ac`  
		Last Modified: Wed, 03 May 2023 05:58:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055ef3089b9a2f598b1acf9be9ce3f9c8ca52737a33b747346c1d95163280eb`  
		Last Modified: Wed, 03 May 2023 05:58:46 GMT  
		Size: 73.7 MB (73687109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce127d0f710a63a0c4f56d4db41b96c20ef29e12706dd814ad1791a03d4e78`  
		Last Modified: Wed, 03 May 2023 05:58:33 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5128568fc52dd737c8c7c6e4619d2d953f7823880670051fb58a3cd97f4f142f`  
		Last Modified: Wed, 03 May 2023 05:59:16 GMT  
		Size: 18.5 MB (18548530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3ea7ea903f65a529fc14b10916ebd2596aeab47d1938317742b4cd4879d69b`  
		Last Modified: Wed, 03 May 2023 05:59:12 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8260da688e16d2b01fda95e7d18674e0b415261617c9ab6ec78996b1015add03`  
		Last Modified: Wed, 03 May 2023 05:59:12 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e0b396472522762b055fcf7dbecf3b22da490efd1743ce5277bc4ac612090f`  
		Last Modified: Wed, 03 May 2023 06:03:44 GMT  
		Size: 12.1 MB (12121351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435fcb5341ccfe5bc99d4018eb3dd65d8adc9cbfb55f8ec986caa7f1d9cf2fc9`  
		Last Modified: Wed, 03 May 2023 06:03:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e12e8eda202eb6d8256094f736bb7e5d044537e1b77211105a72ca91b6d5ac`  
		Last Modified: Wed, 03 May 2023 06:03:44 GMT  
		Size: 10.1 MB (10082369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef1af05a7d0082122dda402d59e75e79e3cb01e05820a845bcf32eb5456866e`  
		Last Modified: Wed, 03 May 2023 06:03:41 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd51294d4a6f5b2ef4ba367ba010cb5924663c76ec94a568555e77c773dbf6f9`  
		Last Modified: Wed, 03 May 2023 06:03:41 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9fd819b9f20e06073de204394e2044b1c1096641b7ba489169ad3a924165ad`  
		Last Modified: Wed, 03 May 2023 06:03:41 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8109ca849f12995a0e1e7fe4e9831e6902e3ec84c1a8b1d220b1d2905afa5d87`  
		Last Modified: Wed, 03 May 2023 12:58:08 GMT  
		Size: 1.3 MB (1341022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ebab2efbba2eca118fb66ac0c779c4ce15d2ef213a4bb0dd55edad51e3bfc`  
		Last Modified: Wed, 03 May 2023 12:58:08 GMT  
		Size: 3.9 MB (3870416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8946cc781c2ffa45222437835d7f0c93359d9291181521ef362de68a139f75a`  
		Last Modified: Wed, 03 May 2023 12:58:07 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc132a7d8d5e5e575f1fb21797ee57fef0435665a3abbdae13edc4978c6b4a81`  
		Last Modified: Wed, 03 May 2023 12:58:05 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53de0450276130a43db6f6f43da59a97bf236e191288cac558b002a12db5cc7`  
		Last Modified: Wed, 03 May 2023 12:58:05 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f498861f54c744a984b7a713288d26cf9b64b9d8339db9195cdd5146428756`  
		Last Modified: Wed, 03 May 2023 12:58:05 GMT  
		Size: 8.3 KB (8302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038a86cb9088945bcebb760778e30534d9e71563ae7ca36eb1df2d3dff428edf`  
		Last Modified: Wed, 03 May 2023 12:58:13 GMT  
		Size: 27.5 MB (27458439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7720f1a0cd51ae4fc4880b46a6b4461bbe7b69be50c57f5ea17004db346d1`  
		Last Modified: Wed, 03 May 2023 12:58:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; arm variant v7

```console
$ docker pull monica@sha256:327659adee52ee21d801dcd8bcaaa7ce882f0b33202ddea0142537439a60d575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167986290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00e99f7bee3632fe99fa45a2e9f40795b9fbf3e7febaddc785e694c6fcdff33`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 06:02:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 06:02:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 06:02:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 06:02:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 06:02:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 06:05:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 06:05:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 06:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 06:05:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 06:05:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 06:05:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:05:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:05:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 06:46:15 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 07:05:51 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 07:05:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 07:05:51 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 07:06:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 07:06:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 07:08:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 07:08:14 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 07:08:15 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 07:08:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 07:08:15 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 07:08:15 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 07:08:15 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 07:08:15 GMT
EXPOSE 80
# Wed, 03 May 2023 07:08:16 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 04:40:45 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Thu, 04 May 2023 04:40:49 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:42:12 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:42:13 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Thu, 04 May 2023 04:42:13 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Thu, 04 May 2023 04:42:14 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Thu, 04 May 2023 04:42:14 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Thu, 04 May 2023 04:42:15 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Thu, 04 May 2023 04:42:15 GMT
WORKDIR /var/www/html
# Thu, 04 May 2023 04:42:15 GMT
ENV MONICA_VERSION=v4.0.0
# Thu, 04 May 2023 04:42:15 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Thu, 04 May 2023 04:42:32 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:42:33 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Thu, 04 May 2023 04:42:33 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Thu, 04 May 2023 04:42:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4223092dddf6040b9cb3d66826248ca3c50557af6320203e8a40b6e549bb0f2c`  
		Last Modified: Wed, 03 May 2023 07:46:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922e3f7fe606e6c4954d1d9e944c9f9e610ff10a76127e6d51a955e8cc42772b`  
		Last Modified: Wed, 03 May 2023 07:46:36 GMT  
		Size: 69.3 MB (69320181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3bf68a94eff4021eeb6ae2522f556ef8567c37e2fb6f1155469a278208edf3`  
		Last Modified: Wed, 03 May 2023 07:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70939fb624f471cb7fcaaa48c91697a6b8745045cfa06a955b53b7517a5f26c3`  
		Last Modified: Wed, 03 May 2023 07:47:00 GMT  
		Size: 18.0 MB (18007946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2479125a48d14056528c5be7d389f2fb2b0977398a03fc50730f41f2944a26`  
		Last Modified: Wed, 03 May 2023 07:46:57 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c698e83c34140865f214984aca5d4ab163aa1df710e78e5df4fb286f2043e9e`  
		Last Modified: Wed, 03 May 2023 07:46:57 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a45c4a089e1491da4022220073a7e7e4099dd401cc24f6ccadbfbdd3c0febe`  
		Last Modified: Wed, 03 May 2023 07:54:49 GMT  
		Size: 12.1 MB (12121339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afdf91bc313704aa04b3cce5a85d6f585442467f348299ee4d356d71a1d5bc9`  
		Last Modified: Wed, 03 May 2023 07:54:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a255f18e33fa30fbfd5e35687ea538d3d806ea894a3e5b2abdd87506b091346d`  
		Last Modified: Wed, 03 May 2023 07:54:48 GMT  
		Size: 9.6 MB (9551940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aa574475c27484f09de000d48b41f5acfa9fcea580460d42713c77d3b83174`  
		Last Modified: Wed, 03 May 2023 07:54:46 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b61d0e400f88e5a003fa6264fcef07eae576e5f4c56ed8d74e9298719edca`  
		Last Modified: Wed, 03 May 2023 07:54:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db2027fdcdde045547cc95d977c463f01fc85c02e6811be6b9521f2b4a6619e`  
		Last Modified: Wed, 03 May 2023 07:54:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59127795ccccdc2e8b6f00e6226e520c745736b17e7681d9f6229d60d0bd075`  
		Last Modified: Thu, 04 May 2023 04:44:43 GMT  
		Size: 1.2 MB (1220840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a5336504cbb40b42c443b6883a7a4d40127096c53daafdf9eb2d6061e4a99c`  
		Last Modified: Thu, 04 May 2023 04:44:44 GMT  
		Size: 3.7 MB (3723516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e734f8fe6d71d112cd1ac554e7464962704be7fb3d3b42a890f316307deec5ac`  
		Last Modified: Thu, 04 May 2023 04:44:43 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44d76bd9d57f860ff82c9bd79f0a195d70c7219be95deb6de782239d5daf9f5`  
		Last Modified: Thu, 04 May 2023 04:44:41 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46754725aa91cd791ab99a5dac35d159b63cd7b24f0063ed9d27b8716f8ee44e`  
		Last Modified: Thu, 04 May 2023 04:44:41 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a3d5ad141de8c1f3090e9c4769cd891659a55dc15f175ac6414da06dc69709`  
		Last Modified: Thu, 04 May 2023 04:44:41 GMT  
		Size: 8.3 KB (8303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7260e96efcdf55b500e087e8f2646b31cf88a6e248b8a0810c9a07715030945c`  
		Last Modified: Thu, 04 May 2023 04:44:49 GMT  
		Size: 27.5 MB (27458506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db18e211bea4000480dfc2bef6284b8ef40745a62cc675ea35262468f43bdf3b`  
		Last Modified: Thu, 04 May 2023 04:44:41 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; arm64 variant v8

```console
$ docker pull monica@sha256:c55fb387ece656f8c056da582aac28b4543bf4d1868e598151205f795fbd217e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192299023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da52564b798feb3d77e330c8986ce6f661c31a1775f32cdaa8a45b5d7d4ae3c`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 03:52:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 03:52:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 03:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:52:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 03:52:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 03:56:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 03:56:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 03:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 03:56:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 03:56:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 03:56:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 03:56:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 03:56:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 04:45:47 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 05:10:08 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 05:10:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 05:10:08 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 05:10:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 05:10:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 05:13:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 05:13:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 05:13:10 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 05:13:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 05:13:10 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 05:13:10 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 05:13:11 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 05:13:11 GMT
EXPOSE 80
# Wed, 03 May 2023 05:13:11 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 00:36:21 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Thu, 04 May 2023 00:36:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:37:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:37:40 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Thu, 04 May 2023 00:37:40 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Thu, 04 May 2023 00:37:40 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Thu, 04 May 2023 00:37:41 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Thu, 04 May 2023 00:37:41 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Thu, 04 May 2023 00:37:41 GMT
WORKDIR /var/www/html
# Thu, 04 May 2023 00:37:42 GMT
ENV MONICA_VERSION=v4.0.0
# Thu, 04 May 2023 00:37:42 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Thu, 04 May 2023 00:37:56 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:37:57 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Thu, 04 May 2023 00:37:57 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Thu, 04 May 2023 00:37:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3582e155c24272674265389c3b317b84bec7ca237a6761ee690aed30a1c5ec9`  
		Last Modified: Wed, 03 May 2023 05:50:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313de6edf03aac188b999f642b424cdc014f9f45e218d5ad620a727ef81fa7e1`  
		Last Modified: Wed, 03 May 2023 05:51:02 GMT  
		Size: 86.9 MB (86928311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a576c500430404ceffd53e7ce6f2898b260e011e85c77bdabd75342c1a6a54`  
		Last Modified: Wed, 03 May 2023 05:50:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c4246fc75d4a1eefb130895fc367d8150e7076da4e329f94094a45c81cf4e`  
		Last Modified: Wed, 03 May 2023 05:51:26 GMT  
		Size: 19.2 MB (19170211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc677cfb25a8634144c25b4c4f43c1173f08ca1eb16b4f3ae53aa11bc62040`  
		Last Modified: Wed, 03 May 2023 05:51:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca53ccc29d8c43aeff9c96a48096d009ccf0ee902bf0b5076defe39003f2a0e`  
		Last Modified: Wed, 03 May 2023 05:51:24 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4c5c8e5da5ee12d25cc66088d25127c2aae0c6c8ca98e66c5005744849bb09`  
		Last Modified: Wed, 03 May 2023 05:58:52 GMT  
		Size: 12.1 MB (12122246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f2f08835715328d465bff0833e5d47a7040ccc6e81173bcbdfdc590155c1f3`  
		Last Modified: Wed, 03 May 2023 05:58:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1543c77ab1471adf87f1e747fcb65dd2848dcdd5a2e57f1d4fbfb85740ee15ad`  
		Last Modified: Wed, 03 May 2023 05:58:51 GMT  
		Size: 11.1 MB (11129781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254506894587666a75a9f0500cd0d9a57971a3a45a99f54f3a471e1b0601572`  
		Last Modified: Wed, 03 May 2023 05:58:50 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddcbe89ca469c5d5ee0ad97571f8e481adfc0cc0e47fd850342bdfd4d4c93e`  
		Last Modified: Wed, 03 May 2023 05:58:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498e094437d7f9d3c9d688fd05796c57761c88fe959a480e770c1cdbb6f9855d`  
		Last Modified: Wed, 03 May 2023 05:58:50 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75df9ad8784a8f2b94ea64a3227d77ca7fe2aaf35026d0d0a90d04169f98591`  
		Last Modified: Thu, 04 May 2023 00:40:04 GMT  
		Size: 1.3 MB (1331234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c043194e448c4e4b05b911a164aa022485a3f0bf8f876947c88f28ffad44c`  
		Last Modified: Thu, 04 May 2023 00:40:04 GMT  
		Size: 4.1 MB (4088270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fc8239c2d9cad73948d262d24ccfa5bb1252fc501aab65128cd4dda3b35641`  
		Last Modified: Thu, 04 May 2023 00:40:03 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bb8d88ebd84fb325cf973162e24be0700cfd3a2c0c492510af7b6371ea6311`  
		Last Modified: Thu, 04 May 2023 00:40:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae595fd542b6a99df5f60fafc418d4ad41c5ba23038d825ea9ac0c6cedbd027`  
		Last Modified: Thu, 04 May 2023 00:40:01 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677b6215913ea2e1777b5d4b987dfe56ef9d3eb088bb6245850e03ffffc15b3`  
		Last Modified: Thu, 04 May 2023 00:40:01 GMT  
		Size: 8.3 KB (8303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71b1b7cafc6052b47ca5fce0410e851183be137a15a0bbe9696058ef6768f29`  
		Last Modified: Thu, 04 May 2023 00:40:06 GMT  
		Size: 27.5 MB (27458879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfda2a9b00a7e931d3af8954ce45cbc507669178774b63f3e3f5cba86b5eab08`  
		Last Modified: Thu, 04 May 2023 00:40:02 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; 386

```console
$ docker pull monica@sha256:d5f97f2519db5be38bc2b3af61360c246cd6dd587728b3e5ca8c4d9136f76437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201330836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fc82644c9566dbd773186345e240a018ed760710b511151d87c85122ed764a`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 May 2023 00:00:58 GMT
ADD file:caea439e2dbe0148904e3b9a0c5a843d2d0b7c196725d2b41790594e64dcdce8 in / 
# Wed, 03 May 2023 00:00:58 GMT
CMD ["bash"]
# Wed, 03 May 2023 08:55:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 08:55:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 08:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 08:56:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 08:56:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 09:01:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 09:01:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 09:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 09:01:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 09:01:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 09:01:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 09:01:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 09:01:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 10:26:24 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 11:07:47 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 11:07:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 11:07:47 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 11:08:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 11:08:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 11:13:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 11:13:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 11:13:03 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 11:13:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 11:13:04 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 11:13:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 11:13:04 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 11:13:04 GMT
EXPOSE 80
# Wed, 03 May 2023 11:13:04 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 03:27:27 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Thu, 04 May 2023 03:27:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:29:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:29:20 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Thu, 04 May 2023 03:29:20 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Thu, 04 May 2023 03:29:20 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Thu, 04 May 2023 03:29:21 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Thu, 04 May 2023 03:29:22 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Thu, 04 May 2023 03:29:22 GMT
WORKDIR /var/www/html
# Thu, 04 May 2023 03:29:22 GMT
ENV MONICA_VERSION=v4.0.0
# Thu, 04 May 2023 03:29:22 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Thu, 04 May 2023 03:29:42 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:29:44 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Thu, 04 May 2023 03:29:44 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Thu, 04 May 2023 03:29:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:10b34014bd1c165cc57a10e7492f17dce658513b7329319fe6c193c85bf752db`  
		Last Modified: Wed, 03 May 2023 00:05:12 GMT  
		Size: 32.4 MB (32388208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e767304c8a25a06c5180cd0487b1d298c8eb93b9276d7f8a33605daeec5deed`  
		Last Modified: Wed, 03 May 2023 12:27:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8469e5ef909b43afbcce2cb261155375a3b3f423dadb11383bf91b8d037358f`  
		Last Modified: Wed, 03 May 2023 12:28:07 GMT  
		Size: 92.7 MB (92719962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d946dbb11b755f5978864d6cb1f395dc513c314f5d182df53bd573895bbeb7a5`  
		Last Modified: Wed, 03 May 2023 12:27:47 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924158f9311822c03627e43631de70ccf581b97a0430f7b72985bb4724547e87`  
		Last Modified: Wed, 03 May 2023 12:28:33 GMT  
		Size: 19.7 MB (19737280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace747d85a92d8e6182f02d61b25843d51b0e593121c7df2951fb700f4a49e55`  
		Last Modified: Wed, 03 May 2023 12:28:29 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb964761efe81d0142e55a3784ad2802e32884c20d5859d2443482372701fa`  
		Last Modified: Wed, 03 May 2023 12:28:29 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239b8075cc4839de607fcfc45aa1d75f9c61cde146ebe823305912c958b60b85`  
		Last Modified: Wed, 03 May 2023 12:37:18 GMT  
		Size: 12.1 MB (12122329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f031b5b803efaa49aa4c4ffeff55de0b5619a0838530cde72ece79f405fd3958`  
		Last Modified: Wed, 03 May 2023 12:37:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973cb526db77eeabcb461c668fd7eac75251cebf3a0ab2eb006566de2b6ded3`  
		Last Modified: Wed, 03 May 2023 12:37:18 GMT  
		Size: 11.3 MB (11289947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdadb2c249ee9adbf300fce9f8e9b72d3a2bdefe0cd21ae12835eb6b090a854`  
		Last Modified: Wed, 03 May 2023 12:37:14 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd63123cfc4e8322470e51bb37fadbdba8267862d46159445dcd3165d6bfc23`  
		Last Modified: Wed, 03 May 2023 12:37:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185f2c1f3941a63e359567de60e7bc2defe02a6c1c5a8d74cfeaeb653ca95ed`  
		Last Modified: Wed, 03 May 2023 12:37:14 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ea7cf7ac4f828c129953b4575e611868d07be784eddd677a9eed63e79fc966`  
		Last Modified: Thu, 04 May 2023 03:32:26 GMT  
		Size: 1.4 MB (1398354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7ab35c3113932dece30658983d45179ff342b10d0ccd01a3a4ef2e424469ee`  
		Last Modified: Thu, 04 May 2023 03:32:26 GMT  
		Size: 4.2 MB (4198500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec363eecd3429831f2f2c701c41e270a988da71c0786df9c604c3eecc3f9d3`  
		Last Modified: Thu, 04 May 2023 03:32:25 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1af95e72e1170037cf9c647f0c51c69c42c240c69fbacb40341c09bb442948`  
		Last Modified: Thu, 04 May 2023 03:32:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138c6d15e0514469d9f616736a47dc710aa3a5b55f0d7d6e4e8b00628f3f2c03`  
		Last Modified: Thu, 04 May 2023 03:32:23 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e53c0ca3a2cfd56cde77ab146ad0f21bbee64683a5b101ba5ed5b21d89871b2`  
		Last Modified: Thu, 04 May 2023 03:32:23 GMT  
		Size: 8.3 KB (8301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa511b941f143ef7fcdd694a3b861066357d1470e8d998df929540d2daa1ddc`  
		Last Modified: Thu, 04 May 2023 03:32:33 GMT  
		Size: 27.5 MB (27458884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45623c28bdd19592a14445ab777716a35cf26cd7b29cc668ee9c919bcd0517c4`  
		Last Modified: Thu, 04 May 2023 03:32:23 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; mips64le

```console
$ docker pull monica@sha256:2c76f68d6fe68e35aa7854aa2071414d58689f0059ccd0adfad9ff03fa1215ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175048367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4216403e7d18129a6ee28f1f5ce91ec0dd379be78f10ca39c2a5d2d333de1ea6`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 May 2023 23:49:45 GMT
ADD file:c3427ec4e3a2c988fdd372b529660d45ee105e317d6a964ce96f8f9009a3c21e in / 
# Tue, 02 May 2023 23:49:49 GMT
CMD ["bash"]
# Wed, 03 May 2023 00:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 00:10:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 00:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 00:12:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 00:12:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 00:27:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 00:27:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 00:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 00:28:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 00:28:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 00:28:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 00:29:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 00:29:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 02:25:38 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 03:22:43 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 03:22:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 03:22:50 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 03:23:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 03:23:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 03:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 03:37:45 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 03:37:52 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 03:37:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 03:37:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 03:38:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 03:38:06 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 03:38:10 GMT
EXPOSE 80
# Wed, 03 May 2023 03:38:14 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 05:25:22 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Thu, 04 May 2023 05:25:40 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 05:31:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 05:31:42 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Thu, 04 May 2023 05:31:46 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Thu, 04 May 2023 05:31:52 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Thu, 04 May 2023 05:31:58 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Thu, 04 May 2023 05:32:05 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Thu, 04 May 2023 05:32:08 GMT
WORKDIR /var/www/html
# Thu, 04 May 2023 05:32:12 GMT
ENV MONICA_VERSION=v4.0.0
# Thu, 04 May 2023 05:32:15 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Thu, 04 May 2023 05:33:40 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 05:33:49 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Thu, 04 May 2023 05:33:56 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Thu, 04 May 2023 05:34:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:498edd615f8781385e0d5246e189d80b5caceb207fe26608a12605d0a823d4df`  
		Last Modified: Tue, 02 May 2023 23:58:10 GMT  
		Size: 29.6 MB (29623482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9f275f462bc69ed3d423529b2c61717acf92ae94079820567546a9be7dfc90`  
		Last Modified: Wed, 03 May 2023 05:03:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144d8ba9239413b7073602141f7770aa1ecefc91eea8b88d6bef1e57cd24e721`  
		Last Modified: Wed, 03 May 2023 05:04:11 GMT  
		Size: 72.0 MB (72018435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926473715e8c6e64ac6be14864c39343324c6cd9496c16cf520fac2ee94cafda`  
		Last Modified: Wed, 03 May 2023 05:03:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287b54b2fc0e2ddfd944a13aed3214414be47643ec0dd994e526c66d6164caab`  
		Last Modified: Wed, 03 May 2023 05:04:50 GMT  
		Size: 18.9 MB (18947010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9724b961784537f2a20fe86f36e2cc87ce7aee7c70f18e9010c2d4814cc66346`  
		Last Modified: Wed, 03 May 2023 05:04:37 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceec3ed73b30dcb9b15eb29224da2ee99fb658f743acf7882099046b54abcfb9`  
		Last Modified: Wed, 03 May 2023 05:04:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac93df2830b0cfa8a5e4176d3d9ee83a250c8008fdd34565f4094a5ed61f5278`  
		Last Modified: Wed, 03 May 2023 05:11:55 GMT  
		Size: 11.9 MB (11906015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd551c1a4f1a599dcd4e33bd6547563c1b549a1f32765b67209dd9a96fbbbc2`  
		Last Modified: Wed, 03 May 2023 05:11:50 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b95cb897381c5d9d8a13c1d6b5f66a80cc302d0c66bdacfa28fd05e60b1d36`  
		Last Modified: Wed, 03 May 2023 05:11:57 GMT  
		Size: 10.2 MB (10214141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62085dc5fd70c411eed32a582b10ca289f0a900d373739ff86e3879b4089dbd`  
		Last Modified: Wed, 03 May 2023 05:11:50 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae1bf9a85856c9ffafcf5b24ec126532ff0fc95c18dd50f89c3496ea6cc973`  
		Last Modified: Wed, 03 May 2023 05:11:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b860dd358802640655985368bbb95a01313381285eb4ce026d7575a03d732126`  
		Last Modified: Wed, 03 May 2023 05:11:50 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb663184b43628baf45d6a6cfcbd1157f2eb96f4f1dda98e973c1a0982e6a0d`  
		Last Modified: Thu, 04 May 2023 05:43:18 GMT  
		Size: 1.2 MB (1246268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a115998e273c7746d27bb049959b8949fdcc50547ba9ab12ca81106e515a874`  
		Last Modified: Thu, 04 May 2023 05:43:20 GMT  
		Size: 3.8 MB (3838940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ce6a21efdcef78032df63cd41d58dbb71df74e94e72d9068a15b26f7a19e80`  
		Last Modified: Thu, 04 May 2023 05:43:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6952c4e2df2aca65796a5f0dd821dca0831670629423ac86e7b44e8cf03987e`  
		Last Modified: Thu, 04 May 2023 05:43:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664411c6b71db8a099e2774794e8efadd16d7a3932ede457bdea4cf007ba0cb1`  
		Last Modified: Thu, 04 May 2023 05:43:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e565410e3e5b5eb3f928e5dd949dbd96893f9c750cde722aa1a62333f81ae717`  
		Last Modified: Thu, 04 May 2023 05:43:15 GMT  
		Size: 8.3 KB (8308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a414d29936623090e8c69fb18a9284bd8314124670e6dd77e6cea36ed2512`  
		Last Modified: Thu, 04 May 2023 05:43:43 GMT  
		Size: 27.2 MB (27236811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60db257b04cd7b1a88e3a5fea04f82ed7cfc389afee5d21585651bb4fa46c1`  
		Last Modified: Thu, 04 May 2023 05:43:15 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; ppc64le

```console
$ docker pull monica@sha256:03ad4bab4f196929f882e4fbacb69987cbc6fc2900a27096b4a7b57e07a7354d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199394040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6466a1e108e886334e1b7e7af5cb788cf807cbba0a194c112ba804d9087b84b2`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 02:53:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 12 Apr 2023 02:53:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 12 Apr 2023 02:54:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 02:55:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 12 Apr 2023 02:55:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 12 Apr 2023 03:00:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 12 Apr 2023 03:00:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 12 Apr 2023 03:00:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 12 Apr 2023 03:00:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 12 Apr 2023 03:00:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 12 Apr 2023 03:00:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 03:00:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 03:00:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 12 Apr 2023 03:40:32 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 14 Apr 2023 18:11:50 GMT
ENV PHP_VERSION=8.1.18
# Fri, 14 Apr 2023 18:11:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Fri, 14 Apr 2023 18:11:50 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Fri, 14 Apr 2023 18:12:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 14 Apr 2023 18:12:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 14 Apr 2023 18:16:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 14 Apr 2023 18:16:29 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 14 Apr 2023 18:16:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 14 Apr 2023 18:16:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 14 Apr 2023 18:16:30 GMT
STOPSIGNAL SIGWINCH
# Fri, 14 Apr 2023 18:16:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 14 Apr 2023 18:16:31 GMT
WORKDIR /var/www/html
# Fri, 14 Apr 2023 18:16:31 GMT
EXPOSE 80
# Fri, 14 Apr 2023 18:16:31 GMT
CMD ["apache2-foreground"]
# Fri, 14 Apr 2023 20:40:56 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 14 Apr 2023 20:41:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 14 Apr 2023 20:43:58 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 14 Apr 2023 20:44:00 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 14 Apr 2023 20:44:01 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 14 Apr 2023 20:44:02 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Fri, 14 Apr 2023 20:44:03 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 14 Apr 2023 20:44:05 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 14 Apr 2023 20:44:05 GMT
WORKDIR /var/www/html
# Fri, 14 Apr 2023 20:44:05 GMT
ENV MONICA_VERSION=v4.0.0
# Fri, 14 Apr 2023 20:44:05 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Fri, 14 Apr 2023 20:44:39 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 14 Apr 2023 20:44:42 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 14 Apr 2023 20:44:42 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 14 Apr 2023 20:44:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881dab4e16a2b31707f063b4a6d06a7622c29a571e9941b45d4f1dbab9fa535`  
		Last Modified: Wed, 12 Apr 2023 04:52:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7112207942602cdd0c4444cb2cf85085ac4ac494a4140f7ad0d4b40bc5d9af2`  
		Last Modified: Wed, 12 Apr 2023 04:53:17 GMT  
		Size: 86.6 MB (86633054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc8a1d48af817593b6b8be59cd4822dcbbf90138a02afc42d1c359a66cef044`  
		Last Modified: Wed, 12 Apr 2023 04:52:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eebee4fe70939a7f850866922cd16aca329703d3398407739e4b38a6f027d89`  
		Last Modified: Wed, 12 Apr 2023 04:53:47 GMT  
		Size: 20.5 MB (20464162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb6aa8a531755afded14a8c4ba085e312d53bcaf78332aeafd1dd4d3d8dbc0`  
		Last Modified: Wed, 12 Apr 2023 04:53:42 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef12174c7227dbbeb6d056ac319756c11bf63363c72a33b9ab7899b9dfc7f097`  
		Last Modified: Wed, 12 Apr 2023 04:53:42 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c38e27804e7de781604fc7987995b611df38c6a144b877111134cb04e95ff00`  
		Last Modified: Fri, 14 Apr 2023 19:01:39 GMT  
		Size: 12.1 MB (12122982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b2d3d9d03551f7b0e4d7a786c89a9612a0aaed6dc9739c38c242de28cec0c3`  
		Last Modified: Fri, 14 Apr 2023 19:01:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f9b9401d9b048c57fcd45d13667c1760401834c81f5d480d7f94fed1b8b59b`  
		Last Modified: Fri, 14 Apr 2023 19:01:40 GMT  
		Size: 11.5 MB (11462631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5dddce9d56b1b4fa337645bcd5b1c5713358aed99710c505a83c95cf501945`  
		Last Modified: Fri, 14 Apr 2023 19:01:36 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be96b43a01486cbe7e5cbf79cd3e989b133d1fa4114756332c46998ee86994c0`  
		Last Modified: Fri, 14 Apr 2023 19:01:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087bbc8144cc96eb647c719e768a85951d09c41f6aeb2670cbb9313a594c0687`  
		Last Modified: Fri, 14 Apr 2023 19:01:36 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a564baee704e834b47bad921b62dffff265476899d9eb49988c90979733a2074`  
		Last Modified: Fri, 14 Apr 2023 20:52:37 GMT  
		Size: 1.5 MB (1507873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fd0dac6d1481a67abe1fe0af43715058081f3336ed502b46b5ec3abc1c4513`  
		Last Modified: Fri, 14 Apr 2023 20:52:38 GMT  
		Size: 4.4 MB (4434598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b0115f368c2334c1de5212b6cdb0e2f088ca741dc3888c1dcc39b6c30ef4f3`  
		Last Modified: Fri, 14 Apr 2023 20:52:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b38d3e532ec0511e553da63424d534524396002920629ecbe77556de5ac99`  
		Last Modified: Fri, 14 Apr 2023 20:52:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389f396ec39c26978a1d324575db3006ff67b11ff76755e89102fb980b923092`  
		Last Modified: Fri, 14 Apr 2023 20:52:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251cd5deb84517685dae487f2887083d0cea2d82f3f6fe6c37010680c812af1f`  
		Last Modified: Fri, 14 Apr 2023 20:52:34 GMT  
		Size: 8.3 KB (8303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb70e1b6525e30e00af4a13328dd06a694080cf649edc94e1ed48ed3fe2692f0`  
		Last Modified: Fri, 14 Apr 2023 20:52:47 GMT  
		Size: 27.5 MB (27459353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f381a8d15c8d98b29514a4c5c5ef642ee24a965ea1e27142d0cc619c9e355d`  
		Last Modified: Fri, 14 Apr 2023 20:52:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:4-apache` - linux; s390x

```console
$ docker pull monica@sha256:21cf49f980b019b37f6c875254c34a37b06fa2a907838c5a1552ebff68e353b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175547548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a82187cd67b1cbae90336d583be68fda028dd4c2ab393f65ac4d39d337e5637`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 May 2023 03:41:57 GMT
ADD file:7dcdb7d695d9510a1a7e1623776d63d56f7025bdd1702a13a3acd52af825b9c3 in / 
# Wed, 03 May 2023 03:41:59 GMT
CMD ["bash"]
# Wed, 03 May 2023 12:28:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 12:28:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 12:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:29:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 12:29:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 12:33:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 May 2023 12:33:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 May 2023 12:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 May 2023 12:34:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 May 2023 12:34:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 May 2023 12:34:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 12:34:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 12:34:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 13:13:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 May 2023 13:31:39 GMT
ENV PHP_VERSION=8.1.18
# Wed, 03 May 2023 13:31:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.18.tar.xz.asc
# Wed, 03 May 2023 13:31:39 GMT
ENV PHP_SHA256=f3553370f8ba42729a9ce75eed17a2111d32433a43b615694f6a571b8bad0e39
# Wed, 03 May 2023 13:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 13:31:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 13:34:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 13:34:37 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 May 2023 13:34:38 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 13:34:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 13:34:38 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 May 2023 13:34:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 May 2023 13:34:38 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 13:34:38 GMT
EXPOSE 80
# Wed, 03 May 2023 13:34:39 GMT
CMD ["apache2-foreground"]
# Thu, 04 May 2023 07:26:01 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Thu, 04 May 2023 07:26:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libwebp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         soap     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;         ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;             apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:04 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '*/5 * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Thu, 04 May 2023 07:27:04 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Thu, 04 May 2023 07:27:04 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > $PHP_INI_DIR/conf.d/memory-limit.ini
# Thu, 04 May 2023 07:27:05 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Thu, 04 May 2023 07:27:05 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Thu, 04 May 2023 07:27:05 GMT
WORKDIR /var/www/html
# Thu, 04 May 2023 07:27:06 GMT
ENV MONICA_VERSION=v4.0.0
# Thu, 04 May 2023 07:27:06 GMT
LABEL org.opencontainers.image.revision=e1a3e1315b1a92a5ff0ccab6c22ba9ded77a599e org.opencontainers.image.version=v4.0.0
# Thu, 04 May 2023 07:27:22 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:26 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Thu, 04 May 2023 07:27:26 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Thu, 04 May 2023 07:27:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8e4cb8eb5d7a86a02dfc1d3645e982def0fc1c20e1fd14d9c6736177d3887dfa`  
		Last Modified: Wed, 03 May 2023 03:44:59 GMT  
		Size: 29.6 MB (29642157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7039311ef77b804a6867c187f4e31e7b4489fd899d1e33e1be82b55aeec5058`  
		Last Modified: Wed, 03 May 2023 13:55:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f7a91cc134a44679fc67a325a5e92393aabc8331c299c922aa2538945e222c`  
		Last Modified: Wed, 03 May 2023 13:55:52 GMT  
		Size: 71.6 MB (71630105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6562325ea2cb0173d4a5d95a099f62aeddcf32b69d42020e16bb238583a626`  
		Last Modified: Wed, 03 May 2023 13:55:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c516462b4dbcc4350ab682f108bbe6b072d2490fe597fd6a9340fbceef176b67`  
		Last Modified: Wed, 03 May 2023 13:56:08 GMT  
		Size: 19.1 MB (19077671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddd35b1eab1b78359adbcde58ecf0d5aef38ef08a87ea613146f6d6cbdb1adf`  
		Last Modified: Wed, 03 May 2023 13:56:05 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5db7363519fbfac402b87b15937f641af2b29b768153c0bfb60037a478f722`  
		Last Modified: Wed, 03 May 2023 13:56:05 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc89e11d2fa1e1badd0f36f6bd17dde185a27e413f34ed8bb875f57e09795a`  
		Last Modified: Wed, 03 May 2023 13:59:30 GMT  
		Size: 12.1 MB (12121997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a158832d7991b8a82c1b7d8f442b95e452dc0f09cc092368cf5fd1b339646a7`  
		Last Modified: Wed, 03 May 2023 13:59:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1cd73703e2ad4c168afc3fd62dc7fb71c45c9fe8098312896f6738eb71bfb5`  
		Last Modified: Wed, 03 May 2023 13:59:30 GMT  
		Size: 10.2 MB (10198920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d84c5225a73174e73cf64f87f758a88b678c1adb0c6d5cac4ece8d05c7503fd`  
		Last Modified: Wed, 03 May 2023 13:59:28 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d979afef397a82e827da1d1bc32f52ddb8951678c151d6963ca00f020c7062a`  
		Last Modified: Wed, 03 May 2023 13:59:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5b03a1212a6335a0911ec3eee39149a77f58eeb0ae481398f0a8007712f39a`  
		Last Modified: Wed, 03 May 2023 13:59:28 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5ebff91d3a45eaed4cece29425108e3949890c880460404877e13bedb1d59`  
		Last Modified: Thu, 04 May 2023 07:29:21 GMT  
		Size: 1.3 MB (1349866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e59d04eb50799fcdd88974b9f480bdc4546258ee4439db7fd28b37826f318d`  
		Last Modified: Thu, 04 May 2023 07:29:22 GMT  
		Size: 4.1 MB (4050508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa40ee7edebd44fe80c786f4458104f0bf2a8db3ba87022a5835e6fa7fe2cdeb`  
		Last Modified: Thu, 04 May 2023 07:29:22 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c746c1cb5363d3c15a9892766c51b40e80daa03fc8cf11bdea0726f68c6538c`  
		Last Modified: Thu, 04 May 2023 07:29:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5879287ee821ea77841bb0cdc13a3fc28f2f20a555823cf81110895ef8beea74`  
		Last Modified: Thu, 04 May 2023 07:29:20 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a0352a0773da638959fdf3b2b94ed8cb6cf8720d4bd22bd38e6d8cf5de7e39`  
		Last Modified: Thu, 04 May 2023 07:29:20 GMT  
		Size: 8.3 KB (8302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d08bf6aa35ded9e9ed198fab0015ec4070a9fbdcf08f3e143cc48a26b447225`  
		Last Modified: Thu, 04 May 2023 07:29:26 GMT  
		Size: 27.5 MB (27458933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538394d10c926759c454b35b65919425099f0f411a02b5249a8690db3e38fced`  
		Last Modified: Thu, 04 May 2023 07:29:20 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
