## `friendica:dev-apache`

```console
$ docker pull friendica@sha256:1d03916c46b8a832227ace9ae4749488feedb338caf107ddaf267d46922f8df6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `friendica:dev-apache` - linux; amd64

```console
$ docker pull friendica@sha256:a90e7809db58bd7db1a3ccb4462c8c6e6a4c483d0fb24ea20f50ce371de55dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216659844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d720158f4aa52618869a983ff706533c91f355f625e6d76b0f6579e6fc28cc7`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 17 Nov 2024 02:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_VERSION=8.2.27
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 17 Nov 2024 02:07:21 GMT
STOPSIGNAL SIGWINCH
# Sun, 17 Nov 2024 02:07:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
WORKDIR /var/www/html
# Sun, 17 Nov 2024 02:07:21 GMT
EXPOSE map[80/tcp:{}]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GOSU_VERSION=1.17
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
VOLUME [/var/www/html]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_VERSION=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_ADDONS=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ebccf552eb1278d43896a5ad2c404013ff4ee4203aa57c40d6564bb4e03256`  
		Last Modified: Tue, 24 Dec 2024 22:27:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf0d30b62f5af172fd22facaab38ae23d83958c32f5c2632de4bee6b981926`  
		Last Modified: Tue, 24 Dec 2024 22:27:20 GMT  
		Size: 91.4 MB (91448348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84b6b6b184cf75c456c5bf01bb13dd9d73bbbb1aba31d315ce3e78fcb192ffc`  
		Last Modified: Tue, 24 Dec 2024 22:27:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced2201721b90b9e39daa11020538b3b47be2df10e8c46ce37ea559bcb0916f`  
		Last Modified: Tue, 24 Dec 2024 22:27:19 GMT  
		Size: 19.1 MB (19064413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b270c399f4daf57c82773fe9283ba5a3f712f3bba1fedb531b758795486e6208`  
		Last Modified: Tue, 24 Dec 2024 22:27:19 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6450bf41e0fc5c18c4b7202eb962e370e448899a17984f3f36b5452a8df3dfd0`  
		Last Modified: Tue, 24 Dec 2024 22:27:19 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00948e7d57dcc5305cbef284af666c38b33fbcd4d5e2c7fdadfc32cf17d29cc`  
		Last Modified: Tue, 24 Dec 2024 22:27:20 GMT  
		Size: 12.3 MB (12275658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cc254639c7aeb5202b13d5eeeda6351678b024e528ffc0c884da90c1264a4b`  
		Last Modified: Tue, 24 Dec 2024 22:27:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd08eb49873ff3ec2c67ac67a73698727e9ae3e9889160716daff4845745cb`  
		Last Modified: Tue, 24 Dec 2024 22:27:20 GMT  
		Size: 11.4 MB (11352992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978472ec0a8e8e1bd88628c38ba488a9c53a4a3f6690042d2823c9f7f6672a1e`  
		Last Modified: Tue, 24 Dec 2024 22:27:21 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a5f4f6d5dc04d1a59d8f5b685fe60fe40ace5c16636ebed8cb1973d3c5b2e`  
		Last Modified: Tue, 24 Dec 2024 22:27:21 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569c18c0fcc41a74d729c34926e8eb3e2065b3663ec4bf9e86536bbcc3ae489f`  
		Last Modified: Tue, 24 Dec 2024 22:27:21 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f208f59b93694433454a667d30cf92075ac88963519c0f14783fd56ee2e53d1`  
		Last Modified: Tue, 24 Dec 2024 23:22:45 GMT  
		Size: 15.7 MB (15719256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63772e92b9c0746da408ef17781b402644b7d1507b3516289485b19caefbed2`  
		Last Modified: Tue, 24 Dec 2024 23:22:44 GMT  
		Size: 1.1 MB (1122804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1c33745c556fdbef7d62c60c0548f7a35f1ec5e4e87c5592eb5971af244280`  
		Last Modified: Tue, 24 Dec 2024 23:22:44 GMT  
		Size: 18.3 MB (18308533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a1cc39914dd7e7007ff970c3fc7cd02dd0111c548dc57e1c734a14c3fa6262`  
		Last Modified: Tue, 24 Dec 2024 23:22:44 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3c6a65c001d6dfcf307c786e170d69ba1c1b1a1f4149a9b833d6dcaa258d1`  
		Last Modified: Tue, 24 Dec 2024 23:22:45 GMT  
		Size: 532.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c541323a8049ade7ca478c3b97989acb560086e6bfc83db3136ee38994de77ba`  
		Last Modified: Tue, 24 Dec 2024 23:22:45 GMT  
		Size: 17.1 MB (17103814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b450d100d332cc4ea8659c9ffb86dcdf88a26b6d33760932855efe84f7e662`  
		Last Modified: Tue, 24 Dec 2024 23:22:45 GMT  
		Size: 3.8 KB (3820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003421c55aff922ae029f17876faa9c34d3b80f93ebf613e87af438cecaace4`  
		Last Modified: Tue, 24 Dec 2024 23:22:45 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:a474b7c25f5c40bf41d566c3bcdd087b431b0f336483e91f66a8c0d6377d3bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd2b06c253f51e4f70cbf3c08247ab9e4b017f9fdf0a387e4126e5a850793b`

```dockerfile
```

-	Layers:
	-	`sha256:dc969e56fa75c02a95b29c6f959a70be2ee3cee108ea2e0d0be2d1c4ac4e8845`  
		Last Modified: Tue, 24 Dec 2024 23:22:44 GMT  
		Size: 58.5 KB (58502 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:6528546e68091777613dfb34b613ac6a5b8b04223b39a90f886a7134ad612bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182999672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da092d92cd14a79a9b592e29503aaa808db5b1e548098b1482eb35f6e86f349d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 17 Nov 2024 02:07:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_VERSION=8.2.27
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 17 Nov 2024 02:07:21 GMT
STOPSIGNAL SIGWINCH
# Sun, 17 Nov 2024 02:07:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
WORKDIR /var/www/html
# Sun, 17 Nov 2024 02:07:21 GMT
EXPOSE map[80/tcp:{}]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GOSU_VERSION=1.17
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
VOLUME [/var/www/html]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_VERSION=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_ADDONS=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:79ae44024aa8e358b5fbaad284a41a7c359d47ad28af854839c0e44435b875ba`  
		Last Modified: Tue, 03 Dec 2024 01:28:54 GMT  
		Size: 25.5 MB (25533944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f4cd0ed182c41a7840e3bd6aeb9858708e8c6b99baae88a51faf80b4559a51`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682dddbc2d895e7263b87741543ce754592ab412d0d97e492925c117dfb408e3`  
		Last Modified: Tue, 03 Dec 2024 03:00:19 GMT  
		Size: 69.1 MB (69119217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f7c0f9947f1b2a09b6fb724d5e29aec91c63413c8b1ab8510d897d0b179b52`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7728885a127c27ece4b92b9fe5a46d8aee99959b4c6a8176c69da516af79e1`  
		Last Modified: Tue, 03 Dec 2024 03:03:47 GMT  
		Size: 17.8 MB (17816810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666592da9a8e3da05702b450abfd50251066b4280e0166696d843ed6dc062e7`  
		Last Modified: Tue, 03 Dec 2024 03:03:46 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb831e09aaec10c45d38ede42b26a3c3463bc2a9c5fc3e25f366b39db0b232ba`  
		Last Modified: Tue, 03 Dec 2024 03:03:46 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a58dff9677d19eca195cbbac444a4f19c37be01ac4181210e5196a541713be4`  
		Last Modified: Fri, 20 Dec 2024 23:51:00 GMT  
		Size: 12.3 MB (12274288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc1d69fde4fb57a9c784b00973a553240b37462cd31ee614ee3eef6e13c8fe6`  
		Last Modified: Fri, 20 Dec 2024 23:50:59 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db7d0a3822f0fa1eee8d736124bd1272edfa9bc6724956ab50ec6064f3a19e`  
		Last Modified: Fri, 20 Dec 2024 23:51:00 GMT  
		Size: 9.8 MB (9814427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606a8f7533347b75a3da0dcadeeaca7148595faa78e7266bda02086bdc805de3`  
		Last Modified: Fri, 20 Dec 2024 23:50:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa91d20faa305ff0ec4cb1dc9fa71bd9360a340e462be1c202b1c6f5ee567da`  
		Last Modified: Fri, 20 Dec 2024 23:51:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e3ba35996e7d7dd653b3704040a56a6f133dc1f9d32ea61f11529cb91380aa`  
		Last Modified: Fri, 20 Dec 2024 23:51:00 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd156b938be7b537b5ddb0a5709e3e8b0d65a1ee7c5b7da439faa5dbe8c71bb`  
		Last Modified: Sat, 21 Dec 2024 01:03:58 GMT  
		Size: 15.7 MB (15675159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7010c637b3f08eedf82d92df88443ea7a98a8452417f83e57c63f507ab099240`  
		Last Modified: Sat, 21 Dec 2024 01:03:58 GMT  
		Size: 1.1 MB (1089292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c70f89c8fa8b77dbc519369ad0e916e6349cbe26845bd04fa55a09564ba5894`  
		Last Modified: Sat, 21 Dec 2024 01:03:58 GMT  
		Size: 14.9 MB (14897104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec033cb71193f01956c25013f6b73782a3641cbc64aab339365ebf6b57a39d`  
		Last Modified: Sat, 21 Dec 2024 01:03:57 GMT  
		Size: 653.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b562ecca19fdd7b473d04a6b448579b27ced37e1bccf7f1b9e58ba5f8b96ed`  
		Last Modified: Sat, 21 Dec 2024 01:03:58 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546b06bed7127849d758aacf0d50650525f11386fb448afcbbd85d3f11012048`  
		Last Modified: Sat, 21 Dec 2024 01:11:32 GMT  
		Size: 16.8 MB (16768012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39cd31b73051f8aeee2f3e777c124da6bf8456786ad3978391d83367d6cc29b`  
		Last Modified: Sat, 21 Dec 2024 01:11:31 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f1f79c669785a8b5857e81716558a3d2c96f8cbd0497e0c4b0788dc89341ea`  
		Last Modified: Sat, 21 Dec 2024 01:11:31 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:091693d65d6d541855fc6d08e8a07d26e933d487a64d9c68d44b4297c8283390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 KB (58634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47ed595a80332141a4e4e5169c0e1357b6fc30f969b34027cc1daed18d7ce44`

```dockerfile
```

-	Layers:
	-	`sha256:fa18dccd2941211bee8fb8cec40ead094acbcd62a987426b0bc18f3632df2e56`  
		Last Modified: Sat, 21 Dec 2024 01:11:30 GMT  
		Size: 58.6 KB (58634 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:64b14c5a51174e1a87aec852cfbca00f0e3988500cb6c99bf7535454edd2db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208150350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a699bb70a52a70bfc3577457bb41ac38582ef78091a7690df43f86a4556f8be1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 17 Nov 2024 02:07:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_VERSION=8.2.27
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 17 Nov 2024 02:07:21 GMT
STOPSIGNAL SIGWINCH
# Sun, 17 Nov 2024 02:07:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
WORKDIR /var/www/html
# Sun, 17 Nov 2024 02:07:21 GMT
EXPOSE map[80/tcp:{}]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GOSU_VERSION=1.17
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
VOLUME [/var/www/html]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_VERSION=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_ADDONS=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa51b96f45aeeeac0da5ce8bef54768006d2f3f15d75cc62bf2f673af4c4ee`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf1193220d0cc95806c6408988e7d5348f9ad83ddfb796cd2261f04ce83160a`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 86.7 MB (86734618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80085106d7b6b1e2208214a2555ef1f1d0e5a1cfb68b48454784f2843f1cdc7e`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ea0f9b7f6efbb33f5a749a1cb2cf1751ed31abdb2e294e06286e97eb7fbf1d`  
		Last Modified: Tue, 03 Dec 2024 03:18:03 GMT  
		Size: 19.0 MB (18981083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c696520c2f7aab4ef21c2d1df0a9712fca366f3f0806394db0b7584cea48`  
		Last Modified: Tue, 03 Dec 2024 03:18:02 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d048c750cb6a734595987007d389c6225574a522e46cdede56c149277ef00b58`  
		Last Modified: Tue, 03 Dec 2024 03:18:02 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9005e51090df3e571c0e58708251d94561f8fa9730af0d83534fe503c48aa16`  
		Last Modified: Fri, 20 Dec 2024 23:43:43 GMT  
		Size: 12.3 MB (12274999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab49f509222ee8f1e6c19140d9b1d0a07e35470d4079adcc8320f59b28d1dcb`  
		Last Modified: Fri, 20 Dec 2024 23:43:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd2c532fe02952c78f41409086ff181ed32a0f00d69027e0f5c341572a8644`  
		Last Modified: Fri, 20 Dec 2024 23:43:43 GMT  
		Size: 11.4 MB (11441427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c71a6a56be24aaca0a69493700da91dd226712ea7e1d49f620f10643425caf`  
		Last Modified: Fri, 20 Dec 2024 23:43:43 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59935bedd6f02b7b1a44851705f5e6a5e4a7bc26aa06b1c9f1444416e273f1`  
		Last Modified: Fri, 20 Dec 2024 23:43:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed4c47c5bbf2898e160691e269319631e8195d9f242e8cf64299be98b2aaeb1`  
		Last Modified: Fri, 20 Dec 2024 23:43:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acc3540dcb9f14f8e8e5dcefec743a66b3d11c8687cd596d40e6bb98a536687`  
		Last Modified: Sat, 21 Dec 2024 02:31:23 GMT  
		Size: 15.5 MB (15474355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c1ab98eff54b5f524c17a1dcb45b92339cb30c6799ac6cd62447f7ff997ea6`  
		Last Modified: Sat, 21 Dec 2024 02:31:22 GMT  
		Size: 1.1 MB (1053755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057c91935af486340f994b225da70f1ae43bcafc5c94d36ef3d684a1fd2ab71`  
		Last Modified: Sat, 21 Dec 2024 02:31:23 GMT  
		Size: 16.5 MB (16541268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2108a69c36bc239d53685553f4bd752c9c576d02ba89aa4b88391b7890f7985`  
		Last Modified: Sat, 21 Dec 2024 02:31:22 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9f9863be6cee098a8639f324012382b55abeb5fc8d6a95f6d00f92a810d3cc`  
		Last Modified: Sat, 21 Dec 2024 02:31:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7496e6c3da473cb51839caf84eeccaa2eb77f696dc576916e0edcf3e10a1c71`  
		Last Modified: Sat, 21 Dec 2024 02:31:24 GMT  
		Size: 16.9 MB (16892489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a426dfc199253df3172541737527866ca323e5962bcbe54c2eda7b68bc1f41a7`  
		Last Modified: Sat, 21 Dec 2024 02:31:24 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0683e70830e4fab102872fc654990a158a9278ab3cfedaec2971cfd6ba8b9ef9`  
		Last Modified: Sat, 21 Dec 2024 02:31:24 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:c029b1046efbe59092f2d000fe84588aa85ebad4fcdf9a878fad387a1e754d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 KB (58681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e183fe3c371f84cace78a1dd6d5b7d8233e18aa778fc4f5f458b9f5cbf7efc`

```dockerfile
```

-	Layers:
	-	`sha256:e240e74a37c2214ba063d06bb89086dff9b2904a7f52c919064b5abca4167c70`  
		Last Modified: Sat, 21 Dec 2024 02:31:22 GMT  
		Size: 58.7 KB (58681 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; 386

```console
$ docker pull friendica@sha256:fd7ddb45ce8204b626b188670408ae7ab2d02346f9e2735c3409e627824b1426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219836266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee061f881c0a5eb8088390aa1b4233e6ef633dd906091948035105cba635b6ce`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 17 Nov 2024 02:07:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 17 Nov 2024 02:07:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_VERSION=8.2.27
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 17 Nov 2024 02:07:21 GMT
STOPSIGNAL SIGWINCH
# Sun, 17 Nov 2024 02:07:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
WORKDIR /var/www/html
# Sun, 17 Nov 2024 02:07:21 GMT
EXPOSE map[80/tcp:{}]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV GOSU_VERSION=1.17
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
VOLUME [/var/www/html]
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_VERSION=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
ENV FRIENDICA_ADDONS=2024.12-dev
# Sun, 17 Nov 2024 02:07:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sun, 17 Nov 2024 02:07:21 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sun, 17 Nov 2024 02:07:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a951f0874bb9b8010bb5bed40723198b933b9b0af3994b5911c86ddd380d5`  
		Last Modified: Tue, 24 Dec 2024 22:24:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadc515c061fe38cbef16f17b9772360c74a18686a3cd1fbe93c179d342da20e`  
		Last Modified: Tue, 24 Dec 2024 22:24:11 GMT  
		Size: 92.5 MB (92521312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7119adf6be95e83a6208a795e10da4b8ab26a5c8845b078fa5f1050dd8571470`  
		Last Modified: Tue, 24 Dec 2024 22:24:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe69aaff2d3c7e4d0955e91a9a7ea949a625a5d9bc41f4c59150454c3388a681`  
		Last Modified: Tue, 24 Dec 2024 22:24:09 GMT  
		Size: 19.6 MB (19552834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc8f00f3541bfc4707c8e633190f1ce5db88551227bfe06d870f3a05f6bf1c`  
		Last Modified: Tue, 24 Dec 2024 22:24:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85f995ddcfb9eb6ca33f0c0c19c9a3121271aca0818bd29a7760de17bc9564`  
		Last Modified: Tue, 24 Dec 2024 22:24:09 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65dffb0fc09b07b006b0a09415332c44a85824eb6e673defea3f37cf61e37e`  
		Last Modified: Tue, 24 Dec 2024 22:24:10 GMT  
		Size: 12.3 MB (12274978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b277f9246699215d30f748a0e06a85c4b10429377ad460cbc9c43bc1827408`  
		Last Modified: Tue, 24 Dec 2024 22:24:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4cb820c560b3bd4e95b7415955db052b2cc7562bfa5c10643047b4abf4543e`  
		Last Modified: Tue, 24 Dec 2024 22:24:10 GMT  
		Size: 11.6 MB (11595931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2131c33d1adb1651fab57f155e8c65df43818adf0dcc2bef679dd05333118`  
		Last Modified: Tue, 24 Dec 2024 22:24:10 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f5ddaa36068ba01b984f892a42a240c1a6158448c6f0672402a78e020c4c78`  
		Last Modified: Tue, 24 Dec 2024 22:24:11 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7a3a8ad318e49de104cb657ef87a6b63c30146c7451245ffff968cf168b60`  
		Last Modified: Tue, 24 Dec 2024 22:24:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f55821dc120308e2cd4b481ac213bf650c7676d6d5fa8fe72f9f8f2d6bfb02`  
		Last Modified: Tue, 24 Dec 2024 23:22:33 GMT  
		Size: 16.2 MB (16190352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5862c75215b18e396fd6c3f241e61ce5062a9ce269e7f406d5b278af8439ef6d`  
		Last Modified: Tue, 24 Dec 2024 23:22:32 GMT  
		Size: 1.1 MB (1096571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4284e95c33295b67d205fc0e3cbc7e3ea2b96fe7a67ca613ef9fc7babefb3`  
		Last Modified: Tue, 24 Dec 2024 23:22:33 GMT  
		Size: 17.6 MB (17569694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e11075a77aa59898ccf09daae554585ec352e8859b69e80ec9de95dc90bbc5`  
		Last Modified: Tue, 24 Dec 2024 23:22:32 GMT  
		Size: 647.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139ebcf84452f5bf4a4d270ea943569d6f6a69289300e894321d735560b93edb`  
		Last Modified: Tue, 24 Dec 2024 23:22:33 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622469f646baf0d704e9e1f98611170634348ac85789685fb0d05deeb893c9a0`  
		Last Modified: Tue, 24 Dec 2024 23:22:33 GMT  
		Size: 17.8 MB (17844255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0553945118eb20ff6c412a288e53799df1c218c643ebbe10085758bd5ab13ba8`  
		Last Modified: Tue, 24 Dec 2024 23:22:33 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13735550b582dbaf4bff795c732f20d74494f5f543502b23e6f3d5a053c78fcb`  
		Last Modified: Tue, 24 Dec 2024 23:22:33 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:1a9573199fb5edfb868d89c9fa00aefee899741aae5b89a8a7ee4f2c3ddfa281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c40da26247ed916ec3ed48d1a561c4f0cbeef0178a43ecdbe0d8d478f9e75c`

```dockerfile
```

-	Layers:
	-	`sha256:717a93431167db252b445d3febee6010cbddaa025a7a492bf6e2eb7efb922248`  
		Last Modified: Tue, 24 Dec 2024 23:22:32 GMT  
		Size: 58.5 KB (58460 bytes)  
		MIME: application/vnd.in-toto+json
