## `nextcloud:apache`

```console
$ docker pull nextcloud@sha256:fc83f7c56116633a94952bae0061c46ed047b35fff42b830a1d8108805f83dcd
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

### `nextcloud:apache` - linux; amd64

```console
$ docker pull nextcloud@sha256:c65b3a099746f9168a594adc84f586a6a40719f50889d7814a6b68f6e183b26b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343397590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0cab9b7a843c56ebc413eacfb2e0622760f60d6770142677dd9c2deef7e37d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:08:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 07:08:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 07:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 07:09:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 07:09:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 07:12:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 07:12:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 07:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 07:12:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 07:12:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 07:12:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 07:12:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 07:12:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 07:39:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Oct 2022 07:39:51 GMT
ENV PHP_VERSION=8.1.11
# Wed, 05 Oct 2022 07:39:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 05 Oct 2022 07:39:51 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 05 Oct 2022 07:40:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 07:40:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 07:43:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 07:43:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 07:43:04 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 07:43:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 07:43:04 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 07:43:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 07:43:04 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 07:43:04 GMT
EXPOSE 80
# Wed, 05 Oct 2022 07:43:05 GMT
CMD ["apache2-foreground"]
# Wed, 19 Oct 2022 19:26:51 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 19 Oct 2022 19:26:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Oct 2022 19:26:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Oct 2022 19:29:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:29:46 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 19 Oct 2022 19:29:46 GMT
VOLUME [/var/www/html]
# Wed, 19 Oct 2022 19:29:47 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 19 Oct 2022 19:29:47 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 19 Oct 2022 19:30:38 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:30:39 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 19 Oct 2022 19:30:40 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 19 Oct 2022 19:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Oct 2022 19:30:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e83b070fd9716453dd96b679a05d9d11c1f66d95582736a8d809d73a3f70c0d`  
		Last Modified: Wed, 05 Oct 2022 08:51:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7793be89e9cdecbe7f44d7cdb803c08522f057e4fbdd2b0cc72019e378bb660`  
		Last Modified: Wed, 05 Oct 2022 08:52:06 GMT  
		Size: 91.6 MB (91633715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4220e0c033772bd27ff577c6cc30afe1cd81296bf0d58615a56a8923c07c655a`  
		Last Modified: Wed, 05 Oct 2022 08:51:52 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32ee0a815d231a64b4246375a30b7118a82d5b79313c2b38ea9a467c98a0189`  
		Last Modified: Wed, 05 Oct 2022 08:52:36 GMT  
		Size: 19.2 MB (19244850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89791c7bacac602b302faca96047cd9a37c3764395bfaf24565aac243ba099c3`  
		Last Modified: Wed, 05 Oct 2022 08:52:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263f74f407a4a6a8c3c2f5be972638b7bc8661b62e3d43e3164057335ec3389a`  
		Last Modified: Wed, 05 Oct 2022 08:52:33 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988d3c8c51bdf44d50b57ec2b7b0f48ed5f1bd532f07841ef36676ee192c6efd`  
		Last Modified: Wed, 05 Oct 2022 08:55:39 GMT  
		Size: 12.1 MB (12137376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c18ba5e6a3d5d25c059d664be07041a8166e9336a9ba7708b1d87e7bc4c2429`  
		Last Modified: Wed, 05 Oct 2022 08:55:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3500215877c1fb3c2a3712e2041f63c84507921bd6e54a6123fec2f619a9b`  
		Last Modified: Wed, 05 Oct 2022 08:55:38 GMT  
		Size: 11.0 MB (11037473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290516d677143edfe60643a15bd74e33d3c7135bfd00cfbe40ce03c5064119d1`  
		Last Modified: Wed, 05 Oct 2022 08:55:36 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ac13556272eca9274d40d4d227344a08f12a8186f6415124c522547dcf32a`  
		Last Modified: Wed, 05 Oct 2022 08:55:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12bcfd235820f3316afd932a2da0560b75c3d8b2163d6db8aa0ada85d61c0ec`  
		Last Modified: Wed, 05 Oct 2022 08:55:36 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd74ec2491a89230608d00866522463a979887c4a888848b614855f5d9d45e8`  
		Last Modified: Wed, 19 Oct 2022 19:39:24 GMT  
		Size: 1.7 MB (1701079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1a618323808a07669623d6b76d37290a5a1f8e7d8979dd7209d2a67de95181`  
		Last Modified: Wed, 19 Oct 2022 19:39:26 GMT  
		Size: 17.3 MB (17345384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469a803f0d4ccc99d10eec9004dfd021be8b976d71bc1600a5ab4dbdbd556fa0`  
		Last Modified: Wed, 19 Oct 2022 19:39:21 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6ae7fa5ad3690cbdf2de0c5f3baa688768bf8ae682de934f8dac2e2a2d6e42`  
		Last Modified: Wed, 19 Oct 2022 19:39:22 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330f6567ca86b51b00cc4a5e20d23e1997d94b90f64e335758fc01ac7ae2db09`  
		Last Modified: Wed, 19 Oct 2022 19:39:42 GMT  
		Size: 158.9 MB (158865389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525e78cb0dec44ed828f08cfa65e4e35e44f7131f8d319aaca1303dea879b3c9`  
		Last Modified: Wed, 19 Oct 2022 19:39:21 GMT  
		Size: 3.2 KB (3247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a75f4f2b03fc7f46625d43efc48251bded664c1d2daedbe06d6068fa56254`  
		Last Modified: Wed, 19 Oct 2022 19:39:21 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:47bbc8e728ab598612e93a8c802666f69f321ce7bfc588ddb3148fd8eb88641c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318925964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc669bb9cec4d5b78c14bafc1890e7a25f0578975289eb0b3f92b7543b881418`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 09:46:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 09:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:46:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 09:46:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 09:49:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 09:49:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 09:50:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 09:50:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 09:50:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 09:50:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 09:50:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 09:50:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 10:03:02 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 25 Oct 2022 10:15:34 GMT
ENV PHP_VERSION=8.1.11
# Tue, 25 Oct 2022 10:15:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Tue, 25 Oct 2022 10:15:35 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Tue, 25 Oct 2022 10:15:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 10:15:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 10:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 10:18:33 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Oct 2022 10:18:34 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 10:18:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 10:18:34 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Oct 2022 10:18:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Oct 2022 10:18:35 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 10:18:35 GMT
EXPOSE 80
# Tue, 25 Oct 2022 10:18:35 GMT
CMD ["apache2-foreground"]
# Tue, 25 Oct 2022 18:44:46 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 25 Oct 2022 18:44:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 25 Oct 2022 18:44:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 25 Oct 2022 18:49:50 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:49:52 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 25 Oct 2022 18:49:52 GMT
VOLUME [/var/www/html]
# Tue, 25 Oct 2022 18:49:54 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 25 Oct 2022 18:49:54 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Tue, 25 Oct 2022 18:51:09 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:51:11 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Tue, 25 Oct 2022 18:51:13 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 25 Oct 2022 18:51:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 18:51:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4749c44436d7146c25d70115fa5b5e34b26645fc0cef9f2405abe2e0bd76fa`  
		Last Modified: Tue, 25 Oct 2022 10:53:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63658c2c058585abf8be658a5b892c1d6478a785d529b4d50cdf4e10208f818`  
		Last Modified: Tue, 25 Oct 2022 10:53:52 GMT  
		Size: 73.7 MB (73687743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0da83c90ac4d066406fd53d564c017329ef784939a899d0ff87990f6749dfa5`  
		Last Modified: Tue, 25 Oct 2022 10:53:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78402fcc0964bee4c8b4bc81fc9df86ab450a7fd7ac800e0152f7c012fada2ec`  
		Last Modified: Tue, 25 Oct 2022 10:54:33 GMT  
		Size: 18.6 MB (18554370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b89f4fa9342ec543164d9ae5c78bffd707973f7f58d3da93ef38c9ca8080da3`  
		Last Modified: Tue, 25 Oct 2022 10:54:29 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69ccef4195ea81f0b1e36510aefc83bbd9771507a2affa186cb29a80486343`  
		Last Modified: Tue, 25 Oct 2022 10:54:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fbf191382c660e677768b071e78528db219b5557c6dcdabd7c3c765c1855a`  
		Last Modified: Tue, 25 Oct 2022 10:58:45 GMT  
		Size: 12.1 MB (12136537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141757944ae9504f5b61aa918af860a5df9c49dfcd3e949975d3e80c555fc06`  
		Last Modified: Tue, 25 Oct 2022 10:58:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea0737ce5c9e03b6e80032c9c05bd7a219eff0d23b04a24a8909224b5bd8df`  
		Last Modified: Tue, 25 Oct 2022 10:58:44 GMT  
		Size: 10.1 MB (10064496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494aa4be228e2c20493fe96aa07b98f01223e4938daf38d79e837ec9a08e8530`  
		Last Modified: Tue, 25 Oct 2022 10:58:42 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f6eecfc475f33f505f05d2342da90f64c64131baa4a86048364cf842db91be`  
		Last Modified: Tue, 25 Oct 2022 10:58:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e81e9bf50f6ab303f2cfe92325a5efc0596192473f8832ec5948013bb3766e`  
		Last Modified: Tue, 25 Oct 2022 10:58:42 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1b1c2365bca170ea063a295c7fd56e3690fc70bf78cb634f30a7f2647605ac`  
		Last Modified: Tue, 25 Oct 2022 19:04:15 GMT  
		Size: 1.7 MB (1657246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a065f5675eab5e210e1059a4df2ca6c2d74466a522b61709acadb8c8c68eddcd`  
		Last Modified: Tue, 25 Oct 2022 19:04:17 GMT  
		Size: 15.0 MB (15030853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88b79029b6561e9313f818135e19e85f647d0701841e7e968c23cb5ce5574`  
		Last Modified: Tue, 25 Oct 2022 19:04:12 GMT  
		Size: 568.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3c14efbed151ab9bac9b37c47bf5ce8031c8dcb7b94cc71e0372ef951ef641`  
		Last Modified: Tue, 25 Oct 2022 19:04:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a8d7b527fc51cc2dcd769deef73e52e62ee4055c9cf91b69707bcf33e126`  
		Last Modified: Tue, 25 Oct 2022 19:04:41 GMT  
		Size: 158.9 MB (158864134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f28e43e53c5156f6eaf7265a81d8afa1989183aa5f9f0d134e9f7b1e4f8ea8`  
		Last Modified: Tue, 25 Oct 2022 19:04:12 GMT  
		Size: 3.2 KB (3246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4819ab5e17194af70ecb4214e610e4aaf23b2e08880db17308a5cff093d164d7`  
		Last Modified: Tue, 25 Oct 2022 19:04:12 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:62792b121f6d00be76d7d90676be7497ba8139f5767612bdb1fb7964f27a7e68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309864898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d57f79fa7659dd6390ab27bbe60f9ea7c8e0c95d763fcf72ff931592ce2273`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:24:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 16:24:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 16:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 16:24:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 16:24:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 16:35:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 16:35:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 16:35:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 16:35:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 16:35:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 16:35:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 16:35:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 16:35:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 17:57:01 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Oct 2022 17:57:01 GMT
ENV PHP_VERSION=8.1.11
# Wed, 05 Oct 2022 17:57:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 05 Oct 2022 17:57:02 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 05 Oct 2022 17:57:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 17:57:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 18:06:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 18:06:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 18:06:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 18:06:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 18:06:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 18:06:52 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 18:06:52 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 18:06:52 GMT
EXPOSE 80
# Wed, 05 Oct 2022 18:06:52 GMT
CMD ["apache2-foreground"]
# Wed, 19 Oct 2022 20:04:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 19 Oct 2022 20:04:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Oct 2022 20:04:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Oct 2022 20:07:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 20:07:14 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 19 Oct 2022 20:07:14 GMT
VOLUME [/var/www/html]
# Wed, 19 Oct 2022 20:07:14 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 19 Oct 2022 20:07:15 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 19 Oct 2022 20:08:10 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 20:08:11 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 19 Oct 2022 20:08:11 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 19 Oct 2022 20:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Oct 2022 20:08:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584501380c2ed7550f9448cd6cc5bd8e0a21022806a841c4667e39696bdc1db7`  
		Last Modified: Wed, 05 Oct 2022 21:18:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431b428a901f2bd26cfb604a51e4405b669ceaa8c004401df3e3c7562858e06f`  
		Last Modified: Wed, 05 Oct 2022 21:18:47 GMT  
		Size: 69.3 MB (69320187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264cb2924ffd7444e569f4b67ea64dd54d76f83f9fb925c3b993688e01f3f391`  
		Last Modified: Wed, 05 Oct 2022 21:18:31 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51cde6db43d44597c473f0842a8a4e1932f10801a40c6a4b04e8707177f4c21`  
		Last Modified: Wed, 05 Oct 2022 21:19:29 GMT  
		Size: 18.0 MB (17997873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d1748b177ecc1f1cf92ce0253a0211e152e3682c9fcb00413da72bd6e6b91e`  
		Last Modified: Wed, 05 Oct 2022 21:19:25 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0da66653bbd8074d64df2d02b49a07f67be385ee4581054c2a29fcf0a1fb2b`  
		Last Modified: Wed, 05 Oct 2022 21:19:25 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d83160f96766a9215314c13aedb28a7eecbf438a1ee649bee855225e4f0990b`  
		Last Modified: Wed, 05 Oct 2022 21:23:51 GMT  
		Size: 12.1 MB (12135859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e46e4151d72b23da604b9c43bf2ae1f782fb62b33897e788e859f8088bb28a`  
		Last Modified: Wed, 05 Oct 2022 21:23:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d95ddc9aaca354d252d77a59825d74e3e4e45d88f43d5afb800fe622059b17`  
		Last Modified: Wed, 05 Oct 2022 21:23:51 GMT  
		Size: 9.5 MB (9533825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86c75ec00c7d17f108b5ecdcc864ffcce97a177a4012ccc592b79886f838f0`  
		Last Modified: Wed, 05 Oct 2022 21:23:47 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736220764daaeb14a27fb99ba11b3839077d33fd64dea4ee367f274843d3acca`  
		Last Modified: Wed, 05 Oct 2022 21:23:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b4f3e64ccbfc6b92e8a3fe3fc3fea410b8b45400839acb534c83439dcf17b9`  
		Last Modified: Wed, 05 Oct 2022 21:23:47 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13329fc73852717962d56b863405558cb9106d71d327a2dc3ff20de21ea0d73`  
		Last Modified: Wed, 19 Oct 2022 20:17:45 GMT  
		Size: 1.5 MB (1510585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4969ca7f056fbcfbf5a504716f46a7f34dee0a40bdd1b41b8849dbd3c2714`  
		Last Modified: Wed, 19 Oct 2022 20:17:47 GMT  
		Size: 13.9 MB (13911736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e908ba4bd1e2b9fadec38ad3ddaf04acaf8f7ea5fb2a53a06144bb8781cdaf3`  
		Last Modified: Wed, 19 Oct 2022 20:17:41 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ae457eb38859438a3f4a5b4807e2bb5cd2ea8a450276cd20811f3cd90a85ec`  
		Last Modified: Wed, 19 Oct 2022 20:17:41 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8dfd589aea74fd8ab17ddff6a2b57a004be83601578eb1d7aae10a717993a2`  
		Last Modified: Wed, 19 Oct 2022 20:18:13 GMT  
		Size: 158.9 MB (158863408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aee8a560e1d98fd5c355ae0ed627c2d6ac0f92bb8698a0c1847e4d3f98a4d8`  
		Last Modified: Wed, 19 Oct 2022 20:17:41 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b0534f331b32e5447a02555d38220050833f537141a4aafabd438be1ab0de`  
		Last Modified: Wed, 19 Oct 2022 20:17:41 GMT  
		Size: 2.2 KB (2212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:c821761f060e8bfb2f8eac4443534ebb47b7038cfe2f262c531c19d4ac030c67
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335485825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e25878bb4defb23908a7041d4e3a848c3192fe1be640d79c8538fbd6c5be8e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:00:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 16:00:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 16:00:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:00:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 16:00:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 16:03:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 16:03:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 16:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 16:03:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 16:03:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 16:03:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:03:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:03:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 16:52:19 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 25 Oct 2022 17:40:54 GMT
ENV PHP_VERSION=8.1.11
# Tue, 25 Oct 2022 17:40:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Tue, 25 Oct 2022 17:40:54 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Tue, 25 Oct 2022 17:41:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 17:41:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 17:43:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 17:43:55 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Oct 2022 17:43:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 17:43:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 17:43:56 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Oct 2022 17:43:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Oct 2022 17:43:56 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 17:43:56 GMT
EXPOSE 80
# Tue, 25 Oct 2022 17:43:56 GMT
CMD ["apache2-foreground"]
# Wed, 26 Oct 2022 14:10:59 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 26 Oct 2022 14:10:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 26 Oct 2022 14:10:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 26 Oct 2022 14:13:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 14:13:35 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 26 Oct 2022 14:13:35 GMT
VOLUME [/var/www/html]
# Wed, 26 Oct 2022 14:13:36 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 26 Oct 2022 14:13:36 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 26 Oct 2022 14:14:28 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 14:14:32 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 26 Oct 2022 14:14:32 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 26 Oct 2022 14:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 14:14:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0561680dabe2de60226eae9b638b31d60cc7380348ed91f16fb2323135a44ab4`  
		Last Modified: Tue, 25 Oct 2022 19:38:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351526f9a72c42ff7e19d5c66c23824d15a33b23d4f0614a04aaa485df9e2131`  
		Last Modified: Tue, 25 Oct 2022 19:38:52 GMT  
		Size: 86.9 MB (86928284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b21a5da3a7b221650e7528802ac2b8cdb5c28537f5bd131de3a6dc02694405`  
		Last Modified: Tue, 25 Oct 2022 19:38:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87711ceb3120efe71b86a11c3dbb1f0d3747cad16ed2534ba0f86ce8d6e953ed`  
		Last Modified: Tue, 25 Oct 2022 19:39:23 GMT  
		Size: 19.2 MB (19167499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21369f734b3ab2b4443bd50603048938ed939e1a8c8ffc8c66a62d7492c7396a`  
		Last Modified: Tue, 25 Oct 2022 19:39:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a313d43eb653350da1f8410ebdc3e4d093091f93a81b84e071962f34c513b8a`  
		Last Modified: Tue, 25 Oct 2022 19:39:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f332801235e0932424bc415fb57197858f8e3bafa7233760362c386c116b0e`  
		Last Modified: Tue, 25 Oct 2022 19:48:12 GMT  
		Size: 12.1 MB (12137394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a61ab6b7534b46d54ad62dbb3dbe8e9bd0344460d6d87da22539ac62b1c11`  
		Last Modified: Tue, 25 Oct 2022 19:48:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e6e1fc0be0d2184b1a534d2214334160dc7851469c96b8e4dba748760eb083`  
		Last Modified: Tue, 25 Oct 2022 19:48:11 GMT  
		Size: 11.1 MB (11112628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83a07b0452d223b9ab07739500c7ea267a1082b80cc9aa36fc2eed5f1c039ea`  
		Last Modified: Tue, 25 Oct 2022 19:48:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f756c2d272b3a0467af533c1aafc87833b947c74d063a4b1011e780bd410602`  
		Last Modified: Tue, 25 Oct 2022 19:48:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52012e2885d79b8698f7ba2b0f98a5075d14103143ee9d6cb716685d53de451`  
		Last Modified: Tue, 25 Oct 2022 19:48:09 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74f47d18197614cba9c908c925ab5092eac6cdefb49a773a579c97d1ef8838b`  
		Last Modified: Wed, 26 Oct 2022 14:27:03 GMT  
		Size: 1.6 MB (1648458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4326ab5fa2e93d41984f6a41e6bf145e4cf07f7b08e5ad8d57c36e2da5022e39`  
		Last Modified: Wed, 26 Oct 2022 14:27:05 GMT  
		Size: 15.6 MB (15550254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d13321108e10848b855e4b8a9a93faa664a90c96904486ed91296f2499374d7`  
		Last Modified: Wed, 26 Oct 2022 14:27:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b185f909f4b96ba2137bbe9492bbf1c2bfb11964513b0b5635a9451164de9ce`  
		Last Modified: Wed, 26 Oct 2022 14:27:00 GMT  
		Size: 571.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dfb2a18d9a9aa68e2c0a6fcc9422ce12d50160594b6a17a150a7abd57e4f20`  
		Last Modified: Wed, 26 Oct 2022 14:27:17 GMT  
		Size: 158.9 MB (158865198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcea46037f4410b9379c9dcb3644e0d71b61e1c34b2c58a54a5d7046ce8d1576`  
		Last Modified: Wed, 26 Oct 2022 14:27:00 GMT  
		Size: 3.2 KB (3247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbd667bed028e7666ef00b70a8f55a5b4768a0f0e5bbc9d81df606b713d9ec0`  
		Last Modified: Wed, 26 Oct 2022 14:27:00 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; 386

```console
$ docker pull nextcloud@sha256:62bd71727928b50eaaedd2a16243376b1d926777544c588ffcd7be4d0bd9ad93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344396792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a0f5a97f7c37e12a80a319f06dff0dbe12eeda194da7d01e04a842a182f2c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 05:19:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 05:19:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 05:19:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 05:19:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 05:19:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 05:22:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 05:22:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 05:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 05:23:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 05:23:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 05:23:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 05:23:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 05:23:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 05:49:24 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Oct 2022 05:49:25 GMT
ENV PHP_VERSION=8.1.11
# Wed, 05 Oct 2022 05:49:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 05 Oct 2022 05:49:27 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 05 Oct 2022 05:49:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 05:49:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 05:52:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 05:52:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 05:52:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 05:52:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 05:52:28 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 05:52:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 05:52:30 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 05:52:31 GMT
EXPOSE 80
# Wed, 05 Oct 2022 05:52:32 GMT
CMD ["apache2-foreground"]
# Wed, 19 Oct 2022 19:44:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 19 Oct 2022 19:44:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Oct 2022 19:44:07 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Oct 2022 19:46:34 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:46:35 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 19 Oct 2022 19:46:35 GMT
VOLUME [/var/www/html]
# Wed, 19 Oct 2022 19:46:36 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 19 Oct 2022 19:46:37 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 19 Oct 2022 19:47:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:47:31 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 19 Oct 2022 19:47:32 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 19 Oct 2022 19:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Oct 2022 19:47:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66c6251c9ee245e714f25f116d32ddbeb4b14119624dbeb9462681ffafaadfe`  
		Last Modified: Wed, 05 Oct 2022 07:04:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94148bf9d9bd5e209113c7ec9b4369d30278c956972b89fb4f6fa9ef8924889`  
		Last Modified: Wed, 05 Oct 2022 07:04:41 GMT  
		Size: 92.5 MB (92511256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3222d745baded4e26ec0fa2889971c97b348a1eecb9140306933be5617568aec`  
		Last Modified: Wed, 05 Oct 2022 07:04:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0431b31323d54645f97742530be48808cc5be0a70692901af4acf6986b554dc9`  
		Last Modified: Wed, 05 Oct 2022 07:05:17 GMT  
		Size: 19.5 MB (19515791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235771d7a0c60ffdeffd6e631dd7cf9fb25673dd6d988b0fa11ac263c24c9ff`  
		Last Modified: Wed, 05 Oct 2022 07:05:14 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5962388a2f8dc7aa71a9943e42ed08b049ebf8d77b78bbbbf7f73e8527135474`  
		Last Modified: Wed, 05 Oct 2022 07:05:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccdf8b9d166a89da7c562b28e06659a07c602ae14254576e165b14b7429b8ef`  
		Last Modified: Wed, 05 Oct 2022 07:09:02 GMT  
		Size: 11.9 MB (11921906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66309a74175d90c303e91dc0fe2a3d19b4dcf895848d21f46d6dc323b9475a23`  
		Last Modified: Wed, 05 Oct 2022 07:08:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc106d5dc13b6846286487aa8433d81932cb4732be4eb34c8460bbee288a14e`  
		Last Modified: Wed, 05 Oct 2022 07:09:00 GMT  
		Size: 11.3 MB (11265939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e38c4a09f5ed1411d2386785a0d714ba81d935ac3c70e44f5cdef2cd665a60d`  
		Last Modified: Wed, 05 Oct 2022 07:08:58 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215bdb922a76273b1c380a6e83ceba403d6149ed34d59c84aba9886fca3bf0a4`  
		Last Modified: Wed, 05 Oct 2022 07:08:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5f112d8671758b0277e36926f7e4762eff84ee7303a7175ab7e4d7e5d2276`  
		Last Modified: Wed, 05 Oct 2022 07:08:58 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d08224070ba41f36067373d0e0a1889544a3ccbffbde82a3842abd13b7492fa`  
		Last Modified: Wed, 19 Oct 2022 19:54:00 GMT  
		Size: 1.5 MB (1516452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ddee5da3d05b518fa7ce2c516e109626864b3977473a038127bc44ec7777d`  
		Last Modified: Wed, 19 Oct 2022 19:54:02 GMT  
		Size: 16.6 MB (16635781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb659f0b7b386c152e4ee5419f9b1a2a161d5d711f27d62fc180271451f96e8`  
		Last Modified: Wed, 19 Oct 2022 19:53:57 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a48945f4af64586c838cbc288762b3d67345ac505116ebbab078ef84857c74`  
		Last Modified: Wed, 19 Oct 2022 19:53:57 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9487ac815ba06cf5c968cb1cff909a15369cdd5b25d4f34c4f450e039a553df`  
		Last Modified: Wed, 19 Oct 2022 19:54:17 GMT  
		Size: 158.6 MB (158621300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df631b86bef7c7ae8cebac2d5630e2856baa581dfac9078466f116f598f84800`  
		Last Modified: Wed, 19 Oct 2022 19:53:57 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48a0133ef4b235beeb9389e54b61b85997cbde0b52764c74742b3fd56551085`  
		Last Modified: Wed, 19 Oct 2022 19:53:58 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; mips64le

```console
$ docker pull nextcloud@sha256:3d327bfabded94cdbe521dca2aa09f3af0e3621ddbf1c401e426120d0870de04
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317557614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d0fa6fa580ef7e5db03b8c5cb36f3701bb801df04c96fa75060ea596d2d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:07:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 04:07:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 04:09:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:09:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 04:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 04:24:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 04:24:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 04:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 04:25:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 04:25:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 04:25:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 04:25:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 04:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 05:23:16 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Oct 2022 05:23:19 GMT
ENV PHP_VERSION=8.1.11
# Wed, 05 Oct 2022 05:23:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 05 Oct 2022 05:23:25 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 05 Oct 2022 05:24:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 05:24:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 05:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 05:37:58 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 05:38:04 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 05:38:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 05:38:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 05:38:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 05:38:17 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 05:38:21 GMT
EXPOSE 80
# Wed, 05 Oct 2022 05:38:24 GMT
CMD ["apache2-foreground"]
# Wed, 19 Oct 2022 21:16:13 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 19 Oct 2022 21:16:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Oct 2022 21:16:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Oct 2022 21:28:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 21:28:20 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 19 Oct 2022 21:28:24 GMT
VOLUME [/var/www/html]
# Wed, 19 Oct 2022 21:28:30 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 19 Oct 2022 21:28:34 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 19 Oct 2022 21:43:44 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 21:43:55 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 19 Oct 2022 21:44:04 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 19 Oct 2022 21:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Oct 2022 21:44:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0896fc6eba5b51312bacc6927ac2b365968d6597f00a844bc10807f0c940864f`  
		Last Modified: Wed, 05 Oct 2022 07:44:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71bf7eae2ef4d6ce85ffb69b9a1a5b6fa110c3d599325f657f8700273b09560`  
		Last Modified: Wed, 05 Oct 2022 07:45:15 GMT  
		Size: 71.8 MB (71813495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edadfadfe89d6ab5ad954413fab6b50e3cfb0c39507844b0f850ed0e6463a53`  
		Last Modified: Wed, 05 Oct 2022 07:44:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df1dffdbc96ddfa88f3806a02f5577b9e342e75f524d5b1ea875d297b28f8c4`  
		Last Modified: Wed, 05 Oct 2022 07:45:57 GMT  
		Size: 18.9 MB (18940120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58fa2fd1d28449679abbde219f898b7c3fe6faf3a7aac6e6a2b7b241a0c2985`  
		Last Modified: Wed, 05 Oct 2022 07:45:45 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6181a7bc51a82964ccda6c3b96ac7741d20f3098c7e971681ee5759823207fc`  
		Last Modified: Wed, 05 Oct 2022 07:45:45 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd6920ec748f95e9c5bdaab4e6c1f85a8f69660fbe1fbd9c5a0ecac8e3c1e75`  
		Last Modified: Wed, 05 Oct 2022 07:48:33 GMT  
		Size: 11.9 MB (11920707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25c731232282b0d23ad02d47b0498c91dcd4261ff587ef2d35fc032fb415a28`  
		Last Modified: Wed, 05 Oct 2022 07:48:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25210c390c2fff1431f79a790e2e4965b12e4bfe3f50cedc2e2d51a8f9d665f4`  
		Last Modified: Wed, 05 Oct 2022 07:48:35 GMT  
		Size: 10.2 MB (10192057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f5543c157444b1cdc14f29a6d475205d54fd326a4f46d455c95010aac57c6e`  
		Last Modified: Wed, 05 Oct 2022 07:48:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d658d9c9db0d8c007c2f3cbc251ad4c43fc4abaee238a1c1d4d05d08db1962`  
		Last Modified: Wed, 05 Oct 2022 07:48:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a199ed40205a49fb41b240b44c0815440188079d4f3f68d2722293cd9586a08`  
		Last Modified: Wed, 05 Oct 2022 07:48:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98772f5aff11a0a08dc193363e9f843ed37f2dc01629d918c80bec3131c3ed3b`  
		Last Modified: Wed, 19 Oct 2022 22:10:10 GMT  
		Size: 1.6 MB (1568676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1b00be1addd7e91851450bb200dfabf581b9cd8f714a5dd6380e266c6a6c32`  
		Last Modified: Wed, 19 Oct 2022 22:10:17 GMT  
		Size: 14.8 MB (14847244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc300c9a2549b70f1bea7e8957ef5514d9bc0a04437735f9694248c18c866d32`  
		Last Modified: Wed, 19 Oct 2022 22:10:04 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2e87dd13c0310f4df4cf0fb6728656d5ebd47e1313957436dfe97fba652bac`  
		Last Modified: Wed, 19 Oct 2022 22:10:04 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a39ee4a6a1d5cf6a9ce8a6ea440ac33812161aa87a56b5ba5493bea921bde37`  
		Last Modified: Wed, 19 Oct 2022 22:11:44 GMT  
		Size: 158.6 MB (158622365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6314da5dcb597a30abed6792179d959247b31ed5d1bb56182603b2275f0835cc`  
		Last Modified: Wed, 19 Oct 2022 22:10:04 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b0e5af473328b97c38a8675c3ab1192d2c78dec21069287d0fe7cf5d5671ac`  
		Last Modified: Wed, 19 Oct 2022 22:10:04 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:5e2dd44de03231558a2e365a85a8f7005d8b49c756c3060609c38f7db4e6f1b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343521670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0d4753c0cb1d5be6bd44e17213a4b0aeb5c053fe680b1c2b6de7d1289dcd0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:18:04 GMT
ADD file:66a0f55a4b4dfbb5d64082ffdb24751f20c5773039277ba278fdb4ce4a538c33 in / 
# Tue, 04 Oct 2022 23:18:06 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:46:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 01:46:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:47:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 01:47:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 01:51:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 01:51:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 01:52:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 01:52:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 01:52:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 01:52:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 01:52:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 01:52:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 02:09:59 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Oct 2022 02:09:59 GMT
ENV PHP_VERSION=8.1.11
# Wed, 05 Oct 2022 02:09:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 05 Oct 2022 02:10:00 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 05 Oct 2022 02:10:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 02:10:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 02:14:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 02:14:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 02:14:19 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 02:14:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 02:14:19 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 02:14:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 02:14:20 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 02:14:21 GMT
EXPOSE 80
# Wed, 05 Oct 2022 02:14:21 GMT
CMD ["apache2-foreground"]
# Wed, 19 Oct 2022 19:17:26 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 19 Oct 2022 19:17:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Oct 2022 19:17:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Oct 2022 19:22:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:22:11 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 19 Oct 2022 19:22:11 GMT
VOLUME [/var/www/html]
# Wed, 19 Oct 2022 19:22:12 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 19 Oct 2022 19:22:12 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 19 Oct 2022 19:23:24 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:23:33 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 19 Oct 2022 19:23:34 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 19 Oct 2022 19:23:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Oct 2022 19:23:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4e001127162dd884a6f7bd2e6f74215816d325bebb3a374ae9fcee9f038f99b8`  
		Last Modified: Tue, 04 Oct 2022 23:24:13 GMT  
		Size: 35.3 MB (35290584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6992272455a02d94d5481e1a8b2d4af5e8901d37c339bb9dea375996cd83427`  
		Last Modified: Wed, 05 Oct 2022 03:02:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d634c67a43d21c87f45de27d3ce054bbb1ad89e13fb716769ff598c26f98b062`  
		Last Modified: Wed, 05 Oct 2022 03:02:32 GMT  
		Size: 86.6 MB (86631070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b21a26cbdef3718a5f2e1f2c8a1efe6ae69589af499ed4dac5b9770103389e`  
		Last Modified: Wed, 05 Oct 2022 03:02:08 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b246516d713eb6ed73ec7951494aac991793d401e360acc2628aeb5fc240f6`  
		Last Modified: Wed, 05 Oct 2022 03:03:14 GMT  
		Size: 20.5 MB (20464650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46737e14eecdf1879b293f34c5c1132e6ae97c22c89019a4b0d0aa0293f85d`  
		Last Modified: Wed, 05 Oct 2022 03:03:09 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09132e2f7431e2b522caf38be3e7e0f7368fb0f933a75e2845e1b187f62796b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:08 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacf941bd326460e74c4ed1865f4f85afff310503c6563b7636410aa717b2a1e`  
		Last Modified: Wed, 05 Oct 2022 03:06:06 GMT  
		Size: 12.1 MB (12137251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aecd37e5d8e8f204479c0d721bee626e2f40d13772ad072e637ef82a1091b8`  
		Last Modified: Wed, 05 Oct 2022 03:06:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa377aaaeb1f3424bbebc2725fedf604edd028203f9dca2aa64d9934fb6666`  
		Last Modified: Wed, 05 Oct 2022 03:06:06 GMT  
		Size: 11.4 MB (11433890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58702a0f24718606a8c16774fbed4ec1c90674f4e791e4dd98fcd7abb291425b`  
		Last Modified: Wed, 05 Oct 2022 03:06:03 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1b31f0ec0ad3db3227590b9d313f5424de912f788ba42c8c8189cb3b27dfe3`  
		Last Modified: Wed, 05 Oct 2022 03:06:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8fcfde34144cc49503c4b3c7e54ea4ef953c8ccd501e4edae4dfcfccc46448`  
		Last Modified: Wed, 05 Oct 2022 03:06:03 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc0b82068c46dba54c6b24e4b58e56d993811ee4898a6203a0a70526c74527b`  
		Last Modified: Wed, 19 Oct 2022 19:32:53 GMT  
		Size: 1.9 MB (1870544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739090181c8ab7e087e47b63d8063304d021d1db6b25843f33070bb5a7ae1fba`  
		Last Modified: Wed, 19 Oct 2022 19:32:57 GMT  
		Size: 16.8 MB (16815878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb3ca503c20f11461ffee7066a7b2e4f662404632597fc3487ddcd100e372f7`  
		Last Modified: Wed, 19 Oct 2022 19:32:50 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bed00c6ac1a40a226568f1f7f36c272b1cd0044f98552285a7fb78feeac07d`  
		Last Modified: Wed, 19 Oct 2022 19:32:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a1f5c61829e88bddb4debdc1afb0a1031752b596c98b111885995099a398fc`  
		Last Modified: Wed, 19 Oct 2022 19:33:26 GMT  
		Size: 158.9 MB (158865572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bc492b96b187d74635fce5910f7a7979a14ff375c0dff63c765a47848b3071`  
		Last Modified: Wed, 19 Oct 2022 19:32:50 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e202550fc21c2415f5dbe31684dfdb996e02d31b5ed76909d4d9ece7aa7e611`  
		Last Modified: Wed, 19 Oct 2022 19:32:50 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:4b8ffbbdb4ca55a40e384b4109a60fcf118dafddc65f90d5d414c15b052b828d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318081259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfd2a25ccbd68a1a6aad0624d1abe93fab251e8107d79f6af6643a88b94fdfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:49:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Oct 2022 03:49:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Oct 2022 03:49:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:49:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Oct 2022 03:49:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 05 Oct 2022 03:52:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Oct 2022 03:52:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Oct 2022 03:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Oct 2022 03:52:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Oct 2022 03:52:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Oct 2022 03:52:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 03:52:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Oct 2022 03:52:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Oct 2022 04:06:17 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Oct 2022 04:06:17 GMT
ENV PHP_VERSION=8.1.11
# Wed, 05 Oct 2022 04:06:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 05 Oct 2022 04:06:18 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 05 Oct 2022 04:06:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Oct 2022 04:06:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:08:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Oct 2022 04:08:41 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:08:41 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Oct 2022 04:08:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Oct 2022 04:08:41 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Oct 2022 04:08:41 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:08:42 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 04:08:42 GMT
EXPOSE 80
# Wed, 05 Oct 2022 04:08:42 GMT
CMD ["apache2-foreground"]
# Wed, 19 Oct 2022 19:54:14 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static         libldap-common     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 19 Oct 2022 19:54:14 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Oct 2022 19:54:14 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Oct 2022 19:56:54 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:56:56 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 19 Oct 2022 19:56:56 GMT
VOLUME [/var/www/html]
# Wed, 19 Oct 2022 19:56:57 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 19 Oct 2022 19:56:57 GMT
ENV NEXTCLOUD_VERSION=25.0.0
# Wed, 19 Oct 2022 20:01:25 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 20:01:35 GMT
COPY multi:812ebb13115fbd5eaadc9d9df89b2bcb886e2ec0d6a45d21b802bc1c2c1d6cb1 in / 
# Wed, 19 Oct 2022 20:01:35 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Wed, 19 Oct 2022 20:01:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Oct 2022 20:01:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6100c5da5e147c51c1423d657e79d2dff4dd181c31f934a41ae83c6d39262`  
		Last Modified: Wed, 05 Oct 2022 04:47:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70604a80be4877e1eadd22a96fd3e1d5051435d36194e48876fd138f8773f3f5`  
		Last Modified: Wed, 05 Oct 2022 04:47:58 GMT  
		Size: 71.6 MB (71625657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0fbe4d7818a668f0b61bb2678d6b5a4eba5f84513ae0e51426d69595cb60c`  
		Last Modified: Wed, 05 Oct 2022 04:47:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e41923ed7e48184c82ce912a22590f942a4fc9c68544a5b4ac844e6d9f44ae`  
		Last Modified: Wed, 05 Oct 2022 04:48:23 GMT  
		Size: 19.1 MB (19071175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bf231e21db301dfe535163bb7e7e9f58cb82b58c7a23b90accde229c9d0507`  
		Last Modified: Wed, 05 Oct 2022 04:48:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547889acb757e28fc80e27d9c7cc906e3c367b266b7d03cdbd80d46a306ae75c`  
		Last Modified: Wed, 05 Oct 2022 04:48:21 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710b05dfff28f6b46a5142fbea4fed439306ecfcf14d66db63ff1ba44c8eb059`  
		Last Modified: Wed, 05 Oct 2022 04:50:14 GMT  
		Size: 12.1 MB (12136320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ac356bab7d0554d2ab3589622a3f7d89ec3c7bc2643fbe59232155ac5e2d7f`  
		Last Modified: Wed, 05 Oct 2022 04:50:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36f91d49d3995009e66b1258b8f00bbc11921c4c784a732d9628da7a2084b74`  
		Last Modified: Wed, 05 Oct 2022 04:50:14 GMT  
		Size: 10.2 MB (10175440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2971bdfa84f0576bb2dffcf843ea16b4ab41165ac6893b2ca0b30fc8ac99e11e`  
		Last Modified: Wed, 05 Oct 2022 04:50:12 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d316b2fdec7e97d0159e29c9158ad86de599a214be7d8343d80176c9c6d9518`  
		Last Modified: Wed, 05 Oct 2022 04:50:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a90ae5e000aa178abc1624d83507311bfa1e38f0744e8369ea25ca5c9ebfe`  
		Last Modified: Wed, 05 Oct 2022 04:50:13 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e234706baba27cb964303182ad76cab6ad5aa6fbeee3fac40d056338352c296`  
		Last Modified: Wed, 19 Oct 2022 20:13:42 GMT  
		Size: 1.7 MB (1659466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9203ac8142dc429cb780456b97376bb826b9f43ee19761d1dcb7f8e3bb9f8`  
		Last Modified: Wed, 19 Oct 2022 20:13:44 GMT  
		Size: 14.9 MB (14886453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496347c3c25f75fb386b421804bba06c3269b8ae3228b682b520536e08d9b0c2`  
		Last Modified: Wed, 19 Oct 2022 20:13:41 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22bb5fad903c7570626bc18906e97c26be41490ae0a7d7bc8ee5da24d21b74`  
		Last Modified: Wed, 19 Oct 2022 20:13:41 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5399883c781fb5e0a0327d324396283c35a639df4fba10a60374d0a1a9f314`  
		Last Modified: Wed, 19 Oct 2022 20:13:59 GMT  
		Size: 158.9 MB (158863812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef64831fc8682ee7f93a324340ded2bed4e86462f9a202db771ed85f2fe1d36`  
		Last Modified: Wed, 19 Oct 2022 20:13:41 GMT  
		Size: 3.2 KB (3246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d7312f070742fb1d8957a37ffdfe3129915cd0fe1fc5ea5b0c5f16e357109`  
		Last Modified: Wed, 19 Oct 2022 20:13:41 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
