## `friendica:dev`

```console
$ docker pull friendica@sha256:0383bb7d491ef9a3d3596b6f69bc2ade06d0c32eedb6deed7a608f26fbe8c539
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `friendica:dev` - linux; amd64

```console
$ docker pull friendica@sha256:fd98ba274af64b95fb23a5c3b048a4e19ed31805c90fa154dbb7afef84583c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250395244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f16f18db5fc12db74bf08d320af53cd10fbf7dd4b1309dd7b66fa856a901290`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff4e528452292981a2ac93047f835ba9d486640caf7845a91952e60263df9d`  
		Last Modified: Wed, 21 May 2025 23:18:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede17ea19b1ab4f341ba469f678704a18b6c77fef12b1a304c4b938784dfbcd1`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 104.3 MB (104326256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe273df9238b3085e53711d838ea656926836c275d4db249792a8c37d95a6f`  
		Last Modified: Wed, 21 May 2025 23:18:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d14161c76a807519d8ff6f7b24d84c607780295847efb8696de2d686181ff`  
		Last Modified: Wed, 21 May 2025 23:18:50 GMT  
		Size: 20.1 MB (20124180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9f091f3dbb2f1fbb15d87a4cb5e7c7a5cbb63b65f53ed3495b52b19357fb35`  
		Last Modified: Wed, 21 May 2025 23:18:51 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ad1b79a553bb2180c567693bbe8f9196d637059f644585439027a4dcd37f8c`  
		Last Modified: Wed, 21 May 2025 23:18:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a05f9f2c31f13b756b5c4961f0cc54e6c5c11a0b359451bf3964b2ef77e4d6`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 12.7 MB (12694937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7385e8172628456b50ad41a74dc5bb181a3a701edd8ddcde52d2b305bb0a09b`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0db1ed3ca8711c9d13321aceff6e9b84b1beab2a974aef32d542263f0fbb0`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 11.7 MB (11657661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b5d65604733e42071ed5c3261ca88c0c62bbfce0cc15ab3473aaa6463b2d6`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91f1574d2c458aff78243b3bef4f1f6b79d08495928d0c432430239bad297a5`  
		Last Modified: Wed, 21 May 2025 23:18:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9242b0c7ae99e2b08c75b6b020e18f470fd40c5ed5e3872147af8902b346735d`  
		Last Modified: Wed, 21 May 2025 23:18:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42800c02c5bc10764ad07c0947c84b6fe1ee23a5ca7df31e0d0707ba5fe7926`  
		Last Modified: Wed, 21 May 2025 23:43:09 GMT  
		Size: 18.4 MB (18388722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2cac9b81c6b1333f6b031839541cf59b6f369be59da64236042f1b3e52b61e`  
		Last Modified: Wed, 21 May 2025 23:43:08 GMT  
		Size: 1.1 MB (1126952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a200a6e8e7cb588ceca8251463430fd8d5a558a70558a09ad5ae64dc0b0899dc`  
		Last Modified: Wed, 21 May 2025 23:43:09 GMT  
		Size: 35.5 MB (35518215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58a683adb04fc2e3d3682d980cfc94ecacf7997d57b2f6611ba089b87d0ca4f`  
		Last Modified: Wed, 21 May 2025 23:43:09 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7ac3267f0dacbcce6b535cd794a72888c10d3b71ee56980687aaf9ed9a999b`  
		Last Modified: Wed, 21 May 2025 23:43:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f471993d00638f4dad2374bca921e9f8d8731c43e7bb099a14f1bf54fe5545c9`  
		Last Modified: Wed, 21 May 2025 23:43:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed96def78b3919021f51ba883e99ec7bbc90cbac4b2bc4b3cbc2efe613c42b1`  
		Last Modified: Wed, 21 May 2025 23:43:10 GMT  
		Size: 18.3 MB (18321429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d269e443763d428c5bc9a9f1ba86d83ee8f50f122aaf16e39c4ca9877736778`  
		Last Modified: Wed, 21 May 2025 23:43:10 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c3221c7791e1cdf68abffebff038d432782e31ddfe30ecfd5fe7d9d6e586eb`  
		Last Modified: Wed, 21 May 2025 23:43:10 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:12355769fb65217b34c0507208050b67501c91f56920800fd992e346fbb72c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9af55cbf9089b716f5bc5491287bd87d682a76179a7d757ed19e20994ec5b`

```dockerfile
```

-	Layers:
	-	`sha256:1f11ed35e698c4985038be2901b3461e6fbe24b80a892676cf3a36918a82a8aa`  
		Last Modified: Wed, 21 May 2025 23:43:08 GMT  
		Size: 64.3 KB (64327 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm variant v5

```console
$ docker pull friendica@sha256:715c37fe8650032f1f529ae09a57efa80925d03a61c4c0de2b4823aa749324d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219502709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c65abf737e8d81abb9a49132d12dd7c50a84922888980343225d6450b44228`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630a0ae6a7caa13c26c641757aedb6f2a685e945563086d454f01db874d5a4e`  
		Last Modified: Thu, 22 May 2025 00:01:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c1543f1d03f96cc1c05ba7756b5950bbb8edfd3038bc0902f7bd06c8b3a5a6`  
		Last Modified: Thu, 22 May 2025 00:01:50 GMT  
		Size: 82.0 MB (81970289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1f2e7aca197ce584722af1cb59310256391ea143b4eee91fe64249d0f64ac8`  
		Last Modified: Thu, 22 May 2025 00:01:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58b58ecad378e2c244a47b087001bd8dd7a6bb20346f6a44056db42ab3a5ce`  
		Last Modified: Thu, 22 May 2025 00:06:36 GMT  
		Size: 19.4 MB (19419290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f2b7224a1481ccb5f31a4a4189cf4eba4409cd5baaf7402ee9bf4a6ba1d7c`  
		Last Modified: Thu, 22 May 2025 00:06:35 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e190f82563d835d64144f74a1701508a80fd49ac413b53cda42a431d89cf4b`  
		Last Modified: Thu, 22 May 2025 00:06:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e3505ef52c3447c23905ef5720ea48318bba8d2d9c1afe16b2847c7ea108c9`  
		Last Modified: Thu, 22 May 2025 00:24:18 GMT  
		Size: 12.7 MB (12692927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c83a05b7dc7e95053753fb0afb429a5b95164d0e1b4c2023b4b2c66f119484b`  
		Last Modified: Thu, 22 May 2025 00:24:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cf948e234dd0fb5fdfe8c8467eab33fd34c277e0dc67a805bcb0a2a1ee0e1`  
		Last Modified: Thu, 22 May 2025 00:24:19 GMT  
		Size: 10.6 MB (10628699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97453db94cc98168d4e7824a7a734d55ccb22b0255494f3fa0060db19b09d4`  
		Last Modified: Thu, 22 May 2025 00:24:18 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5e7eabd43b67e84656682d9bdc1a51256528424a71c9ad78c6b1d3bc1698a`  
		Last Modified: Thu, 22 May 2025 00:24:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927c40e88e5cb098b9ee425dca1ec33cd8fb2bf5fa57e85668512f9e2e410a60`  
		Last Modified: Thu, 22 May 2025 00:24:19 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a81ef020c58d4f5aeda29bdd2640aaab3c754476c3d889a0b86e850cec6465c`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 18.1 MB (18109841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcdadc8ddf7e888d5c26becd7eb0822977e4494264248cccfb06efd05e45d5`  
		Last Modified: Thu, 22 May 2025 04:50:27 GMT  
		Size: 1.1 MB (1102626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e235a124f0df46904bc480f4b2a226c3afdce309d9f153867a60d473ba5e28`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 31.8 MB (31763758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d722f27f8c45b0c7e58d01827f36df5b9efb0484516b062e9136690487de7a`  
		Last Modified: Thu, 22 May 2025 04:50:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f6401cadbf4cb7a614f6cd5612895d0de92cc2d04f281836bece42e46a56a`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ffb8e3be806dd39579f249b47c2eafa06be5bfc9185cec7c17fc61b70c6cf9`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f63deb7255e8c340bce94ac625c5d1ce32edf127e960eca00c792ec92e28517`  
		Last Modified: Thu, 22 May 2025 04:54:51 GMT  
		Size: 18.0 MB (18046803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c7511da6846b65454257f9672f22f2ba98b368986f79e9abe53cd0a2c37494`  
		Last Modified: Thu, 22 May 2025 04:54:50 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8ac3655fefb320fbb6f807d91e1e329c81ef8b687a40df2c40a499ccc137cb`  
		Last Modified: Thu, 22 May 2025 04:54:50 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:3afacc72aabd7537de95cf084081a347ac7c6ddcbca626b16a76ccbba81e6397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 KB (64471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5643c3d090238499dec6686c7f1ccca84b21dc127c88696eb0026dbcfa3efc`

```dockerfile
```

-	Layers:
	-	`sha256:960c8e412eb87a0def93cafdaa66748424eeb30283a7b852ce885e5aa806dea7`  
		Last Modified: Thu, 22 May 2025 04:54:50 GMT  
		Size: 64.5 KB (64471 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm variant v7

```console
$ docker pull friendica@sha256:f2f455bc4bddf80320287fc0eb17e519c95afaf3d6aa8a3c750b8b4e067e2d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208740667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a5844de18ab09619bcc23e1c77a73c120c079069c442601ab3483436a0e7f7`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb081af16798c509df91bb641dcb17bd3d33d61f0cf2bac99faf83bffbd9b7da`  
		Last Modified: Mon, 28 Apr 2025 22:37:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf0e8dc8cea29863841153fe9f3a8f89bbb039cb649bf7121f6bd16afce897`  
		Last Modified: Mon, 28 Apr 2025 22:37:33 GMT  
		Size: 76.2 MB (76161444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0d9733969300ceb14706abdd215b86e83169f1554815cbb19abf8d4283b57`  
		Last Modified: Mon, 28 Apr 2025 22:37:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f48e0c7265485795f32b113efa9b04a68faff23123e36dcc1c1409a0e2ebe`  
		Last Modified: Mon, 28 Apr 2025 22:41:55 GMT  
		Size: 18.9 MB (18857578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef6e5c0032a0aa361aa51604b1c53cc9877e3052605e5f873db12f418bfd7cd`  
		Last Modified: Mon, 28 Apr 2025 22:41:54 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d01a9a8ce471d95f06223a7d884bcf99a1eddbaa15f1e4a668e504b9bd3fbe`  
		Last Modified: Mon, 28 Apr 2025 22:41:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00061edfe4e406afa4aa8ec5e455cbfa02fb1e48bde365d770f7530f872d58a5`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 12.7 MB (12692880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f52e86bc33e41fda247977375499af31e3543860f6e0a825db503f7b3f94500`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ddc7d51077483608fe01a866cdd2de8cb567f5838f40bef17565435dab914f`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 10.1 MB (10052334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c49898d54bcbb53097b7f9341eba6689a3b4f9aaebe74ad22fcf060bb1f69`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccf783b7a7bb6ab4398b04011e22ceea4ed0fae19e1e310e2fd05252ec0d2a5`  
		Last Modified: Fri, 09 May 2025 17:57:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b56492d36e11dfd74e6455943015db808d78c91a92fe37dde3b407f475b25`  
		Last Modified: Fri, 09 May 2025 17:57:49 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247075413be4c95baf06067afcd2179bbd77e5782b931213a8c18a1292c03318`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 18.0 MB (18015704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9619e0fa15d445fedc4ae9c22a93222ae89292c347e95f7658083ed5f20d6014`  
		Last Modified: Fri, 09 May 2025 19:54:04 GMT  
		Size: 1.1 MB (1093105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e4e38b1d96cf124c71ac7468995544d419975373eae00bebe03797e9cf0b7e`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 30.0 MB (30039696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a993a8f1fedd8903e6559e15b022a283b187b6528c5485d32da9f807e40e58`  
		Last Modified: Fri, 09 May 2025 19:54:04 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a089d13d798804230481987b59e765c257a1900c512e66b16e63a00c2b58b1`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41cca2d909bc570fb70b1c4abfc9e7632ec1cbed197ea9d754faab910e3af30`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a249d0cd48af8389e20445693662a4dca7ca654616b882d7f033cc81aed110e9`  
		Last Modified: Fri, 09 May 2025 20:00:49 GMT  
		Size: 17.9 MB (17878272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1edaecfc9213a514687fcb1e104ecd790ae3f8d47a735bde1c74c201724412`  
		Last Modified: Fri, 09 May 2025 20:00:48 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93f374f48bac9ea3fc324446c82f0eac6ca3d7b85da6327a1b4c3ad8587e42b`  
		Last Modified: Fri, 09 May 2025 20:00:48 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:9ed9e74283fd99811ded6fe70da7bdfa2a2ea02d921904fb5d95bffb70fbb12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 KB (64470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415ff3e81ccdaf495900aa9abded9261180b45f33a5c54997075451aa7d87a5c`

```dockerfile
```

-	Layers:
	-	`sha256:b7f33d679088666449e23b2f8d1820799ea7f91cba4990789708039d637fd7de`  
		Last Modified: Fri, 09 May 2025 20:00:47 GMT  
		Size: 64.5 KB (64470 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:3c0c1bdb99f38199924b98461ffc8b0ddbff51ce833cab0f7110f165b414448e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241377676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce5c471545a4dc0aa97595336d5437ae59c1c3bfed3ca834e105b017eb82c2b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162264c942aa762db417d45ba0a061dc8a07fdceff32a29a2d59afdc5dce9f9`  
		Last Modified: Thu, 22 May 2025 00:16:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae464486e7a7b754207a11225be678aa24148395332f33c785867c1ee4adcd`  
		Last Modified: Thu, 22 May 2025 00:16:09 GMT  
		Size: 98.1 MB (98128413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa473689d317e799934b0b99abeaba5a91da4380c0b6148373000ed23bde9ba2`  
		Last Modified: Thu, 22 May 2025 00:16:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c2eb5e806f90915c98adca0127759107240352870bfe86a7178c29ff06f3b`  
		Last Modified: Thu, 22 May 2025 00:19:46 GMT  
		Size: 20.1 MB (20121045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0dcaea15d7a4ebb0f4028699191ca3aa2002cfeec7788806c673ebb001eade`  
		Last Modified: Thu, 22 May 2025 00:19:45 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e656b0988010277ad979af2247a277d3699b9eef4559bbf50725b446fb4510`  
		Last Modified: Thu, 22 May 2025 00:19:45 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348f8a5c7d38ff9d4a6ac85622b907b6638ea2fafb66f642f60a5aea9295c68d`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 12.7 MB (12694665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb922c0029f681cffc7285553daebf616bef66ed18a0231cc6e0290040db485`  
		Last Modified: Thu, 22 May 2025 00:47:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb25ea06c756635811426f88394a1c1cbaa648ba02ec7824b19d7253f685b0`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 11.7 MB (11680311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90280cee654716c2503e730efac74700ad9eefc7d8c4773d66c0d20cc6e08326`  
		Last Modified: Thu, 22 May 2025 00:47:14 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29fcacf279cb0fd4697d3a1e0220eaa4100a963bc43a5ea962ce9aa14e8075`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9af748e1436181f47bc7ea7cc9f6539654115603140e9a49de2bbe6235524cc`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1132a7d24e079ecbd7c3f8d47d21b1fa159bd5595efc5ddf2d59b93b114221`  
		Last Modified: Thu, 22 May 2025 10:00:01 GMT  
		Size: 18.2 MB (18157878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55796a0476403f5bf32be3f69eec6e4ebbe8a4f03ad2469bf19962380ea88f0e`  
		Last Modified: Thu, 22 May 2025 10:00:00 GMT  
		Size: 1.1 MB (1059164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3287a9a36fc7f4e27e5ebe986b61d89289e128a7fbfd7111dced348eab7b0`  
		Last Modified: Thu, 22 May 2025 10:00:01 GMT  
		Size: 33.3 MB (33336191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a91abb0ade44da0bfd7b0718c27613d75b340aaf7e2421036315ff8756417`  
		Last Modified: Thu, 22 May 2025 10:00:00 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7f296edd013fa2344830582abe45d94ef65918eebc299dbc963ec053110821`  
		Last Modified: Thu, 22 May 2025 10:00:01 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55958286061142115c9eb428ba560f0a820f0eab0ac811c698f2ba582edb73`  
		Last Modified: Thu, 22 May 2025 10:00:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2ccf8debcf0355a0e5cd32b59c6ca5b5f139b01385e40723dc309709c64fc`  
		Last Modified: Thu, 22 May 2025 10:00:07 GMT  
		Size: 18.1 MB (18123149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b8a5beb0ca1c4408c5a58ff422f4d4ac0ea4a0d44f516173b195ac20224df`  
		Last Modified: Thu, 22 May 2025 10:00:04 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8df9101d3a6a78f127bf3896527c257211382e27b0f36d81634ed9eb7210af`  
		Last Modified: Thu, 22 May 2025 10:00:05 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:1205c1c56f297972083218a6bb648fc37d54266b8dd7f859aad642d729a6f2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 KB (64510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681033b9dbbde365a6e89fa76d1e2a9457f6a3b8fc912d727924a2caec6b237d`

```dockerfile
```

-	Layers:
	-	`sha256:bdab72bf51ec02264d42285bc979c7a2defb5d576ce87c44de3f37240e4af571`  
		Last Modified: Thu, 22 May 2025 09:59:59 GMT  
		Size: 64.5 KB (64510 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; 386

```console
$ docker pull friendica@sha256:e5b3558b7ccfea49df012bead84c7a0bf969ae00d0f864e532a849b432aa127d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249747060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28310cbfe34962e8d4729ad602b9501331f50906c46d898db859f43f7812e905`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b3ae0a3cc1813c1af104d1cf7c4f2fb9834143d9a6f6542b18b9ac8a5011e`  
		Last Modified: Wed, 21 May 2025 23:18:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd423ffbb88db1940d66d06b0021abd7b5766e7188fb2156024e6509069352c`  
		Last Modified: Wed, 21 May 2025 23:18:22 GMT  
		Size: 101.5 MB (101507449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2711ec981d33e8b6d48b89fe12686a6b9d190c34f687d910e058ecce3225b34a`  
		Last Modified: Wed, 21 May 2025 23:18:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e078877c3eb19610f9232307a243240e94a8a7679f9e7c74f8ea3d7d015021c8`  
		Last Modified: Wed, 21 May 2025 23:18:20 GMT  
		Size: 20.6 MB (20638515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7966f53e345e500f89d42fcdfb69088040771dd1788fea554be117e5258cd2c`  
		Last Modified: Wed, 21 May 2025 23:18:20 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ecb17b503894af45c8bc7a0115aa16b3f9a5c8d615207905395af43786ab45`  
		Last Modified: Wed, 21 May 2025 23:18:20 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc368442cd4c98d41af593ce0da6968e85171c7d52ead09539f7f6e23244bb7`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 12.7 MB (12693889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1852c37f3556ec38ed1c1ebe24c27e384d2a8ba3b280601c53c9f75eb0adb6`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b588806f719016cc417569c4caac2ff9ccdcb4b34f35df4e0657a1c01b037d19`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 11.9 MB (11884509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87e07ec6ac0571e93f9080d3bfa744e6b3f15dec788047d87a83bd7bd116e2a`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6fc221041ccb0c7f1033ad6656bcabcb91c18e2b1a568d96497ffd8ad46c6f`  
		Last Modified: Wed, 21 May 2025 23:18:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d7418adfdbef868f03aa9ba2b0d5c2e0dc5d0833a60ded5f483da4418c8759`  
		Last Modified: Wed, 21 May 2025 23:18:22 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2896f883d0693536a92bf3631128661a02aa315412386837e98a0d721296ea`  
		Last Modified: Wed, 21 May 2025 23:43:27 GMT  
		Size: 18.9 MB (18893737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dee40af8d35ac9335ab9cd4c04b278974ddf70e839748931ddefe11015138`  
		Last Modified: Wed, 21 May 2025 23:43:26 GMT  
		Size: 1.1 MB (1101741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77527f8df49b029581ab1a75b8feccb5e3e473418f5f0c5db4a0f6ad2541e65e`  
		Last Modified: Wed, 21 May 2025 23:43:27 GMT  
		Size: 34.8 MB (34815598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98050d2f5835b4f92097899c1cdc84d866d08db240a52dcebb6c2b39da3e38`  
		Last Modified: Wed, 21 May 2025 23:43:26 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9041f4191f1cb75c271d53dc0452164149ba70f2d330b6b3b98d0ca06887aacf`  
		Last Modified: Wed, 21 May 2025 23:43:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eb2841cad0644f8bd82c2b73c9084590a78a82db18a0d54e3a6a5f0087361a`  
		Last Modified: Wed, 21 May 2025 23:43:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efaf338c2a356b314c89f90f92dd9d417abda6cdb5054c27ec39e418aa26d24`  
		Last Modified: Wed, 21 May 2025 23:43:28 GMT  
		Size: 19.0 MB (18992565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d269e443763d428c5bc9a9f1ba86d83ee8f50f122aaf16e39c4ca9877736778`  
		Last Modified: Wed, 21 May 2025 23:43:10 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f44daef9f0c5ad5115583a94c7ee102af58086bc8a2995077b2673941866bb`  
		Last Modified: Wed, 21 May 2025 23:43:28 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:ed3553fe690794971c90a253d29f32e10b0e75a4d43c918942e800f21e192a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee32a4fe969c5b8df7457456c887295269081c479411efb1283fc6b70e3709c`

```dockerfile
```

-	Layers:
	-	`sha256:f9cfb72b9b6793124cf25159bf2331904ba929142af5efb222ace1cc2290fb0f`  
		Last Modified: Wed, 21 May 2025 23:43:26 GMT  
		Size: 64.3 KB (64283 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; mips64le

```console
$ docker pull friendica@sha256:abfae5e71566327528df226248bd1665d1ce883d4f1fb877500f3df8594c4816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221739535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e91365469ba30f9167b19a9b66f681c6c640ea84e8cd798c184bb089fe47b31`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e343296b3c4c73e7393ed7e975e096d3456974497f1542b5ded29fe811633bf0`  
		Last Modified: Mon, 28 Apr 2025 23:52:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b0bd4e1321051cfa09dfb6902859ff6e7b2447f11cced855ce09ed1bafd8d`  
		Last Modified: Mon, 28 Apr 2025 23:52:23 GMT  
		Size: 80.7 MB (80670410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4373130a8dbde2eecc875cae7f6cbf3eac8351ea553d2b6dd0b3cc0ae00fe67`  
		Last Modified: Mon, 28 Apr 2025 23:52:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56746e7214764a2245cd81e761a98bc9b2d38bb60993b2aee05668d56c16a8bd`  
		Last Modified: Tue, 29 Apr 2025 00:12:26 GMT  
		Size: 20.1 MB (20069252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1ae0bd7a891f0e4b151b24f787e34628dbc935f5716272c2c75ca07fdebb0b`  
		Last Modified: Tue, 29 Apr 2025 00:12:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bae42ff97aff3dbe0d62e06582e5344a420ce7bf0f97e842adae3bb17b01c`  
		Last Modified: Tue, 29 Apr 2025 00:12:24 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8a48666e99263ab500ca2a3162e408743d94da04fcbc48ab94d38ec619e626`  
		Last Modified: Fri, 09 May 2025 17:55:09 GMT  
		Size: 12.7 MB (12692586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27aa2e6140cc3ea9686b1a2563c9de202cd78d97eb274ed418f60aa4b75e391`  
		Last Modified: Fri, 09 May 2025 17:55:07 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a3fb921daa75b1ce5ede793c3821b531f05cc3d0686c381119bf5f5abb3e74`  
		Last Modified: Fri, 09 May 2025 17:55:09 GMT  
		Size: 10.7 MB (10726931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461e22c3ecb1b5f5de7addbdbcacea5514c98d6d6a2c734d8f9535e5b322b771`  
		Last Modified: Fri, 09 May 2025 17:55:07 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285593a6b05b4824d8be25bef9e5c5a908a816ee7af6139d49b794783fa2801c`  
		Last Modified: Fri, 09 May 2025 17:55:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e199382d86c1170c1bbf4396f00d38e7631f7a5109a61903243f116cc7c63482`  
		Last Modified: Fri, 09 May 2025 17:55:09 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243ee52ed8cd9231a90c3ecfae63ebe080db6ce8a30f54db6d43bb8f147ebbe3`  
		Last Modified: Fri, 09 May 2025 19:02:54 GMT  
		Size: 17.6 MB (17635411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f9505989c856262190936119cc4430b978ff6703f53b146629679d96b260b`  
		Last Modified: Fri, 09 May 2025 19:02:53 GMT  
		Size: 1.0 MB (1012467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106398096b8676c8177cfb064dd8eede435866da42c16f39a4a63f34a215dbd6`  
		Last Modified: Fri, 09 May 2025 19:02:56 GMT  
		Size: 32.6 MB (32591138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdd449f67a86b211823da1cfeee24e82721c23cf8f69741698c0326b18dd78c`  
		Last Modified: Fri, 09 May 2025 19:02:53 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40fa24f7d3657f775e59d8688dc047b53f23e9b2c6b4ba1c120305f55938904`  
		Last Modified: Fri, 09 May 2025 19:02:54 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb31def92f6e36c2b54685deb2bd3b14d4e1f27c13034fb658c8b0244c9833df`  
		Last Modified: Fri, 09 May 2025 19:02:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc0ad073658dc74dcecb4204462c5ad4e329f642383f53a681acf5c75332fd`  
		Last Modified: Fri, 09 May 2025 19:04:49 GMT  
		Size: 17.8 MB (17815611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2895857547fde659c7e284132eff426be88d4a357a03efe89f42b5e206e9b544`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357c26f7b5ad87174f0813fb8c39db74c822b94904f2c094b4cad9bd788e5add`  
		Last Modified: Fri, 09 May 2025 19:04:48 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:46605118099d81c50ae47d9d8d52fd0d84f62c46194d2ec3fe69729f55743ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79931f6b9dbf89d61c0d45262017c5d19dd6eefa8549522c86edd61138ebaa75`

```dockerfile
```

-	Layers:
	-	`sha256:a6b1295bf03237bd61ad2603121cd3f0a3035da40bdea6192bd340a346e8e57a`  
		Last Modified: Fri, 09 May 2025 19:04:46 GMT  
		Size: 64.4 KB (64400 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; ppc64le

```console
$ docker pull friendica@sha256:ccd81228c655a9d39bd2266a1dd274fb4a2efce5e8e3935ffd9933d9388456a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255036144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc5b07ca4893909b5a777feb1f264dce765fce66cb477229ad9b90b14ea56fd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0826c2c78ee871653d0f57d9c44ce65866504115c48a8494edbe4acb9069b52`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18cc47752cabbb3e0f444ea51014859eeb381a04a9b84e453b349ceeecfef1`  
		Last Modified: Mon, 28 Apr 2025 22:29:46 GMT  
		Size: 103.3 MB (103313187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72914eeea8bb18897afc016693b242383396e76406f7363c6ba1a9be152145bc`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487cf685ebb89da437ccca9553974ef5d8fd1546d00a240c39c8980e18a9075`  
		Last Modified: Mon, 28 Apr 2025 22:34:32 GMT  
		Size: 21.3 MB (21308396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0caf01294aac11114b41679b137bbd5379d9aadc22bcd925f84a08bdb6c5c2`  
		Last Modified: Mon, 28 Apr 2025 22:34:31 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7c93db4f2696ec7aa86f3d1c0a2db0345e19037a7bb07c48cdf34351262d9`  
		Last Modified: Mon, 28 Apr 2025 22:34:31 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b00489313302f54bd0d669303a922403cbcc754cfe1dd849c6ea76276c4334`  
		Last Modified: Fri, 09 May 2025 17:35:40 GMT  
		Size: 12.7 MB (12694307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f224f764ec8447f306715a2cd76f19aadd70dbef22b16bd8ea94946ecf66e7f`  
		Last Modified: Fri, 09 May 2025 17:35:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0762824185d358556420360dea3663243ccb60676bf06b265045d8896a0ce3c7`  
		Last Modified: Fri, 09 May 2025 17:35:40 GMT  
		Size: 12.1 MB (12072483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aad31017e60189a3fb4896dc1fbb26c66f019e88dacff6bd61827a259215be8`  
		Last Modified: Fri, 09 May 2025 17:35:39 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf41f6797581ca12e0e92cbe2e7531103520deae496a6b556213e1bc39b94d7d`  
		Last Modified: Fri, 09 May 2025 17:35:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224f5c81b378874f265769dcbf83ef686e896083ef3df2e4a71a74341d18f98`  
		Last Modified: Fri, 09 May 2025 17:35:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fca62b2f12dcb7de7c39d9686e729bcf4ebcc9edb87e52f2d125b3cb783a0d`  
		Last Modified: Fri, 09 May 2025 19:55:32 GMT  
		Size: 18.5 MB (18469586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd06e7704af2276112071fa9b2d621c80132e3c1340ba608ad5671e113deb82`  
		Last Modified: Fri, 09 May 2025 19:55:32 GMT  
		Size: 1.0 MB (1049722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f10012d3568d75145292a410707b5739b3e048d58e8b2384e999226bbbebe9`  
		Last Modified: Fri, 09 May 2025 19:55:33 GMT  
		Size: 35.4 MB (35441797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0635fe323a07d88b7dce1fe9dfa168e391ff2ef5d538a266a7b095090a5d95`  
		Last Modified: Fri, 09 May 2025 19:55:31 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bae40e55329a3552d0a14290e6bd586983d0f32393ae1e1099e2676ad972e6`  
		Last Modified: Fri, 09 May 2025 19:55:32 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050080c754de8fadbdeac1e8ed73d8b511f2dc0e960bee1b1837cd8b2f54011b`  
		Last Modified: Fri, 09 May 2025 19:55:33 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85841a652a15a0a3726c053fc8725d2ce28cca3752b9566144202c688aaf0229`  
		Last Modified: Fri, 09 May 2025 19:55:34 GMT  
		Size: 18.6 MB (18606638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed960121ae4a525a8b4ca12088d6f12d9107b027be7b0c9364cbe6c0f5b061d8`  
		Last Modified: Fri, 09 May 2025 19:55:34 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e10b2d98c4f9e69584871c943084d3d5a17ce2364dd1af1452b4f0777d135`  
		Last Modified: Fri, 09 May 2025 19:55:34 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:03417742fbdfa88899a426686823a8010584825f3a54065b00473ee4cd8881b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ad5bbd9099190c025e4804581d7a161d28c9707937663b2490b92bace834fc`

```dockerfile
```

-	Layers:
	-	`sha256:d1e1f7c9b5979ee73eed3018f58c8cdd5d87f78d71fec25a6e8e9623fca0abe5`  
		Last Modified: Fri, 09 May 2025 19:55:31 GMT  
		Size: 64.4 KB (64383 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; s390x

```console
$ docker pull friendica@sha256:9db9f4d94a43e3f3b26e27903a1c7bf1a3d499cf428c1e5bb7e1e4d2e813f7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219104601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba03e298e4e2c42a03fcac01bf1e86569e9e62d3337dbce90c9a1e20d04d33b6`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e64042a8c749f17bfb3b660d34f4e07edd06c81899da76f0b866d5592048d`  
		Last Modified: Wed, 21 May 2025 23:40:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae504c4e6cef239a74e8e2bc8e65a5adfc4fd86d2ce43efcb6fcf7b948f38c6`  
		Last Modified: Wed, 21 May 2025 23:40:18 GMT  
		Size: 80.8 MB (80824650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9845dffb4e53bff01a8cc52346eef48b2a105a195a30ab820e7df1e9682a7a`  
		Last Modified: Wed, 21 May 2025 23:40:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d076bcc60b618a69a01c7cec130e41e98f5d4ef5c1db46cceb7b121173ee5`  
		Last Modified: Wed, 21 May 2025 23:43:58 GMT  
		Size: 19.9 MB (19895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf1bc43a3bf929df811240c21fd8f7c539c8a225d996960c3345d25963bc4c`  
		Last Modified: Wed, 21 May 2025 23:43:58 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aaa5fa23882a5d77ecfeca856eb346385fec09755a18d670b6ceb0cba14cd0`  
		Last Modified: Wed, 21 May 2025 23:43:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ac3cbb3ee52181f5870c40d6ff0a1b3c15f7a493834b7ffa858d4ba114e83`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 12.7 MB (12693285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5a12f32c7ad22ee862dedc750d697163f4baa8ba216508aec32a28c72eadae`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e519b3f987f99a350906f85a83308a333dc3bb83c855c6f8039d2bbe4fecb42`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 10.9 MB (10877513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f03137a91efb211c66885cb4db54cc38a9ce7daae5ace4b12e9fb71e26971`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5738264205b6a2bb25b89a22c01b95a2a2d35399772e753209307f4344d4a007`  
		Last Modified: Wed, 21 May 2025 23:57:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e03f6ec5d1a9cc5916c74caf43667c2dfcfca33467fb0983bc8c665c61b78b`  
		Last Modified: Wed, 21 May 2025 23:57:30 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0055561095a4a555cbeee14288c829d3d006fc617775d56970a9da6fdcac094`  
		Last Modified: Thu, 22 May 2025 05:00:12 GMT  
		Size: 17.7 MB (17658531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb0922cbe9c95108f92ff706810ef253648c43f508b5767b59e4ebabd941a75`  
		Last Modified: Thu, 22 May 2025 05:00:12 GMT  
		Size: 1.1 MB (1091720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc33b21dc5f7b74262d61a20418b37587e692a918c29467525e382e42bfa71a`  
		Last Modified: Thu, 22 May 2025 05:00:13 GMT  
		Size: 31.6 MB (31567722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecbfc14ecb79cdf88770cad165616bf0a5bcfbcb9de62654d523da771b41f98`  
		Last Modified: Thu, 22 May 2025 05:00:12 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c300ba2772ac5e9bf6a3498f605dca1edbf9adef5b30f847ebde0de200a35fa5`  
		Last Modified: Thu, 22 May 2025 05:00:13 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1953388cad91e74cd5190eec539a5e59ffe0a303a00a8f03b1225162c80cc0c9`  
		Last Modified: Thu, 22 May 2025 05:00:13 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0062a876f194163994b2258b08ab3892514ec7db9af7d3ff97f5b364e8964b`  
		Last Modified: Thu, 22 May 2025 05:00:14 GMT  
		Size: 17.6 MB (17601505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aebaa24a1dc1d3ca51a93b4d208cf919dc2b6c7d6c6175884c98a945e7a1943`  
		Last Modified: Thu, 22 May 2025 05:00:14 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bc8abd9936acb47c2ae900b235659e68f151efa47105a1a1d4c14c9947d5be`  
		Last Modified: Thu, 22 May 2025 05:00:14 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:dddc1b8c0a8804c0ca46539d023dba5c8e7accdf2f3281790704fc2c295ff690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e89fecee43caed8c2abfead781f2564c72dd9b90402a677774527dee264472`

```dockerfile
```

-	Layers:
	-	`sha256:4993d6a5a921957fdd8d47ac051d7421e8ea77ad1f7c222c60e47cdebd3d8385`  
		Last Modified: Thu, 22 May 2025 05:00:12 GMT  
		Size: 64.3 KB (64316 bytes)  
		MIME: application/vnd.in-toto+json
