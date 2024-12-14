## `friendica:dev`

```console
$ docker pull friendica@sha256:2d48b7e291d492e10d0933e9b2c15cc3f171fc572ff157cad82a2884162f9bbf
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

### `friendica:dev` - linux; amd64

```console
$ docker pull friendica@sha256:72bc4bf2023d1d3becff5d430600a0edf3ba722fa1d4493972f382d0b7dfc760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216627856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52e93f4c078a24d0aef5ac49a9c5dd65a09b19bf1d36313a56712f4b330fd01`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 17 Nov 2024 02:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
ENV PHP_VERSION=8.2.26
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab6856b2c55df8e1c623899dfa4537034d36b336fc16570ba9e8405f98b934c`  
		Last Modified: Tue, 03 Dec 2024 02:28:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe515399e2ac57b09a4612e038c6f7c72dd404a5e67b54fde4c47ecf5d3bf08f`  
		Last Modified: Tue, 03 Dec 2024 02:28:41 GMT  
		Size: 91.4 MB (91448390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd49ea1c0a741382fb74b61e4543aca74349d4d8dcc878fe3f558a1eb08ba71`  
		Last Modified: Tue, 03 Dec 2024 02:28:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f308ee78d90c709d5e259a7580d67b747e4201b5babef0bdd4b328b2fba72a`  
		Last Modified: Tue, 03 Dec 2024 02:28:40 GMT  
		Size: 19.1 MB (19064412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456860cf97ed45144a23bb26e507f3c5ae8993a54d3260f5886e811dea6fd1a9`  
		Last Modified: Tue, 03 Dec 2024 02:28:41 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c03163c24a50e2b30c31068f22a2028c48cc9d21ba946dc1ed6a127e290a43d`  
		Last Modified: Tue, 03 Dec 2024 02:28:41 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85946c8ce2f623da0aa2052395137dbe815a2d16471948aa10cfe610d6bf450c`  
		Last Modified: Tue, 03 Dec 2024 02:28:42 GMT  
		Size: 12.3 MB (12264217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3723604684bb12fc2b862465ebf0509e967fa8508187bf4cebf465c2013d5aa5`  
		Last Modified: Tue, 03 Dec 2024 02:28:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c24951e8715a28933e05453910a3899936ec02635126f063816128bce1a6765`  
		Last Modified: Tue, 03 Dec 2024 02:28:42 GMT  
		Size: 11.3 MB (11349688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeb2a2159f0d7f4799dda152413c7223e6003c855d8545af5f3350f79d8e6d7`  
		Last Modified: Tue, 03 Dec 2024 02:28:42 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b812c23413abef80372b165ca8c982b5cb5bad4abcaf6c8391b2732ef460d`  
		Last Modified: Tue, 03 Dec 2024 02:28:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b224dc35d9298802cbbfb553ed08284b7f29dc14f4d08f511cee6f4ffaeee`  
		Last Modified: Tue, 03 Dec 2024 02:28:43 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a640b3253bba6e9c30927e36ab09eb174aaeab33ca7e4e4932898ca138bdb692`  
		Last Modified: Fri, 13 Dec 2024 21:30:01 GMT  
		Size: 15.7 MB (15710065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af859c6303bea87cb2938b57360050298ef635ae1f72f59a772e59af0d8007`  
		Last Modified: Fri, 13 Dec 2024 21:30:00 GMT  
		Size: 1.1 MB (1122713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76faf130343753e59b22b3746da8d151871e515362d8d72d873a492e789d3c8f`  
		Last Modified: Fri, 13 Dec 2024 21:30:01 GMT  
		Size: 18.3 MB (18308482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cbfda4e19724da10c3dda4fee0ff435a11766a42b9731e077e14c1aac16ef6`  
		Last Modified: Fri, 13 Dec 2024 21:30:00 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1d79a5be8506586f158f479eaac05c6203e07aed2e01458d1e3df10b7bbbdf`  
		Last Modified: Fri, 13 Dec 2024 21:30:01 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923c47dcf1e30442effa0b7cc467c27133cc2ab89519b1a70b47397544e384ac`  
		Last Modified: Fri, 13 Dec 2024 21:30:02 GMT  
		Size: 17.1 MB (17095842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2522ec99825f10250dbcc3ac43357283a1c4d6f83c1142417e4b5b880ef313f`  
		Last Modified: Fri, 13 Dec 2024 21:30:02 GMT  
		Size: 3.8 KB (3818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46f649d3523ea983c482b777bfb268e491fb54601b327462302457a56251bd`  
		Last Modified: Fri, 13 Dec 2024 21:30:02 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:b173d32076fba0ae30c018c2db1115a4aab19470b0efdc41b222fea85f9753df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5461ca13fbb2c2a13e27ccfa496debe1acd44db774926fd8db09dba7b758b5da`

```dockerfile
```

-	Layers:
	-	`sha256:de65af80d01159fbfb1d18f0e333a8e81d05464b951c85997983a5552e9d7e84`  
		Last Modified: Fri, 13 Dec 2024 21:30:00 GMT  
		Size: 58.5 KB (58501 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm variant v7

```console
$ docker pull friendica@sha256:c4df8da22c3e47cbf8c4d877bdd3ff44e7f5277a171c6c507ba8b0ebe0b42766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182979214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a956e891142d8b81f9ba227d81a2b130c6d1bafa5674a0762499e22e27e8939`
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
ENV PHP_VERSION=8.2.26
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
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
	-	`sha256:aaaa85692ebeab1c6fd8ab6388c913202ccd290f0936291d0e91e4327dd8de36`  
		Last Modified: Tue, 03 Dec 2024 03:58:08 GMT  
		Size: 12.3 MB (12262575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d59accc50a0029179981d188b1b03cb7eb36c75686077ce5e595e6473489ec`  
		Last Modified: Tue, 03 Dec 2024 03:58:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818f2d0c07ddb6380570064410e89e649724e6eb90cbbad17f1bb4b90bd3439`  
		Last Modified: Tue, 03 Dec 2024 03:58:08 GMT  
		Size: 9.8 MB (9810854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b941a53a18e07672587e73b73e80dcf9895a1fa9980740ed0c8d4c4e25b60f5`  
		Last Modified: Tue, 03 Dec 2024 03:58:08 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6902850a134ba483c05573047f72f036f85bc9bcc9937e782bbd7570a585c6b`  
		Last Modified: Tue, 03 Dec 2024 03:58:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffea249b6de73c7ca678eaf845f34709ecc52ea78022385d78fdd1fe757eb4dc`  
		Last Modified: Tue, 03 Dec 2024 03:58:09 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89b6ced124246b91571e9fafe47a4d25d444d09cd2b4ec4edd3c4eacbf3ce8c`  
		Last Modified: Fri, 13 Dec 2024 21:30:04 GMT  
		Size: 15.7 MB (15672694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2717a562715476fd9780ce401ae1158341ed3d4b9c15499aa9af562ba4a0cfe`  
		Last Modified: Fri, 13 Dec 2024 21:30:04 GMT  
		Size: 1.1 MB (1089235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166ef49e50a0768f89246a1470d325a20128798e7f5af4f5ffb992b0e3dd17d2`  
		Last Modified: Fri, 13 Dec 2024 21:30:05 GMT  
		Size: 14.9 MB (14897343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3242ebab338c638b6ad32c3ab2425dc7388539de3c42e9d078eb991e1dd392`  
		Last Modified: Fri, 13 Dec 2024 21:30:04 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81928ec36b76b6f6c2ed2166999dba0762e4bea3274a083ef2b32be9022f89c1`  
		Last Modified: Fri, 13 Dec 2024 21:30:05 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25de598e70b4088845d4deef036ef04fa733520fc82de403890dbe8d2c449b7`  
		Last Modified: Fri, 13 Dec 2024 21:34:21 GMT  
		Size: 16.8 MB (16765146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76374205e9212611b78cd82c73d393c5f109db1d58c6cf03f120456830589b9`  
		Last Modified: Fri, 13 Dec 2024 21:34:20 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fe6c2840a3696c6e10bd2132d9b35bdef0b7c2322f1f7e520261aff3be1dff`  
		Last Modified: Fri, 13 Dec 2024 21:34:20 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:d52b110138d988e1ea325e45a6e57361261a5315deab1056c4a43e3ab9b851c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 KB (58633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cbac6071a780006b6e529452e798fe6cac7f4205db17bd06b371ea3ad28e11`

```dockerfile
```

-	Layers:
	-	`sha256:9ffe7297d80842bfa9c02c8e1694a520c3d05bf19347256dc47a703451b06b2c`  
		Last Modified: Fri, 13 Dec 2024 21:34:19 GMT  
		Size: 58.6 KB (58633 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:3a55e5682eedef7112db907648331e19f019a0c5a86906694a3f4d8dfd3b0682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208130232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785af3c46dc1ff70596fb01cbf020477b1a31627a5a2a3aa8f455a24e0a2df3f`
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
ENV PHP_VERSION=8.2.26
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
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
	-	`sha256:15c358a3091f965bc34969de8ea37d4e2ede4a65cdf052c6b4deef6ec798bcae`  
		Last Modified: Tue, 03 Dec 2024 04:16:03 GMT  
		Size: 12.3 MB (12263406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d116b4b452721692af7b4ac71d7cd80ef18fc9e707eb85d64ac2180a4767b`  
		Last Modified: Tue, 03 Dec 2024 04:16:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162548e85294a2ee59b3d44232d0eb9c9f84cc0ed0a193c6eabf47cb309a0f0`  
		Last Modified: Tue, 03 Dec 2024 04:16:03 GMT  
		Size: 11.4 MB (11438639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e042f5acb8603921eca1dae148d8e3b07ea3e43e82df5fb6a6462b2097d2bd2`  
		Last Modified: Tue, 03 Dec 2024 04:16:02 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d100a672003b48e8a0852bcf360625d18bc209dfeb81b26e9e197e85bce76`  
		Last Modified: Tue, 03 Dec 2024 04:16:03 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b4489c982c2def6bf22f3bdad2dcf9efdc2419fdf1bc7e746eed29a6ef038`  
		Last Modified: Tue, 03 Dec 2024 04:16:03 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f35425d682aadb414aec07585119c6dae06d23a185565b4666f81aaa820666`  
		Last Modified: Fri, 13 Dec 2024 21:41:17 GMT  
		Size: 15.5 MB (15471431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ee24d7ec1017f828325d32a083f6e1a24b0d6288310f91554088e9dcc8d20`  
		Last Modified: Fri, 13 Dec 2024 21:41:17 GMT  
		Size: 1.1 MB (1053726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c4ad8d5eba75ab72a72375d7f0ab93f0d4c3cf88f5cf9e3042c47826e4ba58`  
		Last Modified: Fri, 13 Dec 2024 21:41:17 GMT  
		Size: 16.5 MB (16540501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50a39735495764eb9440c80d080fd2c05a96d322e14bdf7931a484d3bb8cb`  
		Last Modified: Fri, 13 Dec 2024 21:41:16 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9440b05c3c5ab672d278d7069b5e100b217dd99bbf72fee41186c3aa6041eeb`  
		Last Modified: Fri, 13 Dec 2024 21:41:17 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1c4869b1c4e044a4f0b4c1a4ea81f569f5265b4e93cd900180393eca149c0`  
		Last Modified: Fri, 13 Dec 2024 21:41:19 GMT  
		Size: 16.9 MB (16890495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4bbf0ef77ad91620ce421eb7d1426e36e0a1b043dce825c246632518d50bc`  
		Last Modified: Fri, 13 Dec 2024 21:41:18 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9f22d87761d75765c8d7d1bd0704795dff5f61921b0de87c13bf24f1c2477f`  
		Last Modified: Fri, 13 Dec 2024 21:41:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:93dbc4d461eb8853a54c81154a85ceb6e5d3d8a199f3e71533089e888d0fae8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 KB (58681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30d1241b610712b688b1774b3bf83203255a43c8390b5c3f89bbd3e5e95920`

```dockerfile
```

-	Layers:
	-	`sha256:82843156811b4e8240b6b3713fa9f8dc6f92d89e378124d636bfd42ab6b41d18`  
		Last Modified: Fri, 13 Dec 2024 21:41:16 GMT  
		Size: 58.7 KB (58681 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; 386

```console
$ docker pull friendica@sha256:b0f46a8f554ff43c84c9ec6f46e29f71bc16b85249051273b3a76d0d6c9b47e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219805624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb2c028d620330971831dc5991e826fa6f54ba389112c690ea65f01634a5762`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 17 Nov 2024 02:07:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
ENV PHP_VERSION=8.2.26
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Sun, 17 Nov 2024 02:07:21 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
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
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac72b3687c8036b6ac087f9410b22c7cb40e878b0f989cac3450fc481b0852c`  
		Last Modified: Tue, 03 Dec 2024 02:27:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d72dfce6762e9a753c22745b9ef5da9eace280a96d5d6e714161a9a5d81316e`  
		Last Modified: Tue, 03 Dec 2024 02:28:00 GMT  
		Size: 92.5 MB (92521751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5e923af0f077dc2bfe4ee9320d5a72a805fbaa906146b6bdc186faa103eba1`  
		Last Modified: Tue, 03 Dec 2024 02:27:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e02b72e003052d2ffaff36901a88561b549caebfe1a1d11c58ab0cb5296f5`  
		Last Modified: Tue, 03 Dec 2024 02:27:58 GMT  
		Size: 19.6 MB (19552821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d31777159c94cfc305e3a1702011e1b26976978f1d00da13ef1e8c996c5c2d`  
		Last Modified: Tue, 03 Dec 2024 02:27:59 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ac5b3e50a58fbd915c1ed0b741d688d9755535aaf9be2938787ffe5681dc92`  
		Last Modified: Tue, 03 Dec 2024 02:27:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951b3a7435b6763e2d40484fced89ecfae1a1fb19e3aa4eb1d00937f6b08b577`  
		Last Modified: Tue, 03 Dec 2024 02:28:00 GMT  
		Size: 12.3 MB (12263433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e26c1218f5f4c41bfa8ea03e802be08c569ef4edd379a4e7cb7cef04ba9231`  
		Last Modified: Tue, 03 Dec 2024 02:27:59 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f38df7d483e1b7e2cceac4109db800ac40949f5692a3480ced1a202aea27c06`  
		Last Modified: Tue, 03 Dec 2024 02:28:00 GMT  
		Size: 11.6 MB (11593163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73d04fda88e14d9893f0e89632bb165c3cfbc6c9d21b6320c85a619192fe5bf`  
		Last Modified: Tue, 03 Dec 2024 02:28:00 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00f7bb65566f69fd43f1187cb463254ad8da402061e2abbfc68cf717af8e942`  
		Last Modified: Tue, 03 Dec 2024 02:28:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588a00616ed6e970321f3d267631fa035f7006ba09ef84cb283d9cd627c3e7d7`  
		Last Modified: Tue, 03 Dec 2024 02:28:01 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445937115118f8b2db71b9eaa909abd596f1a9ccc7dd1cd30fc05dfe523b6c66`  
		Last Modified: Fri, 13 Dec 2024 21:30:19 GMT  
		Size: 16.2 MB (16181783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2daba103dfec99dbf1212cfa112b5068156de27b94c56b3acad246f2b2f39`  
		Last Modified: Fri, 13 Dec 2024 21:30:19 GMT  
		Size: 1.1 MB (1096643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa23385ecdff8916e15d96a6f25b60b8fa44f0fc04209f0e1396c4de68ade56`  
		Last Modified: Fri, 13 Dec 2024 21:30:19 GMT  
		Size: 17.6 MB (17570241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfdf0f0ab45ae51d8bd053df560d3effc533f64362a8e63c886b6cb766ccda5`  
		Last Modified: Fri, 13 Dec 2024 21:30:19 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62e8d2e84a87f1a6e6bfc6a8b38eb57bd3cb60df30b9b3bf516ce96884c0667`  
		Last Modified: Fri, 13 Dec 2024 21:30:20 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabc5e9231e890816b395eb4d8ba8c9c29b040666e3a51e9f7b63f90076de18`  
		Last Modified: Fri, 13 Dec 2024 21:30:21 GMT  
		Size: 17.8 MB (17835321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef087ec5e12f24b99c1177bef46633d86e448d61e261e847f1ddade0ec1920e`  
		Last Modified: Fri, 13 Dec 2024 21:30:20 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034b92bab47ced8ae36ed96212a6351d94a7679d05c13dfba1e76ec95ec32c4`  
		Last Modified: Fri, 13 Dec 2024 21:30:21 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:ec62151358d5fe053bfca4d695458e5dacbcf567ea4b0a8a97c2852563419003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f09e4938cad83b50c7f8ca045c60602e6a8728d88c0cffb3a1eed100425328`

```dockerfile
```

-	Layers:
	-	`sha256:dd72cd91a9bed43eb03bbf27ab6a012653893c654879537378893cffd7f58b4a`  
		Last Modified: Fri, 13 Dec 2024 21:30:18 GMT  
		Size: 58.5 KB (58460 bytes)  
		MIME: application/vnd.in-toto+json
