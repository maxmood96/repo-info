## `monica:latest`

```console
$ docker pull monica@sha256:3ddfc1bae5c71641d99bf84287407b873df35498aed39367145aba96e99e4b62
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

### `monica:latest` - linux; amd64

```console
$ docker pull monica@sha256:a46569ecb98b61522397f75161c84dbddbeca8287198167862dda763ddcfe0ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6773910573eb7b2ed198a1662626d8120837139609fc4414c2df07d162a43d5`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:17:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:17:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:17:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:17:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:21:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:21:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:21:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:22:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:52:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:17:08 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:17:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:17:08 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:17:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:17:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:20:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:20:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:20:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:20:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:20:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:20:54 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:20:54 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:20:54 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 03:53:22 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 03:53:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:55:11 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:55:11 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 03:55:11 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 03:55:11 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 03:55:12 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 03:55:13 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 03:55:13 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 03:55:13 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 03:55:14 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 03:55:14 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 03:55:14 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 03:55:14 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 03:55:30 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:55:31 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 03:55:31 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 03:55:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ab1cc5ca33d8382a34578c5ac4fec4d1f4a381d747e3c9d2e8fd8bdc20b621`  
		Last Modified: Thu, 17 Oct 2024 04:18:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee5e1490ca9e76fb6078eb2581366decdceea48fa3e65583e2c80e10522849`  
		Last Modified: Thu, 17 Oct 2024 04:19:14 GMT  
		Size: 104.3 MB (104346971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e807ae4973d0b87fd52b4704132912240c54d7c5110dabfbd3e5032ca5249eec`  
		Last Modified: Thu, 17 Oct 2024 04:18:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1846dfbe9adb998f8c506143dfcf02b7dee1b6b39ba6746202c87e2f3e41ff`  
		Last Modified: Thu, 17 Oct 2024 04:19:36 GMT  
		Size: 20.3 MB (20327779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1d0bbde8147dd947d4227d005cf449ab44cfefebf706b899000054185f9d7`  
		Last Modified: Thu, 17 Oct 2024 04:19:33 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac5e585cd612eddd957e7c3edb4712bfabc4f504eb4a72e6dc5088776b51b0`  
		Last Modified: Thu, 17 Oct 2024 04:19:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c65c4fca52e66ad639ef8f1b89254b614c937ca676ee12c88c10ef03163b32f`  
		Last Modified: Fri, 25 Oct 2024 02:19:22 GMT  
		Size: 12.5 MB (12459142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2e2799aa38d234b5907b767a6da9cab47e91e6d50b721e6d0156d451fbad8e`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54527c6f928b18fe9aef233c061c29d980603a47607954003ab00bc703bdcce`  
		Last Modified: Fri, 25 Oct 2024 02:19:21 GMT  
		Size: 11.4 MB (11411365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d76291219c34281af41ae9436d8f53096e1059fa1ac9ed2bdebdd77d190ff12`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e14935230bbc66875d6e9b6b234732cb402089ab8e04e6704f5830ec8e9be2`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cbeb13063d7e707ba17678d2ee4cf2ff4fa5608fdc3bc1111435561ff46b09`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5a3b1d0f9b776bec35f475b6ba3e05efe32bfd99bb3e18fa0ef6b6699e8bdb`  
		Last Modified: Fri, 25 Oct 2024 04:07:43 GMT  
		Size: 1.4 MB (1398729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6413fc59a4e747b800046d4fffbdf74eb4fa416551d8b625d3cfc12082ce15`  
		Last Modified: Fri, 25 Oct 2024 04:07:44 GMT  
		Size: 4.7 MB (4701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317d971d1d120032b727c02ebc32090f5265edaf5c5f1b3f18191ce9c255cc03`  
		Last Modified: Fri, 25 Oct 2024 04:07:43 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0d3e80b4f4ca56058730e1c62008709a57515fc9679fdd59fa04a7a0c746a`  
		Last Modified: Fri, 25 Oct 2024 04:07:43 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabde8ce664f8e7754423dda00810f756a824e9ad151acb7c5dfff91741af216`  
		Last Modified: Fri, 25 Oct 2024 04:07:41 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742f64c0c1148aace5d5f111c6b425d5eb9b4b89859d176465889bb7aa52e4ce`  
		Last Modified: Fri, 25 Oct 2024 04:07:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976e081a83c6378cddf2e173a53e6edb664d746d329b4bfbe4529c2c470c068d`  
		Last Modified: Fri, 25 Oct 2024 04:07:41 GMT  
		Size: 8.2 KB (8203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392d7e51cb3ee2a1a65b6bb4fcba51fce867e701d22abfbab9faac58005c13e6`  
		Last Modified: Fri, 25 Oct 2024 04:07:47 GMT  
		Size: 28.7 MB (28696050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92baefe7d4871b74fe120fc38d71c7d261183b9daa3da2f27841647afc6a0b03`  
		Last Modified: Fri, 25 Oct 2024 04:07:41 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; arm variant v5

```console
$ docker pull monica@sha256:f5e3814b80be8919f580d485032a6481fbe170b3384c98a901e02ea76540e87b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185863812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d63c2bc204c7ec22cf4ac9597ededca4ae639dc85ae01454c08f9cfb6de69`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:28 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 17 Oct 2024 00:54:29 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:39:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:39:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:40:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:40:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:48:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:48:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:48:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:48:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:48:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:09:07 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 00:35:17 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 00:35:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 00:35:18 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 00:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 00:35:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:40:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:40:30 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:40:31 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:40:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:40:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 00:40:32 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:40:32 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:40:32 GMT
EXPOSE 80
# Fri, 25 Oct 2024 00:40:32 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 01:36:24 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 01:36:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 01:38:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 01:38:24 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 01:38:24 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 01:38:24 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 01:38:25 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 01:38:27 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 01:38:27 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 01:38:28 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 01:38:28 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 01:38:29 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:38:29 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 01:38:29 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 01:38:56 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 01:38:58 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:38:59 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 01:38:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5235299add7bb4a13b494a07f66eb5939b6cb20e1cc0d0f75550967a7376c`  
		Last Modified: Thu, 17 Oct 2024 03:45:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8907632e889fbd259ac6ebe1d70401840bf18fb005d7c35952efd42916d520`  
		Last Modified: Thu, 17 Oct 2024 03:45:21 GMT  
		Size: 82.0 MB (81995968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6a7f456b58f9278213fe4b51fb3844191e9e472c54adce160d2e3ebea1c81e`  
		Last Modified: Thu, 17 Oct 2024 03:45:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19743805d7cb37913f1b3f1b2cf18aa012ad377a421c22b0a52997bbc49d64e5`  
		Last Modified: Thu, 17 Oct 2024 03:45:46 GMT  
		Size: 19.6 MB (19624385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056f964ef6cf0cfd02b1e7ab1e9df4a4500d9af80762867bf9f4da4ee999f9e`  
		Last Modified: Thu, 17 Oct 2024 03:45:42 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567fd2c394a19ce53e7a88c0cef2c03c411330889c3b51677db7bd9d1fa408`  
		Last Modified: Thu, 17 Oct 2024 03:45:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19051b235de6dfbfb33dbb4563b65db22d8cc50e32ee918ff27a1005c9e15238`  
		Last Modified: Fri, 25 Oct 2024 00:55:24 GMT  
		Size: 12.5 MB (12457446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3372071af8134f9af497a3fecbc2f41b997a999e496991e046834bfc1fe4cd6c`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea77592d248ec01d8ba9ee5913e4788f1588b00a99cffa7106cb28251564ab63`  
		Last Modified: Fri, 25 Oct 2024 00:55:24 GMT  
		Size: 10.4 MB (10395166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eae1544b7f8f18792fda85e7fa6d60683402b2e54735b0854195e8da97c5bb1`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800893d28af528dd5f0dd74fb563e8cc644678420648b2ee9a24e5df6e74617e`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cecafa4446a8d5fe60aba51d2d57b102ef7c73ebfa77efb9f7fd85559a74db`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cd17f15b72e8f73898c7b1f2a1f5fa508c7d2a160e60f9ddaa250c5d1cde6f`  
		Last Modified: Fri, 25 Oct 2024 01:47:57 GMT  
		Size: 1.4 MB (1374244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19aea4957be97f97fa1d15d5c4656e02a6bcc7286bc01de96fbe5adb753ee2b`  
		Last Modified: Fri, 25 Oct 2024 01:47:57 GMT  
		Size: 4.4 MB (4420722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b84902c412ca5934e38b858539f6ce596667e26f84705ca92573ac3654797f`  
		Last Modified: Fri, 25 Oct 2024 01:47:56 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba4adb4aadfc6cc627bff8814cafc6d77ef06bc7ae0ea83415f5abc300677f8`  
		Last Modified: Fri, 25 Oct 2024 01:47:56 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc25bf23895563341575a0d20ec5903b63a40b4ccc8f32accbf08ece9b1b8eba`  
		Last Modified: Fri, 25 Oct 2024 01:47:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2838b59646046cda5a536c95ad8d5e54a3cd84b85da1c6baf677a8e1d1507416`  
		Last Modified: Fri, 25 Oct 2024 01:47:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491a76e782d18c99a9997d8740fd2ace58298ba0a8f1c5550a06609602244a5a`  
		Last Modified: Fri, 25 Oct 2024 01:47:54 GMT  
		Size: 8.2 KB (8197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d179741796e0975737e40740d3b56a89ea293b9ccfa1d993fc95609c2d8955bc`  
		Last Modified: Fri, 25 Oct 2024 01:48:05 GMT  
		Size: 28.7 MB (28690990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9372414e13ba0e16572b43ef7e1b8ea18dd4be6256a53e05dc88d28f315cd763`  
		Last Modified: Fri, 25 Oct 2024 01:47:54 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; arm variant v7

```console
$ docker pull monica@sha256:25ae985d846d2e2a92d390a5dab08db9a42b0d5fd7ab1cea78999525b3a8d57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176445939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9408e4e53e5fad1fc21eb9400a0cfa453cc0711d1f250ff4f6a6f16a4660c`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 03:43:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 03:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:44:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 03:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 03:47:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 03:47:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 03:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 03:47:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 03:47:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 04:55:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:49:31 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:49:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:49:31 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:49:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:49:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:52:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:52:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:52:45 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:52:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:52:45 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:52:45 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:52:45 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:52:45 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:52:45 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 03:35:19 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 03:35:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:37:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:37:08 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 03:37:08 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 03:37:09 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 03:37:09 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 03:37:10 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 03:37:10 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 03:37:10 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 03:37:11 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 03:37:11 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 03:37:11 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 03:37:11 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 03:37:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:37:30 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 03:37:30 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 03:37:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57816ea258091707b20fd42869f1859c1543e794b483b8003de268daf39132a0`  
		Last Modified: Thu, 17 Oct 2024 06:00:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f29e3f6b59ec149599415083926b75214bfab19a179c7ef4d7535bbee364a84`  
		Last Modified: Thu, 17 Oct 2024 06:00:36 GMT  
		Size: 76.2 MB (76163462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace57af7e6d627dfdf6574de994827570ba429858c8118ccf5028e7c121e0e9b`  
		Last Modified: Thu, 17 Oct 2024 06:00:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863416241c1e20444861f13ebb223232950439972781be1e45b6704fee41682`  
		Last Modified: Thu, 17 Oct 2024 06:00:59 GMT  
		Size: 19.1 MB (19062321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300e0800b02d2903ba85150c9b5f31cab1e364d99e199b1614838bb031e1116c`  
		Last Modified: Thu, 17 Oct 2024 06:00:56 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11748bf3dd7f577b46d343e58bff8badc4bb124233ef94312a971750f9db7079`  
		Last Modified: Thu, 17 Oct 2024 06:00:56 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333fe2ac6423f3cb82ef6b6e757d13ad4a5400b56bdd9a4e0d3a25fd4fd83234`  
		Last Modified: Fri, 25 Oct 2024 02:40:12 GMT  
		Size: 12.5 MB (12457386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22740d32b386066e1690c2b730acfb1e18f77b45480e9a453a76f01bb86c9a98`  
		Last Modified: Fri, 25 Oct 2024 02:40:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef620ba8968e386e5e8ec89b292e7d2779df2c2dbcf358c4e5d3cd623052861`  
		Last Modified: Fri, 25 Oct 2024 02:40:12 GMT  
		Size: 9.8 MB (9826203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ac45144f0f21ba1f72d5aaa145d0597adc0917b6eb55821509d3ecb22c8106`  
		Last Modified: Fri, 25 Oct 2024 02:40:10 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce85ad194d099e4d39f5c7f4126abc80485a98b234a421fd0c6de1cd3dd829d1`  
		Last Modified: Fri, 25 Oct 2024 02:40:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8687b3a9cb4557f6e5fa3fe2eecbf7c9e6d892f0ab0efc59476dcd3aabac916c`  
		Last Modified: Fri, 25 Oct 2024 02:40:10 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5f6641fbcf8196bf77294c4a3d1f7ee4c3f764a1d1eb64e49c94b77801e859`  
		Last Modified: Fri, 25 Oct 2024 03:49:36 GMT  
		Size: 1.2 MB (1245897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baded6808a98b844103482681dbbd4e21506c5d3f60c0ddf1eb070e09a5625d3`  
		Last Modified: Fri, 25 Oct 2024 03:49:36 GMT  
		Size: 4.3 MB (4264159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098d0bef97042b8555b0c345b84dfec19cb38fe67b961fb59b5cd2b7a31f07d2`  
		Last Modified: Fri, 25 Oct 2024 03:49:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e7c108b50c63d018ffcd3d23912b24351acb865bac167beb2540188fa0cc8`  
		Last Modified: Fri, 25 Oct 2024 03:49:35 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80592d738638e2bcfc087c81c43d02974afdb0b459ef4ee199ce76591076661a`  
		Last Modified: Fri, 25 Oct 2024 03:49:34 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6ff48064a1d685f1476c6d4b9ee2e591e98e29ffbe2c259a0b14723f790d56`  
		Last Modified: Fri, 25 Oct 2024 03:49:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47fe3f66b6d06fbde55797b606c466994f2160e29a08c5190114cca5ffddcd4`  
		Last Modified: Fri, 25 Oct 2024 03:49:34 GMT  
		Size: 8.2 KB (8198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682c65bfcd1de47ef861fe9208bb4c0e2fe622144471f1959b93358ac799e2c`  
		Last Modified: Fri, 25 Oct 2024 03:49:42 GMT  
		Size: 28.7 MB (28690748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd16737a4822c1a81a522f956cef716a15f850d7631ecec15cc9efff9c29174b`  
		Last Modified: Fri, 25 Oct 2024 03:49:34 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; arm64 variant v8

```console
$ docker pull monica@sha256:580a1a08d1f76a0b308185cd3fcb29939ce52c8f2f7b7d7946bf2ff0bef163b4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.2 MB (206203209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cad7ce0106c42924c5c6e1fed67ad0ac9fb71421b2698d738dcc3f9489e641e`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:35:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:35:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:35:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:35:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:35:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:38:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:38:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:38:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:38:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:38:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:59:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:23:47 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:23:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:23:47 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:23:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:23:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:27:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:27:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:27:12 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:27:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:27:12 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:27:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:27:12 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:27:12 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:27:12 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 04:07:20 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 04:07:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:08:53 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:08:53 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 04:08:53 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 04:08:53 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 04:08:54 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 04:08:54 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 04:08:54 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 04:08:55 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 04:08:55 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 04:08:55 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 04:08:56 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 04:08:56 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 04:09:09 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:09:11 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 04:09:11 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 04:09:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6530e6e936cdf7969275d55704b89e0466613540a41ab09fa6edc24a35d57e8`  
		Last Modified: Thu, 17 Oct 2024 04:17:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ffd48d74a0a5446013c25727b2812f6f385b0ffe0ff99f0439d18dad5e5e8c`  
		Last Modified: Thu, 17 Oct 2024 04:17:25 GMT  
		Size: 98.1 MB (98131870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046151abb10af1a2158520721c2b5006584c918b2f36fdb943a5dc36edebe22`  
		Last Modified: Thu, 17 Oct 2024 04:17:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cbece021606df0e0fd4b7b7123856cec73a741c16c93632a0050521f432385`  
		Last Modified: Thu, 17 Oct 2024 04:17:48 GMT  
		Size: 20.3 MB (20325322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce14de3b55afb7a464228d842abfe056cbe1fc2d0809fc69a0206aa13dbdc345`  
		Last Modified: Thu, 17 Oct 2024 04:17:45 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f9962d8983968c3cbbc14b531cea8c72c6c3e0f3e8f36dd3838319b579fc16`  
		Last Modified: Thu, 17 Oct 2024 04:17:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5125b3b76c5ba0e6724648c8f4798af50b98e90bd375ae1811f1deeab36faa5`  
		Last Modified: Fri, 25 Oct 2024 02:22:12 GMT  
		Size: 12.5 MB (12458887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ee3ecc14b867ddd8874bfd50ef49db513b3e610e4c5c276ff39039415772c`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848c5be4a9e5a145c773bde98431924758e9e0a39522b86a065c1546ec5e46da`  
		Last Modified: Fri, 25 Oct 2024 02:22:11 GMT  
		Size: 11.4 MB (11419330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e059d1686fe3ea39a3679a73b0a8edee2c9fecb353c15f38fc9047bfec9a9b04`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa7e7c0785a7bc161d801044e1a2f01dd87249769446664e7f4adad10597eaf`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d420417b0cb4572f3beba13f282a9d028174c4dfc97e2394f6b618fec3703f8a`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650a4dffdeba701a7f7b9f5edd4c21bb752c556c1aeb5c9d1812067c647a8009`  
		Last Modified: Fri, 25 Oct 2024 04:19:53 GMT  
		Size: 1.4 MB (1353202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72d643f418da2f78017f74b84b0107a7509b5788332ddbbab7c1e2bca051800`  
		Last Modified: Fri, 25 Oct 2024 04:19:53 GMT  
		Size: 4.6 MB (4645475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a4ced39592f851248822ea43f6cbed99c8e6cf707dd311d66365cb3bcecb14`  
		Last Modified: Fri, 25 Oct 2024 04:19:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22c70cb2e29a206bb9cba696edec3cd941268d340d2557f682a1564f7846e42`  
		Last Modified: Fri, 25 Oct 2024 04:19:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4267476e90a9b9c5d9065316d0db195a4995eb5a73d3958cb01abcebfffd87`  
		Last Modified: Fri, 25 Oct 2024 04:19:51 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dd6418a9a383de681377887157b1b2ea60769c0726b37db847c78504cc1b67`  
		Last Modified: Fri, 25 Oct 2024 04:19:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c98f4e8c16d025a4514367b590ea3eed3dd7ca647167e8602ce73d8c6131e6`  
		Last Modified: Fri, 25 Oct 2024 04:19:51 GMT  
		Size: 8.2 KB (8197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51dbcafc0d8e70a21a8f3d53fbd015af75845799a35e37e9925d3ee8cb006e1`  
		Last Modified: Fri, 25 Oct 2024 04:19:56 GMT  
		Size: 28.7 MB (28695215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a30a14ce350e2611e150c2a8fc546606aa734c1595809af5eb81ea95f55e27f`  
		Last Modified: Fri, 25 Oct 2024 04:19:51 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; 386

```console
$ docker pull monica@sha256:9668a8798f759555ec14f6067861d7a887ad9346f6ce34085f9fdee1275a0d10
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211463237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78604a8754a85af1c5cf14f488f28d776303a837b3f766785a77485daa208285`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:15:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:15:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:15:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:15:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:15:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:22:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:22:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:22:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:22:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:51:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 02:50:54 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 02:50:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 02:50:54 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 02:51:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 02:51:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:57:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 02:57:08 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:57:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 02:57:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 02:57:09 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 02:57:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:57:09 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 02:57:09 GMT
EXPOSE 80
# Fri, 25 Oct 2024 02:57:09 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 06:23:27 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 06:23:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 06:25:38 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 06:25:38 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 06:25:38 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 06:25:39 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 06:25:39 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 06:25:40 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 06:25:40 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 06:25:41 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 06:25:41 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 06:25:41 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 06:25:41 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 06:25:42 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 06:26:02 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 06:26:03 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 06:26:04 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 06:26:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ade5403812963eef73a48c4f07cea521affbaab25dbb28bfe5359cbc22bac9`  
		Last Modified: Thu, 17 Oct 2024 06:07:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e936af8dfe7f46433beca18a2d23ce12cc58b84c97bd759cde69ae04ffd1ef8f`  
		Last Modified: Thu, 17 Oct 2024 06:07:43 GMT  
		Size: 101.5 MB (101513470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6390a21b9a7d3612aec1c9c3ddfe5307169cf7c8fe4dd367e3bd5be8f7f53934`  
		Last Modified: Thu, 17 Oct 2024 06:07:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df26b407a97966ce11f72a59d30a9c0c723177d7b69a0565ecb1fcb3f09c1baf`  
		Last Modified: Thu, 17 Oct 2024 06:08:08 GMT  
		Size: 20.8 MB (20842838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8733f6ebe17cf6bd9288e771b20ef3e8623fb0118e887ac501fffddccd07ff5b`  
		Last Modified: Thu, 17 Oct 2024 06:08:03 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf9132130b1c398a4e2da6fffcd1f6cdb97ae92cabd3573482cb658a1bf94c7`  
		Last Modified: Thu, 17 Oct 2024 06:08:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f252495fde81680392bdf7668ef61c1ee3e75288d8342852ef76c3df821da9b2`  
		Last Modified: Fri, 25 Oct 2024 04:25:15 GMT  
		Size: 12.5 MB (12458339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc9f656cdc10aa3e4b69d2430321c14f63b3d7cbe37a5a6e03629aca2315ab1`  
		Last Modified: Fri, 25 Oct 2024 04:25:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dcf03c5dc86ae441a346dbc846301c57e78ba688ab6b4cb4b0da1d1e04c46f`  
		Last Modified: Fri, 25 Oct 2024 04:25:16 GMT  
		Size: 11.6 MB (11640826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a9d41910df2cf195cba4099de635e53edf5dc2fcd2888bab0943531895bce`  
		Last Modified: Fri, 25 Oct 2024 04:25:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735913b9ba3ff1b8e3dd28e6ac1120ad1c1137ebe6d0dd437d9fde22236cb136`  
		Last Modified: Fri, 25 Oct 2024 04:25:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdca763f5a2b3d7eedee6ee1ca5308f5ad5aadf030810edc1ccff106cac4540a`  
		Last Modified: Fri, 25 Oct 2024 04:25:12 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15763b90f5ed5edc5129067eda6665a1029991e4dd54ef7367d346ba1627b72`  
		Last Modified: Fri, 25 Oct 2024 06:39:49 GMT  
		Size: 1.4 MB (1432608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e72560f9badae0877e31bc1f66c572007056fba963662ba28d6b924f43da40`  
		Last Modified: Fri, 25 Oct 2024 06:39:50 GMT  
		Size: 4.7 MB (4719111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c7c64205e257c55f926c701bcef68ce925765b38938a09e84d8de779749972`  
		Last Modified: Fri, 25 Oct 2024 06:39:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524ca7c8e839c81a7b51c6d6c4a750cc2502d4ac7f2ffec778155add98f655e1`  
		Last Modified: Fri, 25 Oct 2024 06:39:48 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3825a158513373b06f6e3ac6af78a0f9eeaaae80acad356f4d8e78e007534f`  
		Last Modified: Fri, 25 Oct 2024 06:39:47 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9047bcd066512717529fe5060bc47683ba21abfc5a3542000ab98bb313694f70`  
		Last Modified: Fri, 25 Oct 2024 06:39:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b5577a0a65df8158bf3cda0381cf49f629fdeda49e2aa052df5d9781f1a3a2`  
		Last Modified: Fri, 25 Oct 2024 06:39:47 GMT  
		Size: 8.2 KB (8198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222e4a1a4c90dced69ce37a708b6bac5c0e00f6f597003640647f2b4ac1a91bd`  
		Last Modified: Fri, 25 Oct 2024 06:39:57 GMT  
		Size: 28.7 MB (28694202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6fc59a31c99e7a4f01b8fb921ebd47d994e9ef4ca00d15f0204aa1b82c549a`  
		Last Modified: Fri, 25 Oct 2024 06:39:47 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; mips64le

```console
$ docker pull monica@sha256:fe8465b9581a3ebdff68cd1fbd985b11cd1d3c1d735376709c69eef95592c58c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186748953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1853df19e3131d7f8a69e7beea619e7d59cbd26f7ddd269df1f86de496443c2`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:19:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 02:19:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 02:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 02:21:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 02:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 02:38:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 02:39:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 02:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 02:39:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 02:40:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 02:40:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:40:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 05:56:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:39:17 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:39:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:39:25 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:40:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:40:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:55:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:55:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:55:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:55:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:56:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:56:06 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:56:10 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:56:14 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 05:54:28 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 05:54:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 06:02:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 06:02:10 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 06:02:15 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 06:02:19 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 06:02:26 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 06:02:33 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 06:02:37 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 06:02:44 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 06:02:50 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 06:02:54 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 06:02:58 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 06:03:02 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 06:04:35 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 06:04:46 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 06:04:54 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 06:05:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3add5d8ad97d2ba7877924447ad98d789dbf096a71456bc495d0a7a74e8afb9`  
		Last Modified: Thu, 17 Oct 2024 08:52:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c68dc9357055fa42cdf1b67ba24c98962d0c7550f84933512d107f85a2c0`  
		Last Modified: Thu, 17 Oct 2024 08:53:18 GMT  
		Size: 80.7 MB (80667204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3adaa11daa51a3a26c065af83992847000612bf88e53a1dcb9feb819b02e3`  
		Last Modified: Thu, 17 Oct 2024 08:52:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1669fc913ce96fa2d4887bd63e3e183b72f0354914597276391ec0d6a3d04262`  
		Last Modified: Thu, 17 Oct 2024 08:53:57 GMT  
		Size: 20.1 MB (20068775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771bdfe6c9af3f18291fcf55f0351d9928f5669267b76b3837a0e3a221e5b09`  
		Last Modified: Thu, 17 Oct 2024 08:53:44 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19aed48dd02184a4d00c1fac98d6cebd3771223e6bd7e4189ad3650fb453a9c`  
		Last Modified: Thu, 17 Oct 2024 08:53:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85a00e5c087c6f5556663db3e6cfe6934839ff14573ed9af6cf588c7a0895b2`  
		Last Modified: Fri, 25 Oct 2024 02:35:25 GMT  
		Size: 12.3 MB (12252872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9c0797ecca3abcd2801a394e8760c0efda6739544272d6a524a6aa5d020496`  
		Last Modified: Fri, 25 Oct 2024 02:35:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b81bf4cee392daf6f2c6c44413fe477b1f9ed6a7c543a094319d31cabe49aef`  
		Last Modified: Fri, 25 Oct 2024 02:35:28 GMT  
		Size: 10.5 MB (10491022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2917dfca72e783f816d90aa903f7786d258ec42e8babd6a73d69e7e6bf87493`  
		Last Modified: Fri, 25 Oct 2024 02:35:20 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331f5fbd1b21480495b1302042052a3bee74c17c7b6b43fa550906978bee5691`  
		Last Modified: Fri, 25 Oct 2024 02:35:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e509c133745221ac67aa29eb09e133f25ded4b285ba1c4a1ada3dcec11f2d236`  
		Last Modified: Fri, 25 Oct 2024 02:35:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011be36be84dcb19c0f05b0f70f3528f397b84597caa132ed7370b7cbffd2b84`  
		Last Modified: Fri, 25 Oct 2024 06:36:29 GMT  
		Size: 1.3 MB (1283814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dca0d46109eec6c0f5f98616ff92fc30f0176663bf31a7ccfa0efe4bc17036`  
		Last Modified: Fri, 25 Oct 2024 06:36:31 GMT  
		Size: 4.4 MB (4356213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24c718b97d14ee3b656fcde70e0e194c9f821eb6f04bf12bc2957b25ecdeb80`  
		Last Modified: Fri, 25 Oct 2024 06:36:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c2016ee0ca233bf1af7a09c0f622f30d909b811557b16d77caeca8ca30ec23`  
		Last Modified: Fri, 25 Oct 2024 06:36:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862319c1818ca71baca974567e3a57113266751abd74a2ad61a2a80f932cd085`  
		Last Modified: Fri, 25 Oct 2024 06:36:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eded499ee46c8d7aec6a52903413f78d8cb7eee0d7dbec4a1f61a6fc0553fdeb`  
		Last Modified: Fri, 25 Oct 2024 06:36:25 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a6d865bb9390933c80c5c34f7bdfba03785983ca1f36a6bfad17b7e9f5e5f1`  
		Last Modified: Fri, 25 Oct 2024 06:36:25 GMT  
		Size: 8.2 KB (8202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c263f2ecb6f1e696dbeedb62e5da095acdfa21e0c94da2b793729b090b3a`  
		Last Modified: Fri, 25 Oct 2024 06:36:55 GMT  
		Size: 28.5 MB (28486674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c972ce55dbf291fcc0b69d536aaa4907f0f016892ac5189375d52302364c7e7`  
		Last Modified: Fri, 25 Oct 2024 06:36:25 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; ppc64le

```console
$ docker pull monica@sha256:300bcec04e1395a95fb0e363513a46b6c196814ae92937ba2e8aef2dd233303f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217556659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d4fae0bff6bf4dcbfb605f0fcfcce62fbed93dad8f7d764ac0be042e5b61b0`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:55:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:55:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:55:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:59:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:59:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:36:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 00:25:00 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 00:25:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 00:25:01 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 00:25:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 00:25:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:28:07 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:28:08 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 00:28:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:09 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:28:09 GMT
EXPOSE 80
# Fri, 25 Oct 2024 00:28:09 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 02:12:06 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 02:12:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 02:14:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 02:14:25 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 02:14:25 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 02:14:26 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 02:14:27 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 02:14:28 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 02:14:28 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 02:14:29 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 02:14:30 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 02:14:30 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 02:14:30 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 02:14:30 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 02:14:55 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 02:14:58 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:14:58 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 02:14:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107c787f39ae7163741fce22e3034e0e43a10e9cbe2ac207f64434e68645221`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627c9d0cca1e0cdb09f43b27bb6bf7d4cca0cad4afc8598940b57844dfe38615`  
		Last Modified: Thu, 17 Oct 2024 03:12:13 GMT  
		Size: 103.3 MB (103326981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cec6f65da0d52cc8cb283752415023a1057b44c8df8167e0417aa9e0b89f632`  
		Last Modified: Thu, 17 Oct 2024 03:11:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6c7dcb4627fcb50a0780a80643b33a0c7eb8fc97cde415a93b5d62392d81d`  
		Last Modified: Thu, 17 Oct 2024 03:12:38 GMT  
		Size: 21.5 MB (21512775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafbf479aff109b64c60ed07d292ff0964425a857bdce0d29ae39eaa8c05d41c`  
		Last Modified: Thu, 17 Oct 2024 03:12:34 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fee26a079f6b552d2d32941008aecadbb3abf8951c2ad54afd96eb2589a1836`  
		Last Modified: Thu, 17 Oct 2024 03:12:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bf9a3f50b556a820b3505902b6fda99bb316b0d3cd7c7f179edeb843004ed9`  
		Last Modified: Fri, 25 Oct 2024 01:00:27 GMT  
		Size: 12.5 MB (12458612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a53cfcf50e538e21591ed2db3678db6b4d8402a117fda2c3fba9e0b74738d45`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89416117a014da531bcadaf40966b5f3a080814ffae1f55f673c154e76a7df6`  
		Last Modified: Fri, 25 Oct 2024 01:00:26 GMT  
		Size: 11.8 MB (11828108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe46118398aad8e5e907a0d79726110a2114cea6d1a975d19812d42b817d778f`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0532a4431ae678b4dbe42418912e53dcabc0132cf8c92dbdf84b40a0e565bc27`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7929ed290a546169e077961ca1bfd228bcd18968389b75c46f802ce3855936`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5be66040304639c75c3642f5d0efaaa8b66c3081d260452ce465b05cc43776`  
		Last Modified: Fri, 25 Oct 2024 02:29:36 GMT  
		Size: 1.6 MB (1563486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5948b3921e8210e3b50516691ee0bb7bbf3488a082832315e4f14a82dcf138fc`  
		Last Modified: Fri, 25 Oct 2024 02:29:36 GMT  
		Size: 5.0 MB (5031625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf5d3278e978dcc857d62bcd5d7ecefb269214d76cc59d96525f116bd250ffd`  
		Last Modified: Fri, 25 Oct 2024 02:29:35 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2445abddc788d1d015e8f4dd2d6c238348e2cd37ff1a20629803eed0f55cdf50`  
		Last Modified: Fri, 25 Oct 2024 02:29:35 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fbcc164d8cd9bdd1c804c61c1e812ae0269c210541e31a0066eae2adfbfa84`  
		Last Modified: Fri, 25 Oct 2024 02:29:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ca45c8c8fe1af345deedd4341fab0804cc4bae957d36ff82b99f44fd2d0724`  
		Last Modified: Fri, 25 Oct 2024 02:29:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135253340798aba0bbcc8af563e018a028e181576c77a889c7c851632ca62744`  
		Last Modified: Fri, 25 Oct 2024 02:29:33 GMT  
		Size: 8.2 KB (8197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe6b18df2576a431bfdf4339343a8e9dd578caebf7842d4a4a48d3ed9d1f710`  
		Last Modified: Fri, 25 Oct 2024 02:29:41 GMT  
		Size: 28.7 MB (28695286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d9aa7b388abbb1e46609ecbb1ef42f1485cd538553d575e9d0f730a0b562cc`  
		Last Modified: Fri, 25 Oct 2024 02:29:33 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `monica:latest` - linux; s390x

```console
$ docker pull monica@sha256:999f75411ac758a8bb70218c68e7f9ce39774e05c9dfbceec7ad90184c595e77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186118827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec2e7b4bb876bcf0285101f6d6b647919541c20f140e3d4eb2decb02c8c4cd8`
-	Entrypoint: `["\/usr\/local\/bin\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:09:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 02:09:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 02:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 02:09:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 02:09:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 02:13:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 02:13:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 02:13:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 02:13:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 02:13:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:51:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:51:45 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:51:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:51:45 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:52:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:52:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:57:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:57:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:57:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:57:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:57:27 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:57:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:57:27 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:57:28 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:57:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 03:19:28 GMT
LABEL org.opencontainers.image.authors=Alexis Saettler <alexis@saettler.org> org.opencontainers.image.title=MonicaHQ, the Personal Relationship Manager org.opencontainers.image.description=This is MonicaHQ, your personal memory! MonicaHQ is like a CRM but for the friends, family, and acquaintances around you. org.opencontainers.image.url=https://monicahq.com org.opencontainers.image.source=https://github.com/monicahq/docker org.opencontainers.image.vendor=Monica
# Fri, 25 Oct 2024 03:19:34 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         bash         busybox-static     ;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:23:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libicu-dev         zlib1g-dev         libzip-dev         libpng-dev         libpq-dev         libxml2-dev         libfreetype6-dev         libjpeg62-turbo-dev         libgmp-dev         libmemcached-dev         libssl-dev         libwebp-dev         libcurl4-openssl-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure intl;     docker-php-ext-configure gd --with-jpeg --with-freetype --with-webp;     docker-php-ext-configure gmp;     docker-php-ext-install -j$(nproc)         intl         zip         bcmath         gd         gmp         pdo_mysql         mysqli         pdo_pgsql         soap     ;         pecl install APCu-5.1.23;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         memcached         redis     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:23:03 GMT
RUN set -ex;         mkdir -p /var/spool/cron/crontabs;     rm -f /var/spool/cron/crontabs/root;     echo '* * * * * php /var/www/html/artisan schedule:run -v' > /var/spool/cron/crontabs/www-data
# Fri, 25 Oct 2024 03:23:03 GMT
ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS=0 PHP_OPCACHE_MAX_ACCELERATED_FILES=20000 PHP_OPCACHE_MEMORY_CONSUMPTION=192 PHP_OPCACHE_MAX_WASTED_PERCENTAGE=10
# Fri, 25 Oct 2024 03:23:04 GMT
ENV PHP_MEMORY_LIMIT=512M PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 03:23:06 GMT
RUN set -ex;         docker-php-ext-enable opcache;     {         echo '[opcache]';         echo 'opcache.enable=1';         echo 'opcache.revalidate_freq=0';         echo 'opcache.validate_timestamps=${PHP_OPCACHE_VALIDATE_TIMESTAMPS}';         echo 'opcache.max_accelerated_files=${PHP_OPCACHE_MAX_ACCELERATED_FILES}';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.max_wasted_percentage=${PHP_OPCACHE_MAX_WASTED_PERCENTAGE}';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> $PHP_INI_DIR/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/limits.ini;
# Fri, 25 Oct 2024 03:23:08 GMT
RUN set -ex;         a2enmod headers rewrite remoteip;     {         echo RemoteIPHeader X-Real-IP;         echo RemoteIPTrustedProxy 10.0.0.0/8;         echo RemoteIPTrustedProxy 172.16.0.0/12;         echo RemoteIPTrustedProxy 192.168.0.0/16;     } > $APACHE_CONFDIR/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 25 Oct 2024 03:23:09 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 25 Oct 2024 03:23:11 GMT
RUN set -ex;         {         echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > $APACHE_CONFDIR/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 25 Oct 2024 03:23:12 GMT
RUN set -ex;     APACHE_DOCUMENT_ROOT=/var/www/html/public;     sed -ri -e "s!/var/www/html!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/sites-available/*.conf;     sed -ri -e "s!/var/www/!${APACHE_DOCUMENT_ROOT}!g" $APACHE_CONFDIR/apache2.conf $APACHE_CONFDIR/conf-available/*.conf
# Fri, 25 Oct 2024 03:23:13 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 03:23:14 GMT
ENV MONICA_VERSION=v4.1.2
# Fri, 25 Oct 2024 03:23:14 GMT
LABEL org.opencontainers.image.revision=32028ce3ce79cef38df5d27a297e5b20680f0065 org.opencontainers.image.version=v4.1.2
# Fri, 25 Oct 2024 03:23:55 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         for ext in tar.bz2 tar.bz2.asc; do         curl -fsSL -o monica-${MONICA_VERSION}.$ext "https://github.com/monicahq/monica/releases/download/${MONICA_VERSION}/monica-${MONICA_VERSION}.$ext";     done;         GPGKEY='BDAB0D0D36A00466A2964E85DE15667131EA6018';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$GPGKEY";     gpg --batch --verify monica-${MONICA_VERSION}.tar.bz2.asc monica-${MONICA_VERSION}.tar.bz2;         tar -xf monica-${MONICA_VERSION}.tar.bz2 -C /var/www/html --strip-components=1;         gpgconf --kill all;     rm -rf "$GNUPGHOME" monica-${MONICA_VERSION}.tar.bz2 monica-${MONICA_VERSION}.tar.bz2.asc;         cp /var/www/html/.env.example /var/www/html/.env;     chown -R www-data:www-data /var/www/html;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:24:03 GMT
COPY multi:84468128947ba1749e6048b0956ef2297175650942a70e8e8bc5df81159d8cc7 in /usr/local/bin/ 
# Fri, 25 Oct 2024 03:24:04 GMT
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
# Fri, 25 Oct 2024 03:24:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641c5b42b9f8e9cc9d65697a8723928dceb047b06377f2d116b9c2a5512b08e6`  
		Last Modified: Thu, 17 Oct 2024 03:32:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e053e76a5c11aa5d9c2fad8f4e883c1ee8ecbb5f99da4b72f7d634499baa8`  
		Last Modified: Thu, 17 Oct 2024 03:32:17 GMT  
		Size: 80.8 MB (80817901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09024721ae9944c22f86461ed99527ff7d8bee6b9b1f1eff3cd1958f41748694`  
		Last Modified: Thu, 17 Oct 2024 03:32:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6555ecb57349a77868c914c1f994918fb11b71be072532ae14ce8d6f30f680`  
		Last Modified: Thu, 17 Oct 2024 03:32:32 GMT  
		Size: 20.1 MB (20099005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abd9390b6a7484b8a8e03acda3fa992d14c0fd34c5f02599c8c829380a9f9af`  
		Last Modified: Thu, 17 Oct 2024 03:32:30 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b03dab143724a784bcb1c6b3d2011f7a1b4423744088d9ff791064fbb0355d`  
		Last Modified: Thu, 17 Oct 2024 03:32:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ef2a4eb0dba6a42fb445f9c902755a5356ccfda2111d794fbe67952072140a`  
		Last Modified: Fri, 25 Oct 2024 02:48:43 GMT  
		Size: 12.5 MB (12457735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60d7385418537c7130426d97c179ffdb27f035b141331aaf8e633521d709599`  
		Last Modified: Fri, 25 Oct 2024 02:48:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49297dd2d180d867cce17abc338e1a6c11ce65c58a5c81f83526fb465e137adc`  
		Last Modified: Fri, 25 Oct 2024 02:48:43 GMT  
		Size: 10.6 MB (10646257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796544b032ec6fe9883ed9748953ccc4e234ea8b5c475d118fa11fb1efba3386`  
		Last Modified: Fri, 25 Oct 2024 02:48:41 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaf4946bb4f7f0bd46184854938ffad4b0bb3a0f513b4d80779805a8d7dd73f`  
		Last Modified: Fri, 25 Oct 2024 02:48:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262b74e5a53c844ff3348b7c47478d90042be3edabb8b3411ea0dd8ebe52fc86`  
		Last Modified: Fri, 25 Oct 2024 02:48:41 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c03b1a45c656af3bbe6e65fefda93577cf1a4237e5b51caedb72638e73561`  
		Last Modified: Fri, 25 Oct 2024 03:41:14 GMT  
		Size: 1.4 MB (1365132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc8260c2bee535bbf88bd78a1450679bf6d3905527e7e2eb604423167e8f8d9`  
		Last Modified: Fri, 25 Oct 2024 03:41:14 GMT  
		Size: 4.5 MB (4532259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97090586c16e7bd313d54b951d008d4f5f0669f048b752f29ce6fc1452a3644a`  
		Last Modified: Fri, 25 Oct 2024 03:41:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4728f67f4c8fd56b92d2b7e1ec743e980a62b08a26dcc9c144b9148ef0352df6`  
		Last Modified: Fri, 25 Oct 2024 03:41:14 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5d748de671d2f77b9085db83c87fc25620ae9005d575c91d98f5377bad1efd`  
		Last Modified: Fri, 25 Oct 2024 03:41:12 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451a58375819dee5fc6c1ab19b056e87bc52fa56aca85cb23177cee38f30f78c`  
		Last Modified: Fri, 25 Oct 2024 03:41:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f3eef7aade21d5960ae503ed48e378bb93e262b104865c10775c2305e1e2c3`  
		Last Modified: Fri, 25 Oct 2024 03:41:12 GMT  
		Size: 8.2 KB (8203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64cf911f7c392b434f1d54361e0078c9458ac64a1fa0953ede815322d65191a`  
		Last Modified: Fri, 25 Oct 2024 03:41:19 GMT  
		Size: 28.7 MB (28692858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39cdf65de735053509933bec0a99f330b96e905060bb4fdc2deb33fabc93b4a`  
		Last Modified: Fri, 25 Oct 2024 03:41:12 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
