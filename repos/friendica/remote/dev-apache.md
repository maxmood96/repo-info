## `friendica:dev-apache`

```console
$ docker pull friendica@sha256:d293093a38f1891892cff8e2e90790239d1fa3d046a7826a335f13845c8022d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `friendica:dev-apache` - linux; amd64

```console
$ docker pull friendica@sha256:a79d5340b7e23c17218ccd00a0051eef243a4d30a8174efd845ec6fddd89c07b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219151583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcece582ca56a569aee8af22253189fa0e247a81e218f952e994d000a97b9b3f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Thu, 17 Oct 2024 01:37:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:37:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:37:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:37:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:37:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:37:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:37:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:31:59 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:31:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:31:59 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:32:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:35:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:35:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:35:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:35:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:35:19 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:35:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:35:20 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:35:20 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:35:20 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 04:10:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 25 Oct 2024 04:10:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:10:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Oct 2024 04:13:02 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:13:02 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 25 Oct 2024 04:13:02 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 04:13:03 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 25 Oct 2024 04:13:03 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 04:13:04 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 25 Oct 2024 04:13:04 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 25 Oct 2024 04:13:04 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Fri, 25 Oct 2024 04:13:04 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Fri, 25 Oct 2024 04:13:09 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 25 Oct 2024 04:13:09 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 25 Oct 2024 04:13:10 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 25 Oct 2024 04:13:10 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 25 Oct 2024 04:13:10 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:2d49eea953465a4ecc3add99a641e83024465f0e22bd7b3d7500a3ba920a8a04`  
		Last Modified: Thu, 17 Oct 2024 04:20:48 GMT  
		Size: 19.3 MB (19279196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eca754d321489b60cd9eeffb40e7621572eb275775ee43e67e763b79ab18a4a`  
		Last Modified: Thu, 17 Oct 2024 04:20:46 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b2f8e837025a04ecea9a5ed7eb84a58dc64c8e4285b73b4e75aad4ec86ee29`  
		Last Modified: Thu, 17 Oct 2024 04:20:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167fec70ae5fdee24d9a4cfacddbf101f9ebc065af143ec1fd87f373a2e1b4a7`  
		Last Modified: Fri, 25 Oct 2024 02:20:26 GMT  
		Size: 12.5 MB (12466981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5400bf3380f5e983d50c78898fe8873bc508246f6cc14eb2bbd9d751f22ad9`  
		Last Modified: Fri, 25 Oct 2024 02:20:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c7e94bb8c9fa7a04ddf0393b34b2cef319b23b5701f2a18477d0fc0ab16ee7`  
		Last Modified: Fri, 25 Oct 2024 02:20:25 GMT  
		Size: 11.3 MB (11346712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b99686052a151356b432e05cb3eded08911c15e26741d8555b32c84370feb3`  
		Last Modified: Fri, 25 Oct 2024 02:20:23 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b67238dcd35b39e97ac1a361d50293d9715b404d1b83be27bdfbedf0a5b3a2`  
		Last Modified: Fri, 25 Oct 2024 02:20:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae334c0087e76356477a39b41e0b35911d3d15a8d8d20a5fdb8c6a6d0e53521`  
		Last Modified: Fri, 25 Oct 2024 02:20:23 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce80c2aec1bf11a7c1abada72e9a571bd13a8001e1225721ac746ae52f72a33`  
		Last Modified: Fri, 25 Oct 2024 04:20:07 GMT  
		Size: 15.7 MB (15678014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b694fa1e5acf5a3f0c869df04b9260a0697a9966fadd26499bfca0d85b50adfc`  
		Last Modified: Fri, 25 Oct 2024 04:20:06 GMT  
		Size: 1.3 MB (1349366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46757a211c0745a3b9b10fad19bd0b5d7688d21b9efac017923d4df3f09b2876`  
		Last Modified: Fri, 25 Oct 2024 04:20:09 GMT  
		Size: 18.6 MB (18634525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6202c3627fa630baa801a7d933adf1b4676d155962869b9b7788d82debae16`  
		Last Modified: Fri, 25 Oct 2024 04:20:04 GMT  
		Size: 650.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42e629905291cdad893377524c9e8a5dec52781448fcc9114e37e40832f6ae4`  
		Last Modified: Fri, 25 Oct 2024 04:20:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af72225c46bda41fb8bceda26a6ab3227e5d7be8a9a5c469cd6d93fbc08692f6`  
		Last Modified: Fri, 25 Oct 2024 04:20:05 GMT  
		Size: 17.3 MB (17307827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca569c9063f812cd19c0ad098a2cebd5b0e86410e2104044863763001de0f92`  
		Last Modified: Fri, 25 Oct 2024 04:20:04 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143c28912382da42aa4819f75c613c11f88b0ba5c13bd548d44bb3a6309faf6a`  
		Last Modified: Fri, 25 Oct 2024 04:20:04 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:fb29e31d1e28c7ba32f5093d235aa2a992a8e069d309b9aa0c9d9239457ad893
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185346512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d78c03a94485978719ba7d53d966157ae74cae6026f41a67334ad9a7161a6d8`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Thu, 17 Oct 2024 04:00:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 04:00:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 04:00:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 04:00:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 04:00:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 04:00:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 04:00:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 04:00:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 05:06:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 02:01:33 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 02:01:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 02:01:33 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 02:01:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 02:01:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:04:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 02:04:14 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:04:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 02:04:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 02:04:14 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 02:04:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:04:15 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 02:04:15 GMT
EXPOSE 80
# Fri, 25 Oct 2024 02:04:15 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 03:58:09 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 25 Oct 2024 03:58:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 03:58:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Oct 2024 04:00:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 04:00:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 25 Oct 2024 04:00:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 04:00:48 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 25 Oct 2024 04:00:48 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 04:00:49 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 25 Oct 2024 04:00:49 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 25 Oct 2024 04:00:49 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Fri, 25 Oct 2024 04:00:49 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Fri, 25 Oct 2024 04:00:54 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 25 Oct 2024 04:00:55 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 25 Oct 2024 04:00:55 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 25 Oct 2024 04:00:55 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 25 Oct 2024 04:00:55 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:7279221aca8b55f43e6443be212b1657f9c1eb0166b21a5cff7c0dedb83c4987`  
		Last Modified: Thu, 17 Oct 2024 06:02:17 GMT  
		Size: 18.0 MB (18033763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7e67eec042806807953e626da02d18115bfb78f0edd01c3998bc24c88c81d4`  
		Last Modified: Thu, 17 Oct 2024 06:02:13 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cdc9341b31526e89809c4f7c7bc428ebf26dd65f69c5f3e71903660f744e1`  
		Last Modified: Thu, 17 Oct 2024 06:02:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156cb57f7e0188e8065c9aada104e3fecce57c4fe89a155093ca83baef4a83a8`  
		Last Modified: Fri, 25 Oct 2024 02:41:19 GMT  
		Size: 12.5 MB (12465087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99b7ef1aefe84eab8ad1aa4f791ca1acfaae6479247a0c27db1bddcd17d5f9`  
		Last Modified: Fri, 25 Oct 2024 02:41:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8495d34acc4489f6409ea7df2e653dcd2558ca0f29906f5ebdad173b0021ebff`  
		Last Modified: Fri, 25 Oct 2024 02:41:19 GMT  
		Size: 9.8 MB (9809456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fb8aab20227022e46b40837a39d7fb320997806b7179a58c1d82ac0797d88e`  
		Last Modified: Fri, 25 Oct 2024 02:41:16 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c36d9bf7260378f16244a96526698e0852e6e28c9b3d84c2fabf34f4284ba3`  
		Last Modified: Fri, 25 Oct 2024 02:41:16 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89e7b6ed64cd9522ffe530bf75841b9ea7544e9e26fce969a7873f1114c911`  
		Last Modified: Fri, 25 Oct 2024 02:41:16 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c092b4456f045a406aa0eb0e70723cfcc5b01eb8ee911c7443765c3c12cd5`  
		Last Modified: Fri, 25 Oct 2024 04:07:22 GMT  
		Size: 15.6 MB (15637199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d92bb3691411edfa56222418f7f07dc997f913acc38352c2eb8a3fb55e5187`  
		Last Modified: Fri, 25 Oct 2024 04:07:21 GMT  
		Size: 1.3 MB (1315713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200ced8eb63cb60ab207f65dd846b3bc583e3821d77e924890999c40eee9502a`  
		Last Modified: Fri, 25 Oct 2024 04:07:23 GMT  
		Size: 15.2 MB (15181043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8775f27135d2e7ec26efc49aa66326d1010f576c29c73302ddd925eda97bff1f`  
		Last Modified: Fri, 25 Oct 2024 04:07:19 GMT  
		Size: 651.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f109bb239fe4d7936fcc1a26a63f84eddd00723c31b6999a8c39665c1193c0`  
		Last Modified: Fri, 25 Oct 2024 04:07:19 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb42d866c9f9d853f8b1592b56c4bc750fd2261089e762dfdeba421d7f2e00f`  
		Last Modified: Fri, 25 Oct 2024 04:07:20 GMT  
		Size: 17.0 MB (16976172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e974eb960fa8360a7dddf7ac20293f750646d478c9ef6672871f228697ab78`  
		Last Modified: Fri, 25 Oct 2024 04:07:19 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9331de24e7b645d6c960bb9bd3aaeea34a35de73aee2917daab7409a553fc2e0`  
		Last Modified: Fri, 25 Oct 2024 04:07:19 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:5dcc2ea3b0340c1c25cf0dd8bdfb3b8e56c29b406b570caf7f82a2a30a75e36a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210808594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe18a458c897d6b9d442870786a48de4b64b0d692bbb248d379187e63e3ddafc`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Thu, 17 Oct 2024 01:51:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:51:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:51:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:51:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:51:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:51:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:51:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:13:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:37:19 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:37:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:37:19 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:37:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:40:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:40:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:40:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:40:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:40:17 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:40:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:40:17 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:40:17 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:40:18 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 02:40:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 25 Oct 2024 02:40:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 02:40:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Oct 2024 02:43:38 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 02:43:38 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 25 Oct 2024 02:43:38 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 25 Oct 2024 02:43:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 25 Oct 2024 02:43:39 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 02:43:39 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 25 Oct 2024 02:43:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 25 Oct 2024 02:43:39 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Fri, 25 Oct 2024 02:43:40 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Fri, 25 Oct 2024 02:43:44 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 25 Oct 2024 02:43:44 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 25 Oct 2024 02:43:44 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 25 Oct 2024 02:43:44 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 25 Oct 2024 02:43:44 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:74b980c2cf5f1d5985e5fd448ff6d061569c78dab491fdd6cf426d17ed80f5ed`  
		Last Modified: Thu, 17 Oct 2024 04:18:56 GMT  
		Size: 19.2 MB (19196724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8358973d1388c71d67de1b48dfb30463a5b98d0cb1ee434e6e4ed428cd185551`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3c5eb242c4d60a34a586a26ff5f3a53147c64f2f028014b29c6a95cc21d5d9`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e29dcdd0b9473053b1b65189bbd273d018853f9669cd15e804481996bb169c`  
		Last Modified: Fri, 25 Oct 2024 02:23:13 GMT  
		Size: 12.5 MB (12466068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4628e624f3e457e265baaae0955e3453639074a3544ab13b39577262c99b402c`  
		Last Modified: Fri, 25 Oct 2024 02:23:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b124cbeda1e07c8ac121389936c6f0d98d97806c39b7f9b06a7a130c49cc7`  
		Last Modified: Fri, 25 Oct 2024 02:23:13 GMT  
		Size: 11.4 MB (11432318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b772ec77807716af4c26590eca98190969134b4c49dde0876b24dd715b76b`  
		Last Modified: Fri, 25 Oct 2024 02:23:10 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa16866d98a3b72db46ae27cb72e4f55cd2ccc3fddfd05bafeba38a9a39e721`  
		Last Modified: Fri, 25 Oct 2024 02:23:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119fc4c07daf647c4e230d9e9db326ec2e3c14ab94bdf4f43ef21597e4efa39d`  
		Last Modified: Fri, 25 Oct 2024 02:23:11 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b415b511711703c4f7fec7fadbf759557f02a1ac3007af96e3d9c99c217122`  
		Last Modified: Fri, 25 Oct 2024 02:51:06 GMT  
		Size: 15.4 MB (15439666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba1fbe035f269698adb72c69a52da0a2cac49b96f39d426354e56d26ee78c87`  
		Last Modified: Fri, 25 Oct 2024 02:51:05 GMT  
		Size: 1.3 MB (1280639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de28af3d5d38ef1f4f0b69aa9273bf14082d3baec74036011449efd15a551997`  
		Last Modified: Fri, 25 Oct 2024 02:51:07 GMT  
		Size: 16.9 MB (16867065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9e8e030b9307c5f9be6bc793679282e8f7d98913b810156c75ee00e72a5477`  
		Last Modified: Fri, 25 Oct 2024 02:51:03 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3384424c5dfed3207a0e19005d634f486256f65efc82227f77cc751b7e385e1d`  
		Last Modified: Fri, 25 Oct 2024 02:51:03 GMT  
		Size: 535.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b87af780e8f36c9bf122a4419fb31b0591bc1c8c0d9b1eba366d728ce1acee`  
		Last Modified: Fri, 25 Oct 2024 02:51:04 GMT  
		Size: 17.1 MB (17100588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1c1c5c67b43a06f879b83922399001b253373f7fc2b999d2b6b3b3db4b3d89`  
		Last Modified: Fri, 25 Oct 2024 02:51:03 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594fe7e56ee7c1a8860380234caed9d51198b673dc453f1263af5ae3e6858b06`  
		Last Modified: Fri, 25 Oct 2024 02:51:03 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-apache` - linux; 386

```console
$ docker pull friendica@sha256:b239b2c5e4fe3bef5cbcbe1c6d98aa5bd34a85ef3c178e2fd5cb3a34ec0f68a6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (222030959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fc2184ac6e06c29f864f7cf89456cd589d3d461bab364f230ea1c2f8679e89`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Thu, 17 Oct 2024 01:49:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:49:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:49:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:49:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:49:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:49:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:49:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 04:15:36 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 05:02:22 GMT
ENV PHP_VERSION=8.2.24
# Thu, 17 Oct 2024 05:02:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 17 Oct 2024 05:02:23 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 17 Oct 2024 05:02:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 05:02:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:07:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 05:07:41 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:07:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 05:07:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 05:07:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 05:07:42 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:07:42 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 05:07:42 GMT
EXPOSE 80
# Thu, 17 Oct 2024 05:07:42 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 08:20:11 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ;
# Fri, 18 Oct 2024 18:38:29 GMT
ENV GOSU_VERSION=1.17
# Fri, 18 Oct 2024 18:38:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Oct 2024 18:41:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 18 Oct 2024 18:41:46 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Oct 2024 18:41:46 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Oct 2024 18:41:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 18 Oct 2024 18:41:47 GMT
VOLUME [/var/www/html]
# Fri, 18 Oct 2024 18:41:47 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 18 Oct 2024 18:41:48 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 18 Oct 2024 18:41:48 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Fri, 18 Oct 2024 18:41:48 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Fri, 18 Oct 2024 18:41:54 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;
# Fri, 18 Oct 2024 18:41:55 GMT
COPY multi:25ccf1ddc0e0285a533455c8e856fafdfe193ac37a4c3c06069260e518fe72d7 in / 
# Fri, 18 Oct 2024 18:41:55 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Fri, 18 Oct 2024 18:41:55 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 18 Oct 2024 18:41:55 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:b6ddf8ce51c109b7bb83cdc751f321539bb2a49e143c49641e4568e518e78a20`  
		Last Modified: Thu, 17 Oct 2024 06:09:35 GMT  
		Size: 19.8 MB (19767420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dcc3b4a41a7530a5d746216200906369af999165c38a5ff788ec50d3f4115e`  
		Last Modified: Thu, 17 Oct 2024 06:09:31 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ad97ea386e5b7a7e6e2df36ca746b373e1926f47c70d771b709f67e89ba637`  
		Last Modified: Thu, 17 Oct 2024 06:09:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de881ef785600e6ce140f34d4e049d4e37cb4658052596bf34ce2773d6576f00`  
		Last Modified: Thu, 17 Oct 2024 06:19:51 GMT  
		Size: 12.5 MB (12450470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e0278d825bb81c4371bfda68452e0b04167db2f07fe006a9d23f2d0a785456`  
		Last Modified: Thu, 17 Oct 2024 06:19:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa946abbf939be67a077659e8883964efa454bf5a8a8cd922fc1988ae4b1fdc`  
		Last Modified: Thu, 17 Oct 2024 06:19:51 GMT  
		Size: 11.6 MB (11587187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4273a51ae9305ee6f41ed4f9d752328811239a9387529f1012a6bf0ea009b2b2`  
		Last Modified: Thu, 17 Oct 2024 06:19:48 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc86713ef147ba1993b291b3da9382d20d266d3e4cb86d359f1bc2c280c9b8`  
		Last Modified: Thu, 17 Oct 2024 06:19:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1dddd1ebef03ed8e715b7704981b4c59faa95633ee25d0f8253771c564e159`  
		Last Modified: Thu, 17 Oct 2024 06:19:48 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de41fa47161b6185de6969308fa5f8f049f5f486b8bcf8cbb50b7bad71099dbd`  
		Last Modified: Thu, 17 Oct 2024 08:28:55 GMT  
		Size: 16.1 MB (16141848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ee77faa42a596f8adc8b0b48e3e699f0fc937c3812251af809363920d4094b`  
		Last Modified: Fri, 18 Oct 2024 18:49:37 GMT  
		Size: 1.3 MB (1324640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0931e9cd5eca9b4ad162ed71eaec080f28e7da70036782f125199401871dbb`  
		Last Modified: Fri, 18 Oct 2024 18:49:40 GMT  
		Size: 17.6 MB (17571875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fafb5b8a0690f3a31ed4bcb24d15e1e9a80bc3031370cb2abc02334c16b457f`  
		Last Modified: Fri, 18 Oct 2024 18:49:34 GMT  
		Size: 651.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b871d72b2dfd54d880a278610e1c6d6b8063cd26425e08fa69d287d7bac99112`  
		Last Modified: Fri, 18 Oct 2024 18:49:35 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c7bf6bf69b22e05b78173127b6558fe1e18ebb5ba8fc6cfe7f47abba096836`  
		Last Modified: Fri, 18 Oct 2024 18:49:36 GMT  
		Size: 18.0 MB (18041469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2ef05872ee10f8966e5a126e4b42ed2867cbcf6ed73fda55dc1cf8128fe49f`  
		Last Modified: Fri, 18 Oct 2024 18:49:34 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1bc38a12fc0d1f59672c55f3f5800e9b5f4346498323a222fcc5e151a16d61`  
		Last Modified: Fri, 18 Oct 2024 18:49:34 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
