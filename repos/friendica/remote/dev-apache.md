## `friendica:dev-apache`

```console
$ docker pull friendica@sha256:324cecb2f4576452c04eaedd36f94a989f5a8a3f9849c2a373b5f081d7ebee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:dev-apache` - linux; amd64

```console
$ docker pull friendica@sha256:bcf67075bc7aae335298eab1856f2e4127eaf73944d35f47d9ce981bd6921ec9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160167548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b915603b7bd3beff4e29d7bfb7b1cd9a46bb3dc9187dc91e4460d5661a70c0cd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 13:44:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 13:44:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 13:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 13:44:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 13:44:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 13:53:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 13:53:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 13:53:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 13:53:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 13:53:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 13:53:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 13:53:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 13:53:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 13:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 13:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 13:53:24 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 13:53:24 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 13:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 13:53:24 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 13:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 13:53:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 13:58:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:26:19 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:26:20 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:26:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:26:20 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:26:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:26:20 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:26:21 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:26:21 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 23:52:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Jun 2020 23:52:43 GMT
ENV TINI_VERSION=v0.18.0
# Tue, 02 Jun 2020 23:52:47 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Tue, 02 Jun 2020 23:55:38 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 23:55:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 23:55:39 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 23:55:40 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Wed, 03 Jun 2020 00:01:41 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Wed, 03 Jun 2020 00:01:42 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Wed, 03 Jun 2020 00:01:42 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Wed, 03 Jun 2020 00:01:42 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Wed, 03 Jun 2020 00:01:43 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 03 Jun 2020 00:01:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8437c5af8ea63badbd2e04c30da73d703b4bcaa51723033bd55ecc55c3b2088d`  
		Last Modified: Fri, 15 May 2020 15:09:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87afd21c1db9de3d9bebb469d3b858492ea5bad6775bcecec3bd077b55dc0e9`  
		Last Modified: Fri, 15 May 2020 15:10:06 GMT  
		Size: 67.4 MB (67447253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae695bc96cd1a688e078a6723e5d48b62bbee3b084ba3752e6f62762136e8b1a`  
		Last Modified: Fri, 15 May 2020 15:09:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53de6c4594b85e9abfb6944da89fdaa349ac06a3356961b0aaae2538df3f92e4`  
		Last Modified: Fri, 15 May 2020 15:10:18 GMT  
		Size: 17.1 MB (17125338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d50f6d986104e53f68d2cde0fb652648d24eed922bd433955e6971c33c2eb75`  
		Last Modified: Fri, 15 May 2020 15:10:14 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682e8c7c96cf0f12775ba0eebc4c78ba9208db2f4e326f90619e555e65faaf6`  
		Last Modified: Fri, 15 May 2020 15:10:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135710d6acc5ccec6e50d00a35c3e2e198e02c9e7771f1eed33ad6a3d3794f4c`  
		Last Modified: Fri, 15 May 2020 15:10:17 GMT  
		Size: 12.5 MB (12464937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0442d30c63adaf22f834fc175b765a69fcf78d510e9fc1e90076d8cccaacc`  
		Last Modified: Fri, 15 May 2020 15:10:13 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63b53f6351530a8dd257c9b64dee76ff9843bf2c67dca908ef7362d8308e5b9`  
		Last Modified: Fri, 15 May 2020 15:10:17 GMT  
		Size: 13.8 MB (13799158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09b0921f22eb7877f306e2b212144b30a5791f31366d9d1b43692c4599237ee`  
		Last Modified: Tue, 02 Jun 2020 21:31:39 GMT  
		Size: 2.3 KB (2300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de0ba48f4c5a1d89f476167a0e93a2863cca4de8417554e6a1571b8a47a673`  
		Last Modified: Tue, 02 Jun 2020 21:31:39 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0329a664d3ebd534140333df61255ae3074efe8d7aea45488c39abaa4b5cd`  
		Last Modified: Tue, 02 Jun 2020 21:31:39 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b216281e23e9f22116803164518551fd1e5d6de28bf253396bef91250f016f`  
		Last Modified: Wed, 03 Jun 2020 00:02:24 GMT  
		Size: 15.1 MB (15078508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c68bc97d61b6777237455a2df86d475a4c4b32276b0828c7c3b560bdaee1f`  
		Last Modified: Wed, 03 Jun 2020 00:02:03 GMT  
		Size: 16.3 KB (16288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cadc42c3acc9b5dab22788b175cc7cf7ee4eb0a415046569695c37f65d1cbb4`  
		Last Modified: Wed, 03 Jun 2020 00:02:04 GMT  
		Size: 11.7 MB (11705809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791cd92667da86fd50c68ec44778f8f197c22ea548c7f8f9c4fcd8b4db931abd`  
		Last Modified: Wed, 03 Jun 2020 00:02:03 GMT  
		Size: 566.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1e8106aab82fdf8083bd68fa53b40270559a9155a429b940c86189b5c03df1`  
		Last Modified: Wed, 03 Jun 2020 00:02:02 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9692bae350afe099221b31b9a826512f502040608a2787c139ed0397daf0177e`  
		Last Modified: Wed, 03 Jun 2020 00:02:02 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c06f150b38bc522a6c177f2b361bf9df2fd8089a7ea9ff0227fb284809c5e`  
		Last Modified: Wed, 03 Jun 2020 00:02:02 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:f9d7f4fe224bd86b79d0c2e163fb2b8adea3b97085d87b9de49733055b4ba7dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146311094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268566a16569e3eb9093860c134b3200276c7a88810badb9abb3d4f5620dd80`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 00:55:49 GMT
ADD file:af949d376cc9a2ac87d0052d22fe17be59dfe65905f0645d1a903b359208d26d in / 
# Tue, 09 Jun 2020 00:55:51 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:47:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 03:47:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 03:48:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:48:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 03:48:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 03:52:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 03:52:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 03:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 03:53:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 03:53:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 03:53:08 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 03:53:08 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 03:53:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 03:53:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 03:53:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 03:53:11 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 09 Jun 2020 03:53:11 GMT
ENV PHP_VERSION=7.3.18
# Tue, 09 Jun 2020 03:53:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Tue, 09 Jun 2020 03:53:12 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Tue, 09 Jun 2020 03:53:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 03:53:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:57:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 03:57:04 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:57:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 03:57:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 03:57:13 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 03:57:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:57:15 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 03:57:16 GMT
EXPOSE 80
# Tue, 09 Jun 2020 03:57:16 GMT
CMD ["apache2-foreground"]
# Tue, 09 Jun 2020 14:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 14:03:25 GMT
ENV TINI_VERSION=v0.18.0
# Tue, 09 Jun 2020 14:03:42 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Tue, 09 Jun 2020 14:09:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 14:09:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 09 Jun 2020 14:09:24 GMT
VOLUME [/var/www/html]
# Tue, 09 Jun 2020 14:09:26 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 09 Jun 2020 14:17:12 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 09 Jun 2020 14:17:13 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 09 Jun 2020 14:17:15 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 09 Jun 2020 14:17:16 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 09 Jun 2020 14:17:17 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 09 Jun 2020 14:17:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c9b35828d9245f0a85299b96b2d9b0d70390689cf7df0fe7ef29ca6028c0ab56`  
		Last Modified: Tue, 09 Jun 2020 01:03:09 GMT  
		Size: 21.2 MB (21197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54880485c9e08abdbce3b0f76c307a0b9f7aa394b2ce9bac77918ff8a8e31dee`  
		Last Modified: Tue, 09 Jun 2020 04:46:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f743b703af8a45a29170c64a7bc2ac5c574f5f1b7f2b048aff482141d9e1a88`  
		Last Modified: Tue, 09 Jun 2020 04:46:51 GMT  
		Size: 57.4 MB (57430558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc54e06c6d384a48529a64b0b997115c84fb8158108be2409619e46d249e5427`  
		Last Modified: Tue, 09 Jun 2020 04:46:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a131ad31f965fcf10f5e6480abbff66bd851d40dc38f8ee1c33e46e4273d83`  
		Last Modified: Tue, 09 Jun 2020 04:47:10 GMT  
		Size: 16.6 MB (16643927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1336bb4bbf07a2c5e817a06d08c35627e120c4249a0b72da3f8d71161931fc`  
		Last Modified: Tue, 09 Jun 2020 04:47:05 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8b372ad30148c4c47000aef600b46aabe5ba94f16068430ff0eb26a59444d5`  
		Last Modified: Tue, 09 Jun 2020 04:47:04 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7617370cf91905f89b7097a9581dbd9510e98873db1971ba22c4e8309dcff97b`  
		Last Modified: Tue, 09 Jun 2020 04:47:05 GMT  
		Size: 12.5 MB (12463001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181cee44e1ac39cf1734ca0b97b7e79ee4319dcf210147daf96f73f721c09892`  
		Last Modified: Tue, 09 Jun 2020 04:47:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb43ec1e08b866c3d7b6fa98fc22e225c56f289c06ff49b13211aeff71fd954b`  
		Last Modified: Tue, 09 Jun 2020 04:47:09 GMT  
		Size: 13.1 MB (13071362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63d55bdbbc3fa3aa161f839ed525da68aa60e102c22aedee948326ff1274de`  
		Last Modified: Tue, 09 Jun 2020 04:47:02 GMT  
		Size: 2.3 KB (2294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e80a8b316a678e8a213a3c127a2d602bf5b6f122c62cf851af546cc6de26`  
		Last Modified: Tue, 09 Jun 2020 04:47:02 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82780f4309a433ac422a947c7a1d529b53e3440db502b147b7b15561a27df9f`  
		Last Modified: Tue, 09 Jun 2020 04:47:02 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1128d768d2e9d04be0c5b8cee6b827c16e1dfc60e281c1753ff968a58d78e800`  
		Last Modified: Tue, 09 Jun 2020 14:17:51 GMT  
		Size: 14.0 MB (14013348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d852a8fa17167b0a34447b70e1cce7e095d288cd22c9653fef02e4d78f6b4e97`  
		Last Modified: Tue, 09 Jun 2020 14:17:45 GMT  
		Size: 15.7 KB (15713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d6302f8dbb7ca9a681544a8bbb8ecd3668d9dd3652f6166fe9c492e072314`  
		Last Modified: Tue, 09 Jun 2020 14:17:48 GMT  
		Size: 11.5 MB (11465309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2416164bae43836b946e81e8fd36d949fe68d53e79bb0377acbfd1ce37a9bb`  
		Last Modified: Tue, 09 Jun 2020 14:17:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba5828317ac7f69a75c6f427f79d6f780d2901a950926e1127dc211833d1b90`  
		Last Modified: Tue, 09 Jun 2020 14:17:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5c52280664b341ff0840d576d8683a4408fced785201e9d377173e7d7e3f69`  
		Last Modified: Tue, 09 Jun 2020 14:17:44 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bfdb93fe92d113de0d9a8142668255701a0e16345c5de4d1768df727f3beee`  
		Last Modified: Tue, 09 Jun 2020 14:17:44 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:b41940335af5b372658143316ed94621e882a8935a935a7534059a3da57da81e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137346462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c2002dd6ac1e5444366bb72298e8350b46a00602e3cf526826702b835d84cb`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 01:06:56 GMT
ADD file:a0ecfe1283dbc15e795cd274e422095545ef6e8af80bc23ee7063abb597a5a88 in / 
# Fri, 15 May 2020 01:07:00 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:12:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 05:12:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 05:13:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 05:13:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 05:13:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 05:17:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 05:17:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 05:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 05:18:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 05:18:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 05:18:11 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 05:18:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 05:18:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 05:18:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 05:18:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 05:18:15 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 05:18:15 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 05:18:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 05:18:17 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 05:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 05:18:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 05:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 22:05:50 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 22:05:53 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 22:05:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 22:05:55 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 22:05:55 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 22:05:56 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 22:05:57 GMT
EXPOSE 80
# Tue, 02 Jun 2020 22:05:58 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 22:35:19 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Jun 2020 22:35:20 GMT
ENV TINI_VERSION=v0.18.0
# Tue, 02 Jun 2020 22:35:29 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Tue, 02 Jun 2020 22:41:12 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 22:41:15 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:41:17 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:41:20 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 02 Jun 2020 22:53:00 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 22:53:02 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 22:53:04 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 22:53:06 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 22:53:07 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 22:53:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:90cadb81644e46b7fbfb33027f8b34af18f1e04db99f6b29cc1ff98aafe9b5d6`  
		Last Modified: Fri, 15 May 2020 01:15:03 GMT  
		Size: 19.3 MB (19304729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d9f273db153700d1ec18180aff2cf9021e79864d964ad6e6c985427a28137b`  
		Last Modified: Fri, 15 May 2020 06:08:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f57f6eaa08eacd0de6b3c5a550417bc2ecf5da07ed23b775f29179a834442b1`  
		Last Modified: Fri, 15 May 2020 06:09:06 GMT  
		Size: 53.6 MB (53595358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39abdbe68b8491ee7addea5e9435f8524191f2e468cf25d578255d0bad4c5df`  
		Last Modified: Fri, 15 May 2020 06:08:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd4db0a408f7cedbdf1b718138d317be2c6a3de82a0f6cf83d5b8e5e1324b6`  
		Last Modified: Fri, 15 May 2020 06:09:22 GMT  
		Size: 16.2 MB (16159816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0479d20475c424742ebf3860a503b6bb64c1bbc567c8369c825c697d25f3ee13`  
		Last Modified: Fri, 15 May 2020 06:09:17 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b119938ed98d365f2d7798ba17c6054fcc556aaf1861e5255e4690d3243cc802`  
		Last Modified: Fri, 15 May 2020 06:09:17 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cd5e1de0607b6c8652b210e9ff3cfaa1a9438689d7a3d887585ce4bbda6c95`  
		Last Modified: Fri, 15 May 2020 06:09:18 GMT  
		Size: 12.5 MB (12463219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ac271f7d39ee083a62873efc6e4975bdbca57823c01a0e61fe2d308fdbed9d`  
		Last Modified: Fri, 15 May 2020 06:09:15 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ecb84b713ca4c78bcb0637e25c886c5a23c6f429cceac135ff09fad61a93e`  
		Last Modified: Fri, 15 May 2020 06:09:20 GMT  
		Size: 12.4 MB (12390751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d8c4b5a8c58bcd77494c0c18d6a0fe8fd6831bff55d5fa0d2d5a95609f8b6c`  
		Last Modified: Tue, 02 Jun 2020 22:16:29 GMT  
		Size: 2.3 KB (2299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89823e2a7d99e8adecc40327db7bd015a1b8b186a3bfc1d722abe6dc6c4243f9`  
		Last Modified: Tue, 02 Jun 2020 22:16:29 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3eeb598fb113bb27a46dc2ff3a093fc88d67c97240692d20aec69771bfb74c`  
		Last Modified: Tue, 02 Jun 2020 22:16:29 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc46093e97229bc1efcb1a2d44d1b6dcf336a3f1419e610ed8b1bfd45043e63`  
		Last Modified: Tue, 02 Jun 2020 22:53:51 GMT  
		Size: 12.7 MB (12735759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada3cd1cd9c526eb77fcad1f7fdda97d16026b557e372bc2563fb02af628251`  
		Last Modified: Tue, 02 Jun 2020 22:53:49 GMT  
		Size: 15.0 KB (14954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13907b7bc0003a243cdd0c9d2567b84a587fd67d66971342a0a7fbee10afcb`  
		Last Modified: Tue, 02 Jun 2020 22:53:50 GMT  
		Size: 10.7 MB (10671309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c59533b714eb0eec66a182d6ac41ae8f6f667882923e9bcd8b04a1233600e3a`  
		Last Modified: Tue, 02 Jun 2020 22:53:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566aa551e478ebcf39ac549edb642f133660e7d508c7c40a79d9906888144ef2`  
		Last Modified: Tue, 02 Jun 2020 22:53:47 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcad1b43f77740768a60c66c094b3fe6352f131afb20849b3c87d25b4da27b0`  
		Last Modified: Tue, 02 Jun 2020 22:53:47 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad342078bd959743fe50c9f5099d6e1fe8c5d2dc17e2bda119d36963c0fcfb89`  
		Last Modified: Tue, 02 Jun 2020 22:53:47 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:9a97dcf80e35f78cef4d3144e8bdb7c4ba3ae0010c65236a2bfd59be3a427462
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144369051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060be3fe511abe2666f8bcaf846247085e6027e9ac941623eda99a48a83fe5dd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 12:48:45 GMT
ADD file:a808acc4967ce5ecee8ba7a3e8769d6b91e38fecad2a792c8bd5aeef0007c6c0 in / 
# Fri, 15 May 2020 12:48:49 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:20:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 15:20:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 15:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 15:21:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 15:21:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 15:25:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 15:25:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 15:25:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 15:25:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 15:26:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 15:26:03 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 15:26:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 15:26:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 15:26:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 15:26:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 15:26:08 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 15:26:08 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 15:26:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 15:26:10 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 15:26:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 15:26:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 15:29:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:52:10 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:52:15 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:52:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:52:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:52:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:52:18 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:52:19 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:52:19 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 22:43:59 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Jun 2020 22:44:01 GMT
ENV TINI_VERSION=v0.18.0
# Tue, 02 Jun 2020 22:44:07 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Tue, 02 Jun 2020 22:49:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 22:49:49 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:49:50 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:49:52 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 02 Jun 2020 23:01:07 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 23:01:08 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 23:01:10 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 23:01:11 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 23:01:12 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 23:01:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7f439267e48f39a2f7463f7ec54d4ccd7f849de1dd6fd575bc2ee51c096b1da5`  
		Last Modified: Fri, 15 May 2020 12:56:01 GMT  
		Size: 20.4 MB (20375567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856d7c165a0631482a2e3c515210a7aba8b3fcbb2e8007b232d0e482be064f9`  
		Last Modified: Fri, 15 May 2020 16:18:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d01ed52b02845848ed94d7868732ca33e2074b1a8ebd727d2144b1c7e04fefb`  
		Last Modified: Fri, 15 May 2020 16:18:41 GMT  
		Size: 57.6 MB (57630154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3ef083af0037f515c5d25b48d994f1e8a4a50ff060b38c62f90ba1194e872`  
		Last Modified: Fri, 15 May 2020 16:18:07 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe901931ae17e5eef7f86083607d4a0fdf4034dd091fc6278793b6e060a285`  
		Last Modified: Fri, 15 May 2020 16:18:57 GMT  
		Size: 16.7 MB (16708471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9cdca74d19fed34916da78d8cb05a1046e733905693634fec4e6d05126f373`  
		Last Modified: Fri, 15 May 2020 16:18:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e45dc8ecd219796fcad219841fd13179c1fe6920db4717fcec05da88159ad0c`  
		Last Modified: Fri, 15 May 2020 16:18:52 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee911b801ce1345f6457d8a53e6336e9dd1b4a045c51880cdce94582adbf9d2f`  
		Last Modified: Fri, 15 May 2020 16:18:55 GMT  
		Size: 12.5 MB (12463120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f071ec3860b5d12c73508a86fa8fcf67a135ba6c15cc5466ebc596c9afb7d00f`  
		Last Modified: Fri, 15 May 2020 16:18:50 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae62b31898c2f3cd838b39b02546afab9eecbac2deac30c9d04e204ef94c576`  
		Last Modified: Fri, 15 May 2020 16:18:55 GMT  
		Size: 12.9 MB (12863439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8940ae50e2590035dd48ba0801f76ac33d753f08923065c11159f0e1eb62956c`  
		Last Modified: Tue, 02 Jun 2020 22:05:30 GMT  
		Size: 2.3 KB (2297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505fa960dd21599b13bd2745e78752093e40d3b656f913552f9ed09cd1b9419f`  
		Last Modified: Tue, 02 Jun 2020 22:05:29 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36472b553462c6c4a04415cf330e14bc5b5f796b5d46941c1e9568dd79a83ea1`  
		Last Modified: Tue, 02 Jun 2020 22:05:30 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97817d3215d24326cbebc4d0716c89d11c5011e8320a92b4176b5200f5aeda30`  
		Last Modified: Tue, 02 Jun 2020 23:01:53 GMT  
		Size: 13.6 MB (13617700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f82dd1b179f0a7932cd3dcef8b57ac221536a89dc434c9c3f74ad3a87dbb8a`  
		Last Modified: Tue, 02 Jun 2020 23:01:50 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce94b35bf0bdac852ceb213497cae4c47265f3261ed83430e807957aa52bf0b`  
		Last Modified: Tue, 02 Jun 2020 23:01:51 GMT  
		Size: 10.7 MB (10684130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9561f35f74f485b933bfb937d21d86237ca5b830c8489b000f7127dca64f`  
		Last Modified: Tue, 02 Jun 2020 23:01:47 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4381f277d7e22221a82cb1c4248ae6b5e8d4344f1fd4d72816ad4fb245273b80`  
		Last Modified: Tue, 02 Jun 2020 23:01:48 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c64349d4949030d17d9188cc740389a2f8941ca070dbbc41e2132661fa5532`  
		Last Modified: Tue, 02 Jun 2020 23:01:48 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795f8b506ef5c5a71d882ade2c0d639273ae8d8aeb57edd9dc5036d85b4bd19e`  
		Last Modified: Tue, 02 Jun 2020 23:01:48 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; 386

```console
$ docker pull friendica@sha256:c0a10979b58cd568f7a6c97d77173d066e2fa463af5cb3c723734a275dc60397
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167411635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034115612d161ca2e4f2537be47acef4b64545d7f57a9a6a04606f62860e782`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 07:12:59 GMT
ADD file:2008ddcaad4151bac993aa4ee2257b34c811b262f730e06af22a1feb84e3c81f in / 
# Fri, 15 May 2020 07:13:00 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:45:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:45:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:46:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:46:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:54:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:54:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:55:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:55:02 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:55:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:55:03 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:55:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:55:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:55:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:55:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 12:55:04 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 15 May 2020 12:55:04 GMT
ENV PHP_VERSION=7.3.18
# Fri, 15 May 2020 12:55:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Fri, 15 May 2020 12:55:05 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Fri, 15 May 2020 12:55:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 12:55:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 13:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:43:04 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:43:05 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:43:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:43:05 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:43:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:43:05 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:43:06 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:43:06 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 22:37:35 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Jun 2020 22:37:35 GMT
ENV TINI_VERSION=v0.18.0
# Tue, 02 Jun 2020 22:37:38 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Tue, 02 Jun 2020 22:40:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 22:40:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:40:30 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:40:31 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 02 Jun 2020 22:47:38 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 22:47:38 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 22:47:39 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 22:47:39 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 22:47:40 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 22:47:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a5a8cf045c967a24918301a73357fee572dec550e91771d3a97fb26fc5d61070`  
		Last Modified: Fri, 15 May 2020 07:23:21 GMT  
		Size: 23.1 MB (23147615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d5d39b8fa1d05755ff52601396c5dc38c5e88950fdf1285e510b6b50790f77`  
		Last Modified: Fri, 15 May 2020 14:33:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a365113229984abcb9a6c7d9aa5f87fef8800e02737d5ca2f9e40dee08b7279`  
		Last Modified: Fri, 15 May 2020 14:34:12 GMT  
		Size: 71.5 MB (71524494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec8360fe02529c4601fd2b2176d64f304837d1455c653d22875d1ce0a46b99`  
		Last Modified: Fri, 15 May 2020 14:33:50 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929758b5c7739ede888ae1ee868019089a206ea834ba170dea8ae9d0d446132e`  
		Last Modified: Fri, 15 May 2020 14:34:25 GMT  
		Size: 17.6 MB (17559761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e1ee9e77425f35cd6ada17258b287e0527c83b4f812a9cb18cbe68377cf7a6`  
		Last Modified: Fri, 15 May 2020 14:34:19 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb54a3c775ca2d22d03756db5d61e07590b9a037cb0114891570c91efeb2ae7`  
		Last Modified: Fri, 15 May 2020 14:34:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d0a94273e9db4828cfa09de49d02eafe2681068c05792d79f01b937e90ebe`  
		Last Modified: Fri, 15 May 2020 14:34:21 GMT  
		Size: 12.5 MB (12464454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074f2024bfbb84459a08b535462ae6baf473112b326832ee3ef9b0176e4d9337`  
		Last Modified: Fri, 15 May 2020 14:34:18 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcf094a598960b0baa451634a1baca4e9d1b0f4f91c7c1a14429a19d02cb1b1`  
		Last Modified: Fri, 15 May 2020 14:34:24 GMT  
		Size: 14.1 MB (14122919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248ac3997ddbb13cd347879973be50b2a80f639c88e96e4e95e24c961e3a73c3`  
		Last Modified: Tue, 02 Jun 2020 21:48:37 GMT  
		Size: 2.3 KB (2297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce7b181f882e1464d7b0c697a32b9cdc36db108a796a085acf25847af2f2762`  
		Last Modified: Tue, 02 Jun 2020 21:48:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b758744c834e1fa1cc76b773d7f09dee6a43718b639bfb75429f92c10818bf15`  
		Last Modified: Tue, 02 Jun 2020 21:48:37 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302a5549068f6a066d3aea0eb7fa38df2a91643ce681b1d569cc9f9ba2a5adc2`  
		Last Modified: Tue, 02 Jun 2020 22:48:05 GMT  
		Size: 16.8 MB (16799518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c839ea1c387f66a66a5596fe45a8ebfbd8a94fc90bee3d57674b9df7cd768b5`  
		Last Modified: Tue, 02 Jun 2020 22:48:01 GMT  
		Size: 16.3 KB (16311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7cfa569a89cd44e7dba5581d7ae37028cc12ae74209ca00aaedc313ca0fc96`  
		Last Modified: Tue, 02 Jun 2020 22:48:04 GMT  
		Size: 11.8 MB (11766191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9b12faa6d843f4df9b256fb3772dc154fbab611194675634e01355eeab389d`  
		Last Modified: Tue, 02 Jun 2020 22:48:00 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886399f34fc3d5581ea494819a35dd10fa18af596ad347713ddf95ae3f0eab96`  
		Last Modified: Tue, 02 Jun 2020 22:48:00 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282c118d54db84cc64b00067ea91849e838a8a53f52dad44bf41525c31664fd5`  
		Last Modified: Tue, 02 Jun 2020 22:48:00 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c59dc3606c6ee2d68ea26d3d820b492c2e3cc753ff80414d63c26168ce6ffb`  
		Last Modified: Tue, 02 Jun 2020 22:48:00 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:2c2ba9ce1c40ff4298529b090c197930cf0263d2b28091eee79ab65da30b6f7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154416048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430b8e8e7b553c14adbc39c005eb3dde9577789ab07ca1a04f83b1b766eafa7`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 May 2020 22:42:09 GMT
ADD file:341dbc564992a44e81b3a4f399f7de14d7340a45b73c577edb78e16da2c14584 in / 
# Wed, 13 May 2020 22:42:12 GMT
CMD ["bash"]
# Mon, 18 May 2020 09:23:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Mon, 18 May 2020 09:23:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 18 May 2020 09:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 18 May 2020 09:25:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 May 2020 09:25:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Mon, 18 May 2020 09:32:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 18 May 2020 09:32:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 18 May 2020 09:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 18 May 2020 09:33:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 18 May 2020 09:34:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 18 May 2020 09:34:13 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Mon, 18 May 2020 09:34:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Mon, 18 May 2020 09:34:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 May 2020 09:34:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 May 2020 09:34:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 May 2020 09:34:29 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Mon, 18 May 2020 09:34:33 GMT
ENV PHP_VERSION=7.3.18
# Mon, 18 May 2020 09:34:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.18.tar.xz.asc
# Mon, 18 May 2020 09:34:40 GMT
ENV PHP_SHA256=7b3e2479a8d6fd7666dcdef8aec50d49c4599cc6ee86e48d41724cfd99cc9e58 PHP_MD5=
# Mon, 18 May 2020 09:35:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 18 May 2020 09:35:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 18 May 2020 09:41:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:23 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:29 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:36 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:38 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:40 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 22:07:57 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Jun 2020 22:08:00 GMT
ENV TINI_VERSION=v0.18.0
# Tue, 02 Jun 2020 22:08:12 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Tue, 02 Jun 2020 22:17:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.2.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jun 2020 22:17:12 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 02 Jun 2020 22:17:15 GMT
VOLUME [/var/www/html]
# Tue, 02 Jun 2020 22:17:25 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 02 Jun 2020 22:35:24 GMT
ENV FRIENDICA_VERSION=2020.06-dev
# Tue, 02 Jun 2020 22:35:26 GMT
ENV FRIENDICA_ADDONS=2020.06-dev
# Tue, 02 Jun 2020 22:35:29 GMT
COPY multi:79c18253e95b11e5d803cb19685ac5cb4fcedfeda73215d7e2e3f89d93570667 in / 
# Tue, 02 Jun 2020 22:35:29 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 02 Jun 2020 22:35:31 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 02 Jun 2020 22:35:36 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3b6ae894780534c0f99588e9cce4beb8fb7884b4578e6206b72f2db75116bb1c`  
		Last Modified: Wed, 13 May 2020 23:02:51 GMT  
		Size: 22.8 MB (22785361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d6bef61becd2d2173ebba5462183c8dc5cc75db66342fc1b8770f2bacf84fb`  
		Last Modified: Mon, 18 May 2020 12:20:20 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95c753681781cc06a716ddf91985334e35e3cbeb23869a9ed68a9257b4eda26`  
		Last Modified: Mon, 18 May 2020 12:22:03 GMT  
		Size: 61.8 MB (61836608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f340ca9a56757d4401162fc2cc55ba42918162430fcc97a32b2b59d94151873`  
		Last Modified: Mon, 18 May 2020 12:20:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74979f7d51c379b15d3863a95c87cef653017734e90c2385b5cd1cf7105c92c6`  
		Last Modified: Mon, 18 May 2020 12:22:44 GMT  
		Size: 17.3 MB (17341296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3996e5c97c18bc1a8842731a122383fd9cf18a7e12dd9b712d35fe2a0665c7`  
		Last Modified: Mon, 18 May 2020 12:22:31 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954985e68169ba2ff830b796902623d773ccf374a1faf29bddaa254501162f28`  
		Last Modified: Mon, 18 May 2020 12:22:28 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f740c18f12faabf26b908d4ee5be222a9b3a1023590bacd7c8f1c80db28848c`  
		Last Modified: Mon, 18 May 2020 12:22:29 GMT  
		Size: 12.5 MB (12463797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04124574578ad8536a47ba3d61c29b672624cd0bc1a894863306bae6b2f50c83`  
		Last Modified: Mon, 18 May 2020 12:22:20 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b660b5e388f0ed47d98febaf5574b97f219bfacb16523698d4a35c18a1b937c3`  
		Last Modified: Mon, 18 May 2020 12:22:50 GMT  
		Size: 13.6 MB (13585777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf07040a7d70a9e8bc87ae201cb0ca5f3654f3c36831d64c7e037b884ce0c5d3`  
		Last Modified: Tue, 02 Jun 2020 21:43:38 GMT  
		Size: 2.3 KB (2294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d711e3d7b632cfd498cdab95c3eba871fc580f18ccf94957ce4c321400badc`  
		Last Modified: Tue, 02 Jun 2020 21:43:38 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf63bcf50641c411492a5c4c02a8ba1d038d3a9d9e9b9ba7bd9e79250122fd8`  
		Last Modified: Tue, 02 Jun 2020 21:43:38 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d3d52762d909146e5a8d36444458b77cabed57c34d4d276f90a1eb5e5324b5`  
		Last Modified: Tue, 02 Jun 2020 22:36:28 GMT  
		Size: 14.9 MB (14944862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2683963f5936ef39bae63d1057bef244de281f567fd6a93cec04860b84dcd0`  
		Last Modified: Tue, 02 Jun 2020 22:36:25 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473c7b16b59e2a2cc3aff18b5bdb5f5fef69701439e9f801adf0f7b1fb6bde98`  
		Last Modified: Tue, 02 Jun 2020 22:36:25 GMT  
		Size: 11.4 MB (11431263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7da4b78db54c8573d1d202903e5c6634df4b24b74acf27080018ecc5243858`  
		Last Modified: Tue, 02 Jun 2020 22:36:22 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c018c607b9e1edfdf677c44ad1e22f7545ac4a1e47d5dad538aff033c0c9a3`  
		Last Modified: Tue, 02 Jun 2020 22:36:22 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee733c31b32de0094a1f951cfc80088f5956b308f019d5d1d94ef2b08641dcb2`  
		Last Modified: Tue, 02 Jun 2020 22:36:22 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f99f4e30f6d2b74a6e71169086b9edeb5004cb42559b09abd8612fdd6a9aa8b`  
		Last Modified: Tue, 02 Jun 2020 22:36:22 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
