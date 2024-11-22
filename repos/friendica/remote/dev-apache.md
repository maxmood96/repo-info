## `friendica:dev-apache`

```console
$ docker pull friendica@sha256:2aa7fa9c1593f9134b55ad5ddedd5c3e6b49396564e067b6d17d301ba01f7faa
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
$ docker pull friendica@sha256:8db1deccfecd75ca162d9c49f06b8a60bbd1ad4bb22e42f0458ae89557938efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217769371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ca02c6821cadbf60a1805d498338398ac8e758a22f57afd2e4c766b723f5fa`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 22:39:30 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.26
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 22:39:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb4e9a2fcb05a290f77f31597d6909925f6da18152ad91315edaee03939bde`  
		Last Modified: Thu, 21 Nov 2024 18:00:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25583d18515e1b501c41ecba74a23a887ae165ac1869a48e1ad2751d5da0184f`  
		Last Modified: Thu, 21 Nov 2024 18:00:05 GMT  
		Size: 91.4 MB (91448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e622ab61136363f89bac172f18a8f82b27867bdab0b0dc4dcf8e11d9c6c60e`  
		Last Modified: Thu, 21 Nov 2024 18:00:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba93a430a24f1e9c25890589c3b660f4b878aafa32dd6f5a225567d4e923adf`  
		Last Modified: Thu, 21 Nov 2024 18:00:04 GMT  
		Size: 19.1 MB (19064378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f4c0597e9c7996d4df5f80ef7865859197a02db2bc3588b04a2be4e94bc907`  
		Last Modified: Thu, 21 Nov 2024 18:00:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d19d8730856eb80ad0a75dd268968298a510b179219eb87f95572055f9159`  
		Last Modified: Thu, 21 Nov 2024 18:00:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb0ad150174408b7077283de8f5cdf42f6fccd79afb4c4f3ede782457e3290`  
		Last Modified: Thu, 21 Nov 2024 18:00:06 GMT  
		Size: 12.3 MB (12264208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8841cc16c270b9e7c2eb919dcfe806a99b40ba05ae6055305a40ccbd1e18156`  
		Last Modified: Thu, 21 Nov 2024 18:00:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9fa4331f1bdefc7cffa4c66cf4e10f080ba4f96c590e08058edc045bbd02ab`  
		Last Modified: Thu, 21 Nov 2024 18:00:06 GMT  
		Size: 11.3 MB (11349702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47f24e3d817d06af5b71bfecb19c3ac76b176a68cf4f999af2361221defca4`  
		Last Modified: Thu, 21 Nov 2024 18:00:06 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b420df03a5db6c0b16bb961094d3c1bd081a0b1c72b3f86bb22798a6fc9a2c`  
		Last Modified: Thu, 21 Nov 2024 18:00:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58f93ca64353ff087d2a0925de8e9687e0b830797852c5c2de8f257bf3b63`  
		Last Modified: Thu, 21 Nov 2024 18:00:06 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b686a7773758702ec035493ca92b5f9b2291cc03625d914cf7910255f39c53`  
		Last Modified: Thu, 21 Nov 2024 18:13:46 GMT  
		Size: 15.7 MB (15681171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f020835dc266c98aca84a130908722bed9ab2014fa7f917c86a0262d239b8975`  
		Last Modified: Thu, 21 Nov 2024 18:13:46 GMT  
		Size: 1.1 MB (1122742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066d2431325e363e4aa2ec483c520a31052cc87f246da516b6bc0e229fc557d`  
		Last Modified: Thu, 21 Nov 2024 18:13:46 GMT  
		Size: 18.3 MB (18308237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4c058dd89d5de21a2a6416a277a4b0290bce33944ed3a5d6a522fd9e00a711`  
		Last Modified: Thu, 21 Nov 2024 18:13:46 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d1c3a06291c6ead65c2fcdf5c62b7b42c4229584f4690d27fd3e29f190e0d3`  
		Last Modified: Thu, 21 Nov 2024 18:13:47 GMT  
		Size: 532.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70b2bff205f2aad0c1da3de2a36f8e2f018ca74ab300e7703e96beade3e684`  
		Last Modified: Thu, 21 Nov 2024 18:13:47 GMT  
		Size: 17.1 MB (17067149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846c053992c4e135e5e88e746ff7ea1444cef432d94a09aed1e4dc9997d4678c`  
		Last Modified: Thu, 21 Nov 2024 18:13:47 GMT  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2939639b16c62d4a4c81e0ff25a36b7f1551603a2d1efd8904cdf0967e5905ec`  
		Last Modified: Thu, 21 Nov 2024 18:13:47 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:972be74dfd2f0a28c30312eda74b54ddc87487a2761f662e969bcdd597ed16a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39e5d6384ce0ae7ec20312d1b82d548a6246304cf18f9565b600976ca1a6fe3`

```dockerfile
```

-	Layers:
	-	`sha256:ebfbc6b633d859038beb1e90afc58ab446c37ff7d0e50da81354684ef1ca8e57`  
		Last Modified: Thu, 21 Nov 2024 18:13:46 GMT  
		Size: 58.5 KB (58502 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:85f6ebb4531db7f771c818c2d8252734c6faa718f446968a1bfe49c9124ba29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184384747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6909c844013f8b05fb2e1e07103a06f53545c4b68f4c93f3a0a1580d295a6ac`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 22:39:30 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.26
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 22:39:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8516b12615a3e7a2a821bfa14ba9dd6f6761aadf1ebf4642a203f52c8e3818dc`  
		Last Modified: Tue, 12 Nov 2024 03:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7345669dd3937e5ef95133666ed38ccd4ce9f43d25a81fc19533223b2f1211ab`  
		Last Modified: Tue, 12 Nov 2024 03:32:45 GMT  
		Size: 69.1 MB (69119360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef234fa44e31ba745b124f418b0d1419fe927ae1ee59212901e32e4379c7b7`  
		Last Modified: Tue, 12 Nov 2024 03:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccc67da31d98741d766e1e14576a1a4a82179ea731b27b5216521be2fafd87`  
		Last Modified: Tue, 12 Nov 2024 03:38:35 GMT  
		Size: 17.8 MB (17816970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc212dc8c99b268b545549b3677382696cc7e45f8be1e0c02c117ee197066dd`  
		Last Modified: Tue, 12 Nov 2024 03:38:34 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96b11091bf09cea00b18aea6d6b26267f9206d9808f570ad2841552ba5b7f99`  
		Last Modified: Tue, 12 Nov 2024 03:38:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e476a38ed75111603d0a5b7a9cf510fd8ad50fb0801d92d041ad153e8b6df35`  
		Last Modified: Thu, 21 Nov 2024 19:56:23 GMT  
		Size: 12.3 MB (12262662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2144a61d66ced509bff1cb44ab9c3baf58e86e34ce35d0e5aa172ddbd0b0a7a`  
		Last Modified: Thu, 21 Nov 2024 19:56:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4591ed20b161fd368b2d6ad5ede137d6d74a7fe5c616e60de379bacb6e9acf08`  
		Last Modified: Thu, 21 Nov 2024 19:56:23 GMT  
		Size: 10.2 MB (10199263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef27f00aeaaa75a95db643550e7f1192d997bd61dcf3fa568bb65a6421f34ef`  
		Last Modified: Thu, 21 Nov 2024 19:56:22 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3dad0e14de3d6ea18ad299bf85b43e09ca3caa9b648278e3200a96336369c6`  
		Last Modified: Thu, 21 Nov 2024 19:56:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eeb22e5b2dbdda436b88d58edb10a78b83524ca6464a827d4b90b5bd286a71`  
		Last Modified: Thu, 21 Nov 2024 19:56:23 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e40aeec62ebdbb61bff1e02b48dbe109d3fb10ca5b344e5cfade67f90acf4a`  
		Last Modified: Thu, 21 Nov 2024 23:18:59 GMT  
		Size: 15.6 MB (15642368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc94520bc8887336cd94af8fecb64d551d39db9761a51be178e33b8ba853998`  
		Last Modified: Thu, 21 Nov 2024 23:18:58 GMT  
		Size: 1.1 MB (1089477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecac7c1b6c2e913191854d34a27ac51599de7dc6ac8b4b002c82bca509645775`  
		Last Modified: Thu, 21 Nov 2024 23:18:59 GMT  
		Size: 14.9 MB (14897638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95fbea61f8fa2e7a016b4fef3a9828a2b383010f41d961de6e7a1e9eb5f7c5c`  
		Last Modified: Thu, 21 Nov 2024 23:18:58 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc1fbbc5a392ef6136d431bb03c6c9bb08bfcf3a77bf4fe631eedb1c028655`  
		Last Modified: Thu, 21 Nov 2024 23:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4a19cd4850d769d0fe1b21785f49ce68f5cf7c57e7ba6f6f44e87d6c3b49ed`  
		Last Modified: Thu, 21 Nov 2024 23:19:00 GMT  
		Size: 16.7 MB (16736339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9d9957d12df6847a933dcd1749143ad1fbfb9b09b3f092a37b29ecf20da5a3`  
		Last Modified: Thu, 21 Nov 2024 23:19:00 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fc3ceeec4248efd2e98d6128d268e4e7b3fea4fbf56f76128b6ab04a104475`  
		Last Modified: Thu, 21 Nov 2024 23:19:00 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:9de82b077622d1442e0de27085faf01de6ffce218842651185764309982ba6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 KB (58643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02218e217508a6c0e3dfeab253c297ab2cb53d40fe596cf08a4a203c2ed0e00`

```dockerfile
```

-	Layers:
	-	`sha256:69e018454f3c57adcd9ba5161d6a5e7356d764be9ce7a940b236ee09a811aaea`  
		Last Modified: Thu, 21 Nov 2024 23:18:58 GMT  
		Size: 58.6 KB (58643 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:1c03241802ba6886eda5a5f3e282cd5d53bd9859777cfb88ab547b2d97693f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209419253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a05a933ee2fc03633b125c51335766334896e096c768e7acbf88ba8c0a619`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 22:39:30 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.26
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 22:39:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bd3faa0932fc35421ba3d9b516e4a89ae669361e11c5823867344e339bdebc`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3055e0c6f8e9912862ccede0100a720a20054cc3fd5853aae15f71597b84b`  
		Last Modified: Thu, 21 Nov 2024 18:12:00 GMT  
		Size: 86.7 MB (86734316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3b87d95e709de971d52da444f0bcf631b08890e037169e461dcc0609e0cb55`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0938c8c8e3920812824c9c953e2e2d36ed99a6c319f96a60404526a26f0155`  
		Last Modified: Thu, 21 Nov 2024 18:15:22 GMT  
		Size: 19.0 MB (18981079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246d884c9f1b4b8d9c0200579cd9e7cc78f449eae46bca0803f786237a3f7cc0`  
		Last Modified: Thu, 21 Nov 2024 18:15:21 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c256a60d26403b62322d75bf6a15c2709a912dc5dd78e4b8b282b3cf4a832a38`  
		Last Modified: Thu, 21 Nov 2024 18:15:22 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520044ed1d4707c1bc9f78e99f69c9beedad2b5d0bb91f47e5af7a13993ba102`  
		Last Modified: Thu, 21 Nov 2024 20:07:24 GMT  
		Size: 12.3 MB (12263413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0852e1a3d998210b3bfad045d101d2d8d61706d6faa20778b54f42625e91b201`  
		Last Modified: Thu, 21 Nov 2024 20:07:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e84f584a5b00ca28d0cf3e5825ec6d83f48b5bdd53870b5a23547a154e9315`  
		Last Modified: Thu, 21 Nov 2024 20:07:24 GMT  
		Size: 11.4 MB (11438651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5743f3662c69426c76c2bcbe4a845863d25e39ffcf4b94ef8f5e34d0a3ff32d`  
		Last Modified: Thu, 21 Nov 2024 20:07:23 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3dcbd4a57a334b54da1612dff8c104f70b5d408787d447dd295122c050d54`  
		Last Modified: Thu, 21 Nov 2024 20:07:24 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb7f7e9e53b8cd5d2aeaa9b3c02f61fc82adbbd82fd15d491355d1987ccfb3c`  
		Last Modified: Thu, 21 Nov 2024 20:07:24 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e47bc4f3a35d77b2301f0e5038f84b5d4e34a27e4a7ab60f43b4c8d01c3b46`  
		Last Modified: Thu, 21 Nov 2024 22:53:48 GMT  
		Size: 15.4 MB (15442986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55c1763c76811680510d800cfd1eecfc03ead934af8b186ffcd0caa64076b7c`  
		Last Modified: Thu, 21 Nov 2024 22:53:48 GMT  
		Size: 1.1 MB (1053739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725f293ea572fb169e6303cd9a21020d0018430f56f6d00c6982eee74d93a93`  
		Last Modified: Thu, 21 Nov 2024 22:53:48 GMT  
		Size: 16.5 MB (16540439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e11579fe915a81f5b5875f1c6ddfd27cae5df3ceba3e9d921d3a6bc5cbed56`  
		Last Modified: Thu, 21 Nov 2024 22:53:47 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a3a68a1ec954328f3fa527ae353efb1d6b8432d881b431283388b9f7d5c830`  
		Last Modified: Thu, 21 Nov 2024 22:53:48 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57dd44d37515849c80cbb3092e8109a5d245c16263245680585c24c3dac0aec`  
		Last Modified: Thu, 21 Nov 2024 22:53:49 GMT  
		Size: 16.9 MB (16861630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c0fbb72147f542b18a41695535e02efd62198b317a596e0dd161b95afabad`  
		Last Modified: Thu, 21 Nov 2024 22:53:49 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0436399c89f0af4429f8a7ba746c98076661ec031cbdfc9289ab2b1432084e5`  
		Last Modified: Thu, 21 Nov 2024 22:53:49 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:9e3baaac720c08f67c93cd2fe960b9b994466d4711f7c18a3220d6ae41b2cef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 KB (58681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e99ad8117f44abedf2bb62bd801ab59f5b79850f0e6ff755b401991cc78456`

```dockerfile
```

-	Layers:
	-	`sha256:c8674fbb9a06dd52ae04ddaa917ecff4bab61f9a0d1313575d706b1cd2ecc3b0`  
		Last Modified: Thu, 21 Nov 2024 22:53:47 GMT  
		Size: 58.7 KB (58681 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; 386

```console
$ docker pull friendica@sha256:007ced4cb448d7274bd98ab6f5584fc9e40fc1abc67e24edb4d7a6d45f8cd442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220988724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29649d2472f116d380c5f3be6050562a0e22e0e483bccbc9899b39778107c03`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 22:39:30 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 22:39:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_VERSION=8.2.26
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 22:39:30 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 22:39:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 22:39:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_VERSION=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
ENV FRIENDICA_ADDONS=2024.09-dev
# Thu, 17 Oct 2024 22:39:30 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 17 Oct 2024 22:39:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 17 Oct 2024 22:39:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba9f64c1040fc1ad14d01d775141177044907c4aa7ff49a4a400fcf83e3c84`  
		Last Modified: Thu, 21 Nov 2024 18:05:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a2d7425b0238ab12bf9df5bc13c4735c791094a331bc4d8496e7f7b39cb9d`  
		Last Modified: Thu, 21 Nov 2024 18:05:04 GMT  
		Size: 92.5 MB (92521633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceec13c8ded14e7a5313daee13343e5bf84842b7ead1e044bbda520f2b72e47`  
		Last Modified: Thu, 21 Nov 2024 18:05:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c64b60adddd49f0f10d207dfcc753363d8859b12db1674788bb944d1652b35c`  
		Last Modified: Thu, 21 Nov 2024 18:05:03 GMT  
		Size: 19.6 MB (19552803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc4232400f62769e9853f16e9fdba260d5ba7fe88b172090a2fce40b2d5582c`  
		Last Modified: Thu, 21 Nov 2024 18:05:02 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bf37f77782d288b30b234e3cd2e4326797190728e74a0bbe737dc70a19af4`  
		Last Modified: Thu, 21 Nov 2024 18:05:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eacf1380be612145a88b0579f9241bb4d84c513ebd10bb459932897d5c53da`  
		Last Modified: Thu, 21 Nov 2024 18:05:04 GMT  
		Size: 12.3 MB (12263441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0173c532d5b64451c8ee01ab81ec621728d35694fc01a8984e009d33420126d6`  
		Last Modified: Thu, 21 Nov 2024 18:05:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e39a7859900d94e86c46f94eec721e8265a4343af14f6cc5fffab18d35f020b`  
		Last Modified: Thu, 21 Nov 2024 18:05:05 GMT  
		Size: 11.6 MB (11593122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b764a23eba563abc74891fd5863e3464f7cead53b23ea19d4d31ae37fe3359a`  
		Last Modified: Thu, 21 Nov 2024 18:05:05 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f36c5afecd958aed5e33d5cea0a616daaffb7230fc3ce1a9d2c7718ccc09d3`  
		Last Modified: Thu, 21 Nov 2024 18:05:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1af6b2b7f08e2acb8305613135f1b0396177b64bb13a36c9d9c702459951d03`  
		Last Modified: Thu, 21 Nov 2024 18:05:06 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f5cbcda8d835d14e24e3979124d30819552729f20fcf4ee20199154e49d923`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 16.2 MB (16151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aab4c2e8d1fd3d5598fbaa769f217be50dfc30b112ff4f42573ff6783529a3`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 1.1 MB (1096613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d9b4ef063d90af3359e434f4c0494a31f8cb57b09e5ee33c4a9f99f97cb2b`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 17.6 MB (17570281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a082735615918f29346ba5106e54221d5b3952410f2ad1cf475c402023fc48a`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcc19b8a384720f751e3347925fe4b54d5db02d7caf3aeecefee010c8fbe5d0`  
		Last Modified: Thu, 21 Nov 2024 18:13:53 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8552730da76538d519b0be8899476a44fa6afb9791d0c8ac4c78730190820f0`  
		Last Modified: Thu, 21 Nov 2024 18:13:53 GMT  
		Size: 17.8 MB (17804411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562012fea10320c1c1fd680257fccf9500c6174d78f80bac2d3942cbeff6e013`  
		Last Modified: Thu, 21 Nov 2024 18:13:53 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc39fc1c78c7b45ce059dc2854c1e97f9f41a8f20debf35c42a308a26c1ebb13`  
		Last Modified: Thu, 21 Nov 2024 18:13:53 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:b0ddcd8cfbd5050efb26f54ee5bc791090c93a078dc66087b0a1a408d9ab2f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435eece1e167251846cd59bce5482e22104bcf4aa74f6fa8f120e7549a6afa16`

```dockerfile
```

-	Layers:
	-	`sha256:cec0d9452118fc86aa37e1e07af15cc774f42010f535c26ae834ae0934715523`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 58.5 KB (58460 bytes)  
		MIME: application/vnd.in-toto+json
