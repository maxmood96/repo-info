## `friendica:latest`

```console
$ docker pull friendica@sha256:8fe46d9157555570318bf7bfa05e57da8f167b3d3ed0c32c63e93a5b644d696b
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

### `friendica:latest` - linux; amd64

```console
$ docker pull friendica@sha256:56386d48867e162868338ced9da9d595bcc1e2ffe0bc02c79cce12c64d366398
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213622712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3503df86ea99b01436511f8249e84723856a8f519c8c25096d7c70ff7ec6ddb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 16:19:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 16:19:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 16:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 16:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 16:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 16:26:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 16:26:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 16:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 16:26:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 16:26:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 16:26:18 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 16:26:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 16:26:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 16:26:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 16:26:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 18:56:17 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Sep 2021 21:17:47 GMT
ENV PHP_VERSION=7.3.31
# Thu, 23 Sep 2021 21:17:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Thu, 23 Sep 2021 21:17:48 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Thu, 23 Sep 2021 21:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Sep 2021 21:18:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:21:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Sep 2021 21:21:50 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:21:52 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Sep 2021 21:21:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Sep 2021 21:21:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Sep 2021 21:21:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Sep 2021 21:21:55 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:21:55 GMT
WORKDIR /var/www/html
# Thu, 23 Sep 2021 21:21:56 GMT
EXPOSE 80
# Thu, 23 Sep 2021 21:21:56 GMT
CMD ["apache2-foreground"]
# Fri, 24 Sep 2021 02:33:42 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Sep 2021 02:35:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 02:36:00 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Sep 2021 02:36:01 GMT
VOLUME [/var/www/html]
# Fri, 24 Sep 2021 02:36:02 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Sep 2021 02:42:25 GMT
ENV FRIENDICA_VERSION=2021.07
# Fri, 24 Sep 2021 02:42:26 GMT
ENV FRIENDICA_ADDONS=2021.07
# Fri, 24 Sep 2021 02:42:26 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Fri, 24 Sep 2021 02:42:26 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Fri, 24 Sep 2021 02:42:55 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 02:42:56 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Fri, 24 Sep 2021 02:42:56 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Fri, 24 Sep 2021 02:42:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Sep 2021 02:42:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27954d5e890ae7caed70e3e624ff12f502f4272d5d652f054a2f7d4ee773a5d`  
		Last Modified: Fri, 03 Sep 2021 19:22:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000081269276147e96e119ee9ad07bb95d0d7079dd717c5646a28e9bad2d7a5`  
		Last Modified: Fri, 03 Sep 2021 19:22:38 GMT  
		Size: 76.7 MB (76681283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0746dd2f27f766f6196abf9123ec789e0d28eebee2fd19a1eaea4f1b4daa548`  
		Last Modified: Fri, 03 Sep 2021 19:22:24 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27af26c5dec790ca0ee82e76994880d3879628c192cf7942a88e318a245da8f1`  
		Last Modified: Fri, 03 Sep 2021 19:23:01 GMT  
		Size: 18.7 MB (18679358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e310a2e3a5678d5d4729a1ccb6a528ac599bd76df111c1aed666b9a4ae4d65c`  
		Last Modified: Fri, 03 Sep 2021 19:22:57 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ebb7fb18a370099a9e6d12ffc057decc318152938a229a918ddb53b00b5b7`  
		Last Modified: Fri, 03 Sep 2021 19:22:57 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc60b69df8dad367194e9d891d24b0f812af2a4b9b9db1bcf1f990be8b9a619`  
		Last Modified: Thu, 23 Sep 2021 22:44:32 GMT  
		Size: 12.5 MB (12480581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa9a0322177df994a9bf05a911926e5fa0ba0b57d343e05487a1a357b4dbcb`  
		Last Modified: Thu, 23 Sep 2021 22:44:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b771c69f78ec7d169d7693cdbf0f889524ce3abf92fd3c89f79ecf6d0c768047`  
		Last Modified: Thu, 23 Sep 2021 22:44:31 GMT  
		Size: 14.6 MB (14596448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc4a3336a03ca02d6371b95592e7b12321abe3989435400900a298850f8c415`  
		Last Modified: Thu, 23 Sep 2021 22:44:29 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7078b268a64196b573ed7559fc3aae3c0e68672d9ea7f15250bae12fe8708199`  
		Last Modified: Thu, 23 Sep 2021 22:44:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e054950c3847e8be2606ae8d48184548b823a7827486b273d6dc906337f0feaa`  
		Last Modified: Thu, 23 Sep 2021 22:44:29 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fcaeda2e36dc240851823bb7ec12fa1dec70729bdd5b357b089d117781237d`  
		Last Modified: Thu, 23 Sep 2021 22:44:29 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc402c0fa0933c1c5734fd0ee2a90ee3a850b085859be1629ec3a21bd063bd12`  
		Last Modified: Fri, 24 Sep 2021 02:45:43 GMT  
		Size: 2.1 MB (2103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac85949551e651f5a24fc80a4fbdee53900cc4fdac05cbdf5a1302f78c791b4b`  
		Last Modified: Fri, 24 Sep 2021 02:45:46 GMT  
		Size: 15.4 MB (15381101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1099c8864465afeb8b9f3b92caa2eed46d0deec22dae68921d79055611c388`  
		Last Modified: Fri, 24 Sep 2021 02:45:42 GMT  
		Size: 571.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b39c583174e631565c37c0f5f97545d05c53619ebf7310ab86a8adbdcb2005c`  
		Last Modified: Fri, 24 Sep 2021 02:45:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e70d14b0e965043e07e37be8053b7cbdedb782646869c0dd230ebb1f0cd683`  
		Last Modified: Fri, 24 Sep 2021 02:46:35 GMT  
		Size: 46.5 MB (46544164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed263058d3da488e6075c3629af580b5dcdf600a07405116271b71776ac20c`  
		Last Modified: Fri, 24 Sep 2021 02:46:29 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f0a53b81f6225161101af41a8f55ea5517b15670a6cce08655d42c09fdb89a`  
		Last Modified: Fri, 24 Sep 2021 02:46:29 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; arm variant v5

```console
$ docker pull friendica@sha256:4c78ca536fbb2d9f15339060504044a3a3ecb7e26a00dce74c0b32d32057d746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190378234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79a2b391f089d26261ea1d1259e048e652d3f4f25319a11e9beba6351ff96e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:51:26 GMT
ADD file:350748a564076da397b991745cd42e0688d15c72b9fd5c81f8ea0bb8938a2b3d in / 
# Fri, 03 Sep 2021 00:51:27 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:35:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 04:35:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 04:36:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 04:36:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 04:42:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 04:43:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 04:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 04:43:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 04:43:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 04:43:27 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 04:43:28 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 04:43:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 04:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 04:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 07:00:09 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Sep 2021 20:38:03 GMT
ENV PHP_VERSION=7.3.31
# Thu, 23 Sep 2021 20:38:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Thu, 23 Sep 2021 20:38:04 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Thu, 23 Sep 2021 20:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Sep 2021 20:38:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Sep 2021 20:43:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Sep 2021 20:43:08 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 23 Sep 2021 20:43:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Sep 2021 20:43:11 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Sep 2021 20:43:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Sep 2021 20:43:12 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Sep 2021 20:43:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Sep 2021 20:43:13 GMT
WORKDIR /var/www/html
# Thu, 23 Sep 2021 20:43:14 GMT
EXPOSE 80
# Thu, 23 Sep 2021 20:43:14 GMT
CMD ["apache2-foreground"]
# Thu, 23 Sep 2021 23:20:02 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Sep 2021 23:26:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Sep 2021 23:26:16 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Sep 2021 23:26:17 GMT
VOLUME [/var/www/html]
# Thu, 23 Sep 2021 23:26:19 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 23 Sep 2021 23:34:44 GMT
ENV FRIENDICA_VERSION=2021.07
# Thu, 23 Sep 2021 23:34:45 GMT
ENV FRIENDICA_ADDONS=2021.07
# Thu, 23 Sep 2021 23:34:45 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Thu, 23 Sep 2021 23:34:46 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Thu, 23 Sep 2021 23:35:26 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Sep 2021 23:35:29 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Thu, 23 Sep 2021 23:35:30 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Thu, 23 Sep 2021 23:35:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Sep 2021 23:35:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b019db4b5197128481d48d92ecacd6bb356c027a3d08393f6567a6fa183ba769`  
		Last Modified: Fri, 03 Sep 2021 01:07:12 GMT  
		Size: 24.9 MB (24879114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e3ef1526ccd81a0211245e5c08c42d995c0bdadf6b43e83076be8000198c17`  
		Last Modified: Fri, 03 Sep 2021 07:32:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cf4249e3e6a35932cf563c7258add176e395ab51af10abbafda0cc6d36be12`  
		Last Modified: Fri, 03 Sep 2021 07:33:17 GMT  
		Size: 58.8 MB (58821081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e171e4530f4e73270f77d256e24e286beccec1501869658fce3ce1ec337625`  
		Last Modified: Fri, 03 Sep 2021 07:32:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0950838ce123ce03c3455b826c50969e5a08e672ebf510f51228b556880ff`  
		Last Modified: Fri, 03 Sep 2021 07:33:51 GMT  
		Size: 18.0 MB (18025928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3592b378cea011ab1d4e3549924146c0f8c1036dbcb944d02cae20a0ed1e4097`  
		Last Modified: Fri, 03 Sep 2021 07:33:40 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5b17c884ab918ef19fe9ffe49e219acf8f93247fe298b5a3eb563620e0f6f`  
		Last Modified: Fri, 03 Sep 2021 07:33:40 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5caa8e9e7e4bc3a44e7eaa5441f27c15d90474b046f0b2732f8733c448844a52`  
		Last Modified: Thu, 23 Sep 2021 21:19:11 GMT  
		Size: 12.5 MB (12478703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3389d8849dd8a71e6880f9a08696df0b2a0f0ff42d08fc5da4581399843e9c74`  
		Last Modified: Thu, 23 Sep 2021 21:19:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53e4c8c135f2df620b17a1d4f1fa23913ba7470f69d9458b0423dab46fcaa51`  
		Last Modified: Thu, 23 Sep 2021 21:19:16 GMT  
		Size: 13.6 MB (13633380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4c7f508abde5fc3efae19d2b07f8cae55ae63040a646211ae2b5e89d9feb93`  
		Last Modified: Thu, 23 Sep 2021 21:19:05 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf640639ab1c2e11dbe1b2d4dfebe75f2b4b64ae7fd1596e672e9dd5eb26b704`  
		Last Modified: Thu, 23 Sep 2021 21:19:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ae094b4f05c83884f660ec417223325037c7fa5bd406fa1c64289a633c94b6`  
		Last Modified: Thu, 23 Sep 2021 21:19:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00181d6f9c2ce24838095a0075d266a183cb0c8cd11fe12ca11fdbcd49a2be8f`  
		Last Modified: Thu, 23 Sep 2021 21:19:05 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35d37f848448ecfa714c7be32d7b76af2dac7550d541888556842770ce0aeba`  
		Last Modified: Thu, 23 Sep 2021 23:40:29 GMT  
		Size: 2.0 MB (1983589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce910899c47b650814e9c9b6384ccb7e32f57972f7f7c93b542f1292f9ffce7`  
		Last Modified: Thu, 23 Sep 2021 23:40:37 GMT  
		Size: 14.0 MB (14003623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d9441144a92f4aea7351abb55a88ced56aa6470eb19eeae41d2796cd328d86`  
		Last Modified: Thu, 23 Sep 2021 23:40:27 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f35c5ad5604369fbbdf4bc41d82313b1c8129d50f593b930ec276cc7a97900`  
		Last Modified: Thu, 23 Sep 2021 23:40:27 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7d24bdce2ad187a093ffe5255aa56640059df064d6759dfbcf223bab898818`  
		Last Modified: Thu, 23 Sep 2021 23:42:22 GMT  
		Size: 46.5 MB (46542319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ad0720c84483fe74e4ccc2bfe4279c9f47c91899f7be37a5286e609fabc4d9`  
		Last Modified: Thu, 23 Sep 2021 23:41:52 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb182f884b7ff3b58c363b01792b6280b5fc917385ac3d85f4d8811709790d`  
		Last Modified: Thu, 23 Sep 2021 23:41:52 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; arm variant v7

```console
$ docker pull friendica@sha256:da5d35e93b374b4ebbbb911ff0695dc7aba321892bf505415cfc52554c75cce5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c78e2bf4549c27068ea5daa9150c43ca992b453c58e6192167292beceac4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 13:41:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 13:41:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 13:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:41:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 13:41:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 13:47:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 13:47:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 13:47:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 13:47:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 13:47:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 13:47:47 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 13:47:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 13:47:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 13:47:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 13:47:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 15:53:20 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 24 Sep 2021 00:41:09 GMT
ENV PHP_VERSION=7.3.31
# Fri, 24 Sep 2021 00:41:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Fri, 24 Sep 2021 00:41:10 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Fri, 24 Sep 2021 00:41:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Sep 2021 00:41:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Sep 2021 00:45:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Sep 2021 00:45:57 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 24 Sep 2021 00:45:59 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Sep 2021 00:46:01 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Sep 2021 00:46:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Sep 2021 00:46:01 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Sep 2021 00:46:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Sep 2021 00:46:02 GMT
WORKDIR /var/www/html
# Fri, 24 Sep 2021 00:46:03 GMT
EXPOSE 80
# Fri, 24 Sep 2021 00:46:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Sep 2021 05:41:26 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Sep 2021 05:47:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 05:47:12 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Sep 2021 05:47:12 GMT
VOLUME [/var/www/html]
# Fri, 24 Sep 2021 05:47:14 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Sep 2021 06:00:51 GMT
ENV FRIENDICA_VERSION=2021.07
# Fri, 24 Sep 2021 06:00:52 GMT
ENV FRIENDICA_ADDONS=2021.07
# Fri, 24 Sep 2021 06:00:52 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Fri, 24 Sep 2021 06:00:53 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Fri, 24 Sep 2021 06:01:38 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 06:01:40 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Fri, 24 Sep 2021 06:01:41 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Fri, 24 Sep 2021 06:01:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Sep 2021 06:01:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebace6e13da3851cefbbb414e4eed59821719cd726a614087fb7a5fac39289cb`  
		Last Modified: Fri, 03 Sep 2021 16:33:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59984e91461b6b555059a2a0e43939a8229f2d37a02b5c7c46437c2954494fbc`  
		Last Modified: Fri, 03 Sep 2021 16:33:36 GMT  
		Size: 59.5 MB (59516088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5b239a24afb45b0d1e4e4011727fec03f4d129e3abacd507f69ecd59f5bee2`  
		Last Modified: Fri, 03 Sep 2021 16:32:59 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4ca9d80b02f33d1ba33bbddea85216dbf6b5aae8b84b9f6eaa1da143604a9f`  
		Last Modified: Fri, 03 Sep 2021 16:34:09 GMT  
		Size: 17.5 MB (17481672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a400f8b1aa5811bd284dd0ea97ee6fa4eaf536614eeda8a1ca98405d6e13d5`  
		Last Modified: Fri, 03 Sep 2021 16:33:59 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b623733881dd71cee8c2f1016a36f06e6d38344a3cb0097ca985997893fba92`  
		Last Modified: Fri, 03 Sep 2021 16:33:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca94c8e1bbd8295738f416fa30adcba0d5c573f1fc7bc73ec879e9959e1230a`  
		Last Modified: Fri, 24 Sep 2021 02:10:18 GMT  
		Size: 12.5 MB (12478724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c19e2c67bbcd4f6f2a6beb17714c1f44f5aa52a8667816a96a5464ee9009094`  
		Last Modified: Fri, 24 Sep 2021 02:10:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae85de607f359c526dd794f3e8f2bd4e0b8013a49415ba9c060379c1648206f`  
		Last Modified: Fri, 24 Sep 2021 02:10:21 GMT  
		Size: 12.9 MB (12935060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ebb7ed3dc5062038fa70642fee578694a1fee0ba790c140a4877db02c8196`  
		Last Modified: Fri, 24 Sep 2021 02:10:13 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3e89f4dc95f0c4fd6a91a6dbcfe0b240415a55eb07ac1a17856e6379073adc`  
		Last Modified: Fri, 24 Sep 2021 02:10:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cce0bd44c607504298054e4317c568aef39e9468e219f8566926d94744a6d07`  
		Last Modified: Fri, 24 Sep 2021 02:10:13 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4168bbdca15f8419cb6b1632bf94483824b598ab79bf21a79bbf022ead9b204`  
		Last Modified: Fri, 24 Sep 2021 02:10:13 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5cc3993cda87618f11c3590f7e9786852a854b06a7f58f355d8f338caf1527`  
		Last Modified: Fri, 24 Sep 2021 06:08:48 GMT  
		Size: 1.9 MB (1913620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f92e6cebc9feece3e3440c34469580b5899707a92d445ec262007a6186d8ac`  
		Last Modified: Fri, 24 Sep 2021 06:08:54 GMT  
		Size: 13.0 MB (12983836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555995411b6e549b9c993a78c4ccb5a5c006b88f8677b0e319f7c9ff38b180a6`  
		Last Modified: Fri, 24 Sep 2021 06:08:45 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118699e425e25382abde50d9c69280443b45142a08fd7d1f7fa134ebe9d8a6fb`  
		Last Modified: Fri, 24 Sep 2021 06:08:45 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b2131644643953473efa0bca2ff4e931cf884b368cb3d7f0de839d424fc37`  
		Last Modified: Fri, 24 Sep 2021 06:11:25 GMT  
		Size: 46.5 MB (46542346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f1453fa950f0e81f3201d387e58c933a2539b7fbb2e6b58ecc3668f3b3b220`  
		Last Modified: Fri, 24 Sep 2021 06:10:55 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d7d86d8a27c358e542e4cdfcb4ceca2a4bef8b7707fb46948b61637396f0cf`  
		Last Modified: Fri, 24 Sep 2021 06:10:55 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:74b20e87ed0992d8b461f127151092e4d6cee3b4d4a253a36dad30486f7a27d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203853373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553d9c1f2a3fc53b2acc305ce4f2b505337b328498a5c4056fe63beccf44ab76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:58 GMT
ADD file:4a1d7f2d989aee6bd83da076b6e9dd3da2da97cf5654bd37568e9baec30ac4b1 in / 
# Fri, 03 Sep 2021 00:40:58 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:28:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 08:28:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 08:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:29:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 08:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 08:34:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 08:34:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 08:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 08:34:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 08:34:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 08:34:39 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 08:34:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 08:34:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 08:34:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 08:34:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 10:06:09 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 24 Sep 2021 00:04:54 GMT
ENV PHP_VERSION=7.3.31
# Fri, 24 Sep 2021 00:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Fri, 24 Sep 2021 00:04:54 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Fri, 24 Sep 2021 00:05:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Sep 2021 00:05:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Sep 2021 00:07:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Sep 2021 00:07:36 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 24 Sep 2021 00:07:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Sep 2021 00:07:38 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Sep 2021 00:07:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Sep 2021 00:07:38 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Sep 2021 00:07:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Sep 2021 00:07:38 GMT
WORKDIR /var/www/html
# Fri, 24 Sep 2021 00:07:39 GMT
EXPOSE 80
# Fri, 24 Sep 2021 00:07:39 GMT
CMD ["apache2-foreground"]
# Fri, 24 Sep 2021 04:21:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Sep 2021 04:24:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 04:24:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Sep 2021 04:24:07 GMT
VOLUME [/var/www/html]
# Fri, 24 Sep 2021 04:24:07 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Sep 2021 04:30:19 GMT
ENV FRIENDICA_VERSION=2021.07
# Fri, 24 Sep 2021 04:30:20 GMT
ENV FRIENDICA_ADDONS=2021.07
# Fri, 24 Sep 2021 04:30:20 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Fri, 24 Sep 2021 04:30:20 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Fri, 24 Sep 2021 04:30:42 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 04:30:43 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Fri, 24 Sep 2021 04:30:43 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Fri, 24 Sep 2021 04:30:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Sep 2021 04:30:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d10c227306ce3db344a8399cbc02bbf0dcb36519318efbde3c6027c00be8b40e`  
		Last Modified: Fri, 03 Sep 2021 00:49:47 GMT  
		Size: 25.9 MB (25914860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2558f15f925a8832db0fd29887f5c1fd5ecff7fbf22d77acf98dd2d833d7009d`  
		Last Modified: Fri, 03 Sep 2021 10:28:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea4dd757a64db6e7626907bf8a2cfdb012c45d040f896cafb2299b1010a8128`  
		Last Modified: Fri, 03 Sep 2021 10:28:36 GMT  
		Size: 70.4 MB (70356210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723584334c0efef9fc1882fad3745a813fbb18494cf0a6fac32d9ca930440d9c`  
		Last Modified: Fri, 03 Sep 2021 10:28:25 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff90e8e947d02299c735bc563bdc53f104e8996f48d3df73139cd0be9f7a285`  
		Last Modified: Fri, 03 Sep 2021 10:29:01 GMT  
		Size: 18.6 MB (18580210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2a4cc86abc6a337ababec121a765bc0b3a54ff23b8a0a64fe0def5f4463697`  
		Last Modified: Fri, 03 Sep 2021 10:28:58 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5ff5bab3f20229b0a52c2147abb9c0d38e75e8f789d932761277da93380d47`  
		Last Modified: Fri, 03 Sep 2021 10:28:58 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2559a795f605da89dcf967e2cf785834d59846ff674e93652f2c00e9d8d1b`  
		Last Modified: Fri, 24 Sep 2021 01:12:13 GMT  
		Size: 12.5 MB (12479366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f471653d9d15150bb6fa0f41ce7f1c0a9c508b4bbf9f216104db285c9a3d1f`  
		Last Modified: Fri, 24 Sep 2021 01:12:12 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da44b66962367c9c680e38ec9dda1ad8bf33de24b338e8196ec05d0752ba42b5`  
		Last Modified: Fri, 24 Sep 2021 01:12:13 GMT  
		Size: 14.2 MB (14212787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8433073ba62c9ae5a46b4220fb3a9fa34de8cd4a23763b4572578caedacb2a3c`  
		Last Modified: Fri, 24 Sep 2021 01:12:10 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610ffb983773a38c840be2f29489aed97d6dc706adefacb663909b69a9bc7bd2`  
		Last Modified: Fri, 24 Sep 2021 01:12:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4657a52495a418e0aa80cc3754ffe140bc4d5eb5efaaf8e99e7c6d8889c0ac6`  
		Last Modified: Fri, 24 Sep 2021 01:12:10 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264f36ddf6f5ee47a32f0d1f55e2e7329d55f5d3141ef6af8e4eb400dc2a8b9d`  
		Last Modified: Fri, 24 Sep 2021 01:12:09 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725aab6f342965e757f9c7134870a168d218c2d5c8d880aa84de7c11190355e1`  
		Last Modified: Fri, 24 Sep 2021 04:34:10 GMT  
		Size: 2.0 MB (2005625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36a956187132578024bf8456286ee58dc1f632059613c26cd61ae052f816bb`  
		Last Modified: Fri, 24 Sep 2021 04:34:12 GMT  
		Size: 13.8 MB (13750869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c933b825748f295c489126974789c6c220a863042b647bf4457311354dfc8fb7`  
		Last Modified: Fri, 24 Sep 2021 04:34:07 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f2ae83ac896fa6b07c647f97eb9bd99dc903f0a475134c52751545942362d9`  
		Last Modified: Fri, 24 Sep 2021 04:34:07 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929ee163ce049dc21711819d744b7979af0d51826631d8098aceebb4129d40f4`  
		Last Modified: Fri, 24 Sep 2021 04:35:05 GMT  
		Size: 46.5 MB (46542974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17a2841bf5ed13d19d2882f7869d74321401c3a48f9bfe5173353f2e0b4dbde`  
		Last Modified: Fri, 24 Sep 2021 04:34:58 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31293ec5a6944dbe2901158b0056247cbf468221a836f0393ba0cdae4c0996c`  
		Last Modified: Fri, 24 Sep 2021 04:34:58 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; 386

```console
$ docker pull friendica@sha256:6f98f82033b9cf0a3cf737e04300b7df175461a16b5fa30967354715e761479f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218976948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2341edea1ae9483e6e623fa3e1b29d5b5c043f677c8c7250b5e0b4a8568ae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:24 GMT
ADD file:6bf4b6f4aa28306610ef10c68f422a7210ff2fbd5345cec07bc5f76d54a4c8bc in / 
# Fri, 03 Sep 2021 00:40:24 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:25:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 07:25:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 07:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 07:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 07:25:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 07:32:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 07:32:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 07:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 07:32:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 07:32:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 07:32:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 07:32:22 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 07:32:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 07:32:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 07:32:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 10:03:09 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Sep 2021 20:59:54 GMT
ENV PHP_VERSION=7.3.31
# Thu, 23 Sep 2021 20:59:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Thu, 23 Sep 2021 20:59:54 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Thu, 23 Sep 2021 21:00:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Sep 2021 21:00:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:04:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Sep 2021 21:04:59 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:05:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Sep 2021 21:05:01 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Sep 2021 21:05:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Sep 2021 21:05:01 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Sep 2021 21:05:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:05:02 GMT
WORKDIR /var/www/html
# Thu, 23 Sep 2021 21:05:02 GMT
EXPOSE 80
# Thu, 23 Sep 2021 21:05:02 GMT
CMD ["apache2-foreground"]
# Fri, 24 Sep 2021 02:45:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Sep 2021 02:47:28 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 02:47:29 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Sep 2021 02:47:29 GMT
VOLUME [/var/www/html]
# Fri, 24 Sep 2021 02:47:30 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Sep 2021 02:54:52 GMT
ENV FRIENDICA_VERSION=2021.07
# Fri, 24 Sep 2021 02:54:53 GMT
ENV FRIENDICA_ADDONS=2021.07
# Fri, 24 Sep 2021 02:54:53 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Fri, 24 Sep 2021 02:54:54 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Fri, 24 Sep 2021 02:55:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 02:55:22 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Fri, 24 Sep 2021 02:55:23 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Fri, 24 Sep 2021 02:55:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Sep 2021 02:55:23 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7e87f600658a0c0d3bd8b82b9c645b5ec2763492ec627c1c1c1183c2ad3c45d5`  
		Last Modified: Fri, 03 Sep 2021 00:49:06 GMT  
		Size: 27.8 MB (27797513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6820ad6efe74238625ac9c3fe8ba67ac555c38dc1aa3602e8186ae9e85039ff`  
		Last Modified: Fri, 03 Sep 2021 10:44:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfaceb2b2ff5b135b57ab2654776bca5d29ef5ab32cfcb1e68cd29be1946bfb`  
		Last Modified: Fri, 03 Sep 2021 10:44:48 GMT  
		Size: 81.2 MB (81229351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e0d70101bbd8d32dd6db99913c1dc3365d6808819b7c2d017a9e7100ea61c1`  
		Last Modified: Fri, 03 Sep 2021 10:44:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60169c7f4fd1319f016cede7e52f4f136c45e9f5782d7343ede03d3eb9f438d`  
		Last Modified: Fri, 03 Sep 2021 10:45:17 GMT  
		Size: 19.1 MB (19114857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cfe668d2d36a7d9fca5a67792ef98073a3a0bb0880b0fccd8184ed0e66dcc2`  
		Last Modified: Fri, 03 Sep 2021 10:45:12 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cfb1c7bdfd37aa768e417d8687ee4f93d8fd7657d82df35d5205c89c5c0c82`  
		Last Modified: Fri, 03 Sep 2021 10:45:11 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41cc44e023755d3914d69dc9adb722cbcc7110fe83c4437dc2db643d22b428`  
		Last Modified: Thu, 23 Sep 2021 22:45:29 GMT  
		Size: 12.5 MB (12479857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bdb32711b2e2076e9fc8bb093e65f7d4c69950c0e10e840643c0ae9b1154cf`  
		Last Modified: Thu, 23 Sep 2021 22:45:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddcab60641a0ad005b8a4497f6c92357213fa6c06ad2e9d1e03291b02907a93`  
		Last Modified: Thu, 23 Sep 2021 22:45:30 GMT  
		Size: 15.0 MB (14982824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d498085fa551a8e7908def6657d1b461153b61cab72d68866f9b8e9fdec148ee`  
		Last Modified: Thu, 23 Sep 2021 22:45:26 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da8a617e3e3e368deceed0a09dd04dd483232026314723750557cfdd494b66c`  
		Last Modified: Thu, 23 Sep 2021 22:45:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc0331b036d5154e2e41038d0985251b6cef5e0238e20e11ca9e1fb7172747e`  
		Last Modified: Thu, 23 Sep 2021 22:45:26 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1faf79b16fef3b859a035494b62cdb491d06138a0bb0184a268e3be7cbf8b68`  
		Last Modified: Thu, 23 Sep 2021 22:45:26 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18bf6839457f592fed6046bd998469860d3a2c3228a6f2bdb0bf5b0b5e084f9`  
		Last Modified: Fri, 24 Sep 2021 02:59:31 GMT  
		Size: 2.1 MB (2104341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3cede6f93ca26432557efaf5638003d6fd63b22360f2eef105ada675a083d8`  
		Last Modified: Fri, 24 Sep 2021 02:59:37 GMT  
		Size: 14.7 MB (14714340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e944d69f7a85ae3bc9590d13c925bbedb610fc60a271a94ac346f50cc73f3ab7`  
		Last Modified: Fri, 24 Sep 2021 02:59:27 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a9048cb4ff2f22711765cc264822cf05aba4d975d414029bbffb1d141a769c`  
		Last Modified: Fri, 24 Sep 2021 02:59:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a218fe2eec6f8178467272dc8b62f35f6dd57d9a64d6d6c5fffe37506099629`  
		Last Modified: Fri, 24 Sep 2021 03:00:41 GMT  
		Size: 46.5 MB (46543394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0baf213cc3f5c7f0a63addb41671a52bbfc1613065738b16dfcd1befd691baf`  
		Last Modified: Fri, 24 Sep 2021 03:00:30 GMT  
		Size: 2.6 KB (2625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04aff9d8d995c12429f358a39530274bc8e754f9cfb9cadbdfc2af05a46f42e`  
		Last Modified: Fri, 24 Sep 2021 03:00:30 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; mips64le

```console
$ docker pull friendica@sha256:0c521c86a7e45e0f908644831d85f5aea5ea6bfee3312570df1cf36b3a2d9c13
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211225153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684110bd0cac5562bdb9650ae5336379f70883dcffa0f4b1253db2960e7f2530`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:10:49 GMT
ADD file:219b2ce847fd4b227257f60cf40dee2eaf7688371fd76658752f6ccbac9c4353 in / 
# Fri, 03 Sep 2021 01:10:49 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:34:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 04:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 04:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:35:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 04:35:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 04:48:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 04:48:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 04:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 04:49:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 04:49:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 04:49:04 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 04:49:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 04:49:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 04:49:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 04:49:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 09:37:16 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 03 Sep 2021 09:37:16 GMT
ENV PHP_VERSION=7.3.30
# Fri, 03 Sep 2021 09:37:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.30.tar.xz.asc
# Fri, 03 Sep 2021 09:37:17 GMT
ENV PHP_SHA256=0ebfd656df0f3b1ea37ff2887f8f2d1a71cd160fb0292547c0ee0a99e58ffd1b
# Fri, 03 Sep 2021 09:37:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 03 Sep 2021 09:37:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 03 Sep 2021 09:45:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 03 Sep 2021 09:46:00 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 03 Sep 2021 09:46:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 03 Sep 2021 09:46:04 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 03 Sep 2021 09:46:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 03 Sep 2021 09:46:05 GMT
STOPSIGNAL SIGWINCH
# Fri, 03 Sep 2021 09:46:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 03 Sep 2021 09:46:06 GMT
WORKDIR /var/www/html
# Fri, 03 Sep 2021 09:46:06 GMT
EXPOSE 80
# Fri, 03 Sep 2021 09:46:06 GMT
CMD ["apache2-foreground"]
# Sat, 04 Sep 2021 08:47:13 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 04 Sep 2021 08:47:13 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 04 Sep 2021 08:47:17 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 04 Sep 2021 08:54:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Sep 2021 08:54:19 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 04 Sep 2021 08:54:19 GMT
VOLUME [/var/www/html]
# Sat, 04 Sep 2021 08:54:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sat, 04 Sep 2021 09:02:49 GMT
ENV FRIENDICA_VERSION=2021.07
# Sat, 04 Sep 2021 09:02:49 GMT
ENV FRIENDICA_ADDONS=2021.07
# Sat, 04 Sep 2021 09:03:14 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;
# Sat, 04 Sep 2021 09:03:17 GMT
COPY multi:3209742e8a927dbca8685b55decf65ccc1e1ba0dc4386b61a0e5c04e963d86c1 in / 
# Sat, 04 Sep 2021 09:03:18 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Sat, 04 Sep 2021 09:03:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:03:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c11f388d181c313e7657eea7b1ffa2d20856b4701922412adea724a19acdb79f`  
		Last Modified: Fri, 03 Sep 2021 01:19:51 GMT  
		Size: 25.8 MB (25812853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0506876e16a302eaee068c00bc512865ba690141dda3e4e5a79347cf2868a8aa`  
		Last Modified: Fri, 03 Sep 2021 10:20:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad35ab0b589a214622711850323a067085c0478a895bac3ae6d1f416c8dd864`  
		Last Modified: Fri, 03 Sep 2021 10:21:09 GMT  
		Size: 61.4 MB (61403671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5817c867747a042f8144eb56bc11f70ab4b9b9fa8dcd499a5983c0e7564075`  
		Last Modified: Fri, 03 Sep 2021 10:20:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bca85fe4b35fc5db27d9eb902018a05d3bf15940f0c436930fc5830f0cc2d9`  
		Last Modified: Fri, 03 Sep 2021 10:21:54 GMT  
		Size: 18.6 MB (18612053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2d70254e1313d91d0cb7c8638ea77640fa1ba1d1bb34a2aac9916e33467bc1`  
		Last Modified: Fri, 03 Sep 2021 10:21:42 GMT  
		Size: 443.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d25fd96e8786a99327f296a724e5c5e6db589426a9ffc57e54d69abfd42809`  
		Last Modified: Fri, 03 Sep 2021 10:21:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97339fdc2e7c3710b4752d6a1f21260becfd5fde9509f857c482aedb904b1f20`  
		Last Modified: Fri, 03 Sep 2021 10:37:50 GMT  
		Size: 12.5 MB (12477631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81072da18fd2a091387dd5bbe0861bf621ad12f6b95765046f5d474fb557c64d`  
		Last Modified: Fri, 03 Sep 2021 10:37:46 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d71ca0681a6b547a903b32ea2ebd2247d727b7ebae401115dc0aeb90f4fdcc`  
		Last Modified: Fri, 03 Sep 2021 10:37:55 GMT  
		Size: 13.8 MB (13789734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf54eff979e40c437dbff0f23e4a0f88a478067ad46f3658f241a5ce0eb364dc`  
		Last Modified: Fri, 03 Sep 2021 10:37:43 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c7910ca353917196c7d6ca26fb49a987d4dea460be3e96dbf260bf7c0b877a`  
		Last Modified: Fri, 03 Sep 2021 10:37:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e059929815974c789e66ab13e11e676c9ac0b2aa775f5aa64da291d1e3de631`  
		Last Modified: Fri, 03 Sep 2021 10:37:43 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b537212b02c7d762f3bd77be963b2ea8365eec1a5e0bf451927cd606d2b475f1`  
		Last Modified: Fri, 03 Sep 2021 10:37:43 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3beda82336e6e267a573baadeed210975fc5fb834b3e9ff15686b5fd9a4276`  
		Last Modified: Sat, 04 Sep 2021 09:05:07 GMT  
		Size: 19.2 MB (19163080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b1bff2b65d180b6e0f363a3f12c17b0ee44b450c40e22341407517c0727a53`  
		Last Modified: Sat, 04 Sep 2021 09:04:51 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49489558e00a1a3e1071270aedd0b199b02fb6f3c9e6ef0be01dcc2025da4e69`  
		Last Modified: Sat, 04 Sep 2021 09:05:05 GMT  
		Size: 13.8 MB (13817551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4421ccd58953183f779cc824d14b4eab3c47d7a0bf2c08a4a0fff58e02546c5`  
		Last Modified: Sat, 04 Sep 2021 09:04:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492a831f66315c8ce869092091ab1f30b2cf9b057be87267a39c765557792e46`  
		Last Modified: Sat, 04 Sep 2021 09:04:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a683c92c88fed6cb72e225861736de1e9a7e8ad5f9dfc84a1ae82992526fb519`  
		Last Modified: Sat, 04 Sep 2021 09:06:41 GMT  
		Size: 46.1 MB (46122331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30d2fd2a8baa185268b0ae395bb75c24dc316a47debfaf3cfd20f8f5ba7e1`  
		Last Modified: Sat, 04 Sep 2021 09:06:13 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda2b7faf3d8f80b75b11da41fe5cbeff79930072da7f702da7209932b0367e6`  
		Last Modified: Sat, 04 Sep 2021 09:06:13 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; ppc64le

```console
$ docker pull friendica@sha256:4c3ca6b5b866d3497d737bd34d447a79effffb8eaa618d7f0e3cc2cd9acd13b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224979482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8745445a6755385ec7e571914fb2dc4b27fda6915760e7ef850f95c2e799a2a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 12:16:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 12:16:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 12:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 12:19:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 12:19:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 12:26:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 12:26:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 12:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 12:28:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 12:28:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 12:29:02 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 12:29:07 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 12:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 12:29:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 12:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 15:48:58 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 24 Sep 2021 03:31:14 GMT
ENV PHP_VERSION=7.3.31
# Fri, 24 Sep 2021 03:31:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Fri, 24 Sep 2021 03:31:25 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Fri, 24 Sep 2021 03:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Sep 2021 03:33:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Sep 2021 03:42:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Sep 2021 03:42:27 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 24 Sep 2021 03:42:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Sep 2021 03:43:08 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Sep 2021 03:43:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Sep 2021 03:43:33 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Sep 2021 03:43:36 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Sep 2021 03:43:43 GMT
WORKDIR /var/www/html
# Fri, 24 Sep 2021 03:43:50 GMT
EXPOSE 80
# Fri, 24 Sep 2021 03:43:55 GMT
CMD ["apache2-foreground"]
# Fri, 24 Sep 2021 08:10:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Sep 2021 08:31:11 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 08:31:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Sep 2021 08:31:28 GMT
VOLUME [/var/www/html]
# Fri, 24 Sep 2021 08:31:46 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Sep 2021 09:27:09 GMT
ENV FRIENDICA_VERSION=2021.07
# Fri, 24 Sep 2021 09:27:15 GMT
ENV FRIENDICA_ADDONS=2021.07
# Fri, 24 Sep 2021 09:27:19 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Fri, 24 Sep 2021 09:27:34 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Fri, 24 Sep 2021 09:31:02 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 09:31:07 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Fri, 24 Sep 2021 09:31:09 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Fri, 24 Sep 2021 09:31:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Sep 2021 09:31:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb76d147d0063b8960b8a00ba53c0afd0842b1ab19873b7738768495c713902f`  
		Last Modified: Fri, 03 Sep 2021 16:26:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523608b638ae84670283921a7d95b06bf0874f23a642abc20a2f09ac9e428975`  
		Last Modified: Fri, 03 Sep 2021 16:27:44 GMT  
		Size: 82.3 MB (82291876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9657d90e8c8e11fea217e87ea84eb7dbec014a7fb8093040ba57e5c836b3b76d`  
		Last Modified: Fri, 03 Sep 2021 16:26:49 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f17e0a11bc875883b172644a807be90c213e520799582a54b8969fc5d09469d`  
		Last Modified: Fri, 03 Sep 2021 16:28:19 GMT  
		Size: 19.8 MB (19818452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dba5fbb9faf7ad19e6abbb763940260029e745563e58055bc35d77840d3cc9d`  
		Last Modified: Fri, 03 Sep 2021 16:28:08 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4262c89764bdb3458819fc15e0cf1c5738ba8903910e2c3dd3038fda8b49e196`  
		Last Modified: Fri, 03 Sep 2021 16:28:06 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572502eb879436be0f20de7c625090cbcee8af39add8531c7842ae51ae36a0b5`  
		Last Modified: Fri, 24 Sep 2021 05:20:08 GMT  
		Size: 12.5 MB (12480622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df139951316540b65b60a1e98265c32de5f697b09d9ea84d65fda4c3f4b79bfb`  
		Last Modified: Fri, 24 Sep 2021 05:20:07 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c71d85507ec79b63298ab3923e8379858976fa8198995ea13fceec45e3d6a15`  
		Last Modified: Fri, 24 Sep 2021 05:20:08 GMT  
		Size: 15.6 MB (15572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd6e9121d786d4764f2d5093486c00a958c4860841a6fbb43735871e44657dd`  
		Last Modified: Fri, 24 Sep 2021 05:20:05 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffd3948490e2e146b5c369e1661f709a6062d16669c3b13940159e1754ead6`  
		Last Modified: Fri, 24 Sep 2021 05:20:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81271fc58138f126a72223e92cff6165064b995042ec61d796ecde76559fd1c`  
		Last Modified: Fri, 24 Sep 2021 05:20:04 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7e5b522521de204347a5c5feb5b3b4e0ab46acc22a2dc329f14b3ece135f8`  
		Last Modified: Fri, 24 Sep 2021 05:20:04 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb34888f09748a5839a8f2e1d0f5dfbe2530f859435a163e2ddf2dcc700c1bd`  
		Last Modified: Fri, 24 Sep 2021 09:49:32 GMT  
		Size: 2.1 MB (2135212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5651d93516b01e6b70ed61eb93845878f1ee1b612a272b61292231a1b2a12`  
		Last Modified: Fri, 24 Sep 2021 09:49:36 GMT  
		Size: 15.6 MB (15569568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ec80632cc42362e1d96eca2f6107fc6edfc7391b636ab3d14b6c33059a1c81`  
		Last Modified: Fri, 24 Sep 2021 09:49:28 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747b33f211785ed141c03941f5fdf4b8243e461f751d71f1db1c857ec37da5ce`  
		Last Modified: Fri, 24 Sep 2021 09:49:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97305fdb5478ca925644686d279ca34b27c52e4c94d047851165b30a17a22f7`  
		Last Modified: Fri, 24 Sep 2021 09:50:35 GMT  
		Size: 46.5 MB (46547193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e04c8d342c551e4f9645cbf55a497c92f9d5eaa637c0755776b619a13fa4852`  
		Last Modified: Fri, 24 Sep 2021 09:50:27 GMT  
		Size: 2.6 KB (2626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198bb050e1f9565d6b29ec1314ea8426b2769fee011b90ed945c2bd47c1d2bae`  
		Last Modified: Fri, 24 Sep 2021 09:50:27 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:latest` - linux; s390x

```console
$ docker pull friendica@sha256:4ffc8650226bde87e33bf2c0205dfc2acc87b2a889e0bef0072ca74a9b6ebf41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197719615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458f3a4b80523f2a3464b60b568756fa3b40bf5a37485e5c25ce67630ad72a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:44:44 GMT
ADD file:b8ec865f1745d5948e8a6d734df344bcc6aa076754554241a2d12c6d738199b0 in / 
# Fri, 03 Sep 2021 00:44:47 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 09:17:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 03 Sep 2021 09:17:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 03 Sep 2021 09:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 09:18:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 03 Sep 2021 09:18:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 03 Sep 2021 09:24:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 03 Sep 2021 09:24:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 03 Sep 2021 09:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 03 Sep 2021 09:25:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 03 Sep 2021 09:25:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 03 Sep 2021 09:25:03 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 03 Sep 2021 09:25:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 03 Sep 2021 09:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 09:25:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 03 Sep 2021 09:25:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 03 Sep 2021 12:06:55 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Sep 2021 21:26:00 GMT
ENV PHP_VERSION=7.3.31
# Thu, 23 Sep 2021 21:26:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Thu, 23 Sep 2021 21:26:00 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Thu, 23 Sep 2021 21:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Sep 2021 21:26:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:28:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Sep 2021 21:28:26 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:28:26 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Sep 2021 21:28:27 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Sep 2021 21:28:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Sep 2021 21:28:27 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Sep 2021 21:28:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Sep 2021 21:28:27 GMT
WORKDIR /var/www/html
# Thu, 23 Sep 2021 21:28:27 GMT
EXPOSE 80
# Thu, 23 Sep 2021 21:28:27 GMT
CMD ["apache2-foreground"]
# Fri, 24 Sep 2021 00:26:15 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini         gosu     ;     gosu nobody true;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Sep 2021 00:28:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.4;     pecl install imagick-3.5.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 00:28:22 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 24 Sep 2021 00:28:22 GMT
VOLUME [/var/www/html]
# Fri, 24 Sep 2021 00:28:22 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 24 Sep 2021 00:31:37 GMT
ENV FRIENDICA_VERSION=2021.07
# Fri, 24 Sep 2021 00:31:37 GMT
ENV FRIENDICA_ADDONS=2021.07
# Fri, 24 Sep 2021 00:31:37 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d57ebb33ff733f0ad023ad63e8992d8f61cec06363b951d00f1452760eeeda12
# Fri, 24 Sep 2021 00:31:38 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=9752046c5af1003338a668683b24476cfb3f8dfeaef466703492a0883581c790
# Fri, 24 Sep 2021 00:31:54 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Sep 2021 00:31:58 GMT
COPY multi:cbfaa339ea6c4ed31e965c80bb4049c4a72d30f14b76e709e7cc4820ce4ec776 in / 
# Fri, 24 Sep 2021 00:31:58 GMT
COPY multi:33c6df8ca48b360ac89b7ca8e8b370fe30a626687aacfad3b3c3d5c1924a5777 in /usr/src/friendica/config/ 
# Fri, 24 Sep 2021 00:31:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Sep 2021 00:31:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:65229990cda1bd6e6b517c67238f245d103190c9a170014e2c22a40b96dd47ec`  
		Last Modified: Fri, 03 Sep 2021 00:53:39 GMT  
		Size: 25.8 MB (25760757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1604351f5ae83997ad110d5cec6404f6899f8a22264e6313ece3599b6aa4b433`  
		Last Modified: Fri, 03 Sep 2021 12:44:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e819c474c5bd6f1b3fd0b0e163f0c9a0c0efcd0a9a4771b2648bc359cc15c3`  
		Last Modified: Fri, 03 Sep 2021 12:44:13 GMT  
		Size: 64.7 MB (64712644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348f317fa67c2a7926cfeab642b1fc1ce09e34800cbf20796b43f7b98f86bc8b`  
		Last Modified: Fri, 03 Sep 2021 12:44:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6efb8ac2af65c9a71312b790071bb156ec33687742b33290d24472d890e9943`  
		Last Modified: Fri, 03 Sep 2021 12:44:33 GMT  
		Size: 18.5 MB (18524826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0717523231340bc87822817e90190a1ab72a323f35e0266b62d0525139b32ae7`  
		Last Modified: Fri, 03 Sep 2021 12:44:29 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b92c87c1317a5a8c510a6225a9b0ee98eb3613e5ec00c9c8b19248036085c9b`  
		Last Modified: Fri, 03 Sep 2021 12:44:30 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3c594c93091ec9a849b5cb39e2e780f2279aed6728790b465752769c592288`  
		Last Modified: Thu, 23 Sep 2021 22:11:00 GMT  
		Size: 12.5 MB (12479097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6363c4a3f429a05a8e7b3ce49c24cc98b271d9844eaea535dc92abb0cdaa26`  
		Last Modified: Thu, 23 Sep 2021 22:11:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6893cb3ccd9832e4a9d6c572e6450a3c2ff525fceaf5cc82aa5df64b1c1d47`  
		Last Modified: Thu, 23 Sep 2021 22:11:00 GMT  
		Size: 13.8 MB (13782056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f0be67b85a28e594fdcdbd5f91a6b6245438cf77febca3279d84a356994219`  
		Last Modified: Thu, 23 Sep 2021 22:10:58 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2498693ccc5be974b6dd937f96d12d382302d7fa0629cade6c4f1db0f019b56`  
		Last Modified: Thu, 23 Sep 2021 22:10:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3139e35799c07ea51ad24443005b8af6968dea6983bac9e2a41449671f23a7`  
		Last Modified: Thu, 23 Sep 2021 22:10:58 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49625db17b467945cb86226492fb6da5a9b97bd79f1dcd9bb4063a75025d73e`  
		Last Modified: Thu, 23 Sep 2021 22:10:59 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d17123c5064c1084ef2e317b70609a10720e017db33e020c38c3e1abf6649ff`  
		Last Modified: Fri, 24 Sep 2021 00:35:11 GMT  
		Size: 2.1 MB (2056661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448fb1d0f328994ddc0e18082536bdcd11aa3375452f917e630f204e86d414c4`  
		Last Modified: Fri, 24 Sep 2021 00:35:13 GMT  
		Size: 13.9 MB (13850556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19cb90e36d5f37f57dcfc4d59d9cf6aeaa924e19196344072f7cc6cb7142b6d`  
		Last Modified: Fri, 24 Sep 2021 00:35:10 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135860cb8dae1d4a14982aeb69b0ed08b417f12e07ca819506e2403b62bca9a8`  
		Last Modified: Fri, 24 Sep 2021 00:35:10 GMT  
		Size: 540.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07661fb55b9a75f246000bf4dbcb3582fc80bf288a65eb9f4e3b9bd01ba256fb`  
		Last Modified: Fri, 24 Sep 2021 00:35:39 GMT  
		Size: 46.5 MB (46542543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da8a442f7cbba9d53c49011dab619e13a7b8256faccf5d470c49503cbaa8148`  
		Last Modified: Fri, 24 Sep 2021 00:35:35 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fca128cb2236dd0e175450e967a3b90a8f2b3ac190d28c49ba2f422faef634`  
		Last Modified: Fri, 24 Sep 2021 00:35:34 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
