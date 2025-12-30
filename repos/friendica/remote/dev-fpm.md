## `friendica:dev-fpm`

```console
$ docker pull friendica@sha256:dde587fd1d651971c255b5f1f500975a80f226c31222a8258e45af127be5549c
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

### `friendica:dev-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:e60608806587723873f746aa76be2801ae0f8fd00a722a45613d2f72532091b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246883114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b0f6ca846ecb18c36cca7c4ef4e0416065ce02d97552125ba367cca022c157`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:22:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:23:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:29:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:29:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:32:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:32:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:32:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:32:11 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:32:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:32:11 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:32:11 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:32:11 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:30:35 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 01:30:43 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 01:30:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 01:33:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 01:33:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 01:33:18 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 01:33:18 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 30 Dec 2025 01:33:18 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 01:33:18 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 01:33:18 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 01:33:18 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 01:33:18 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 01:33:18 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 01:33:22 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 01:33:22 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 01:33:22 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 01:33:22 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 01:33:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a398ec6c8aa683c2830e9b885258297802776d1043000eaac2cba9f075384a`  
		Last Modified: Mon, 29 Dec 2025 23:26:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06ab08db9626138711bbe15b20e7e68435804f141c6a148a3aabc9c745bb861`  
		Last Modified: Mon, 29 Dec 2025 23:26:36 GMT  
		Size: 104.3 MB (104330506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8e6d8a7bca60c50671aaabbac1ff4054b309012a16ab39e66dfc8e547c165b`  
		Last Modified: Mon, 29 Dec 2025 23:26:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cafc9da57040a65dcd34869a601a00c778214749002332dbb3bdb7fe42ba665`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 12.7 MB (12711809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7adf5d0d96ceed0e2168e4200f792a59fc62703660a0cb3bd2628b2daa7562a`  
		Last Modified: Mon, 29 Dec 2025 23:32:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6aa6c685d191fb4f282b57d1bf66bbed284fea205cbb309f98d9485e9164c7`  
		Last Modified: Mon, 29 Dec 2025 23:32:33 GMT  
		Size: 27.8 MB (27839459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1efc3bd84a917eade1b753b41d00dbf7b3e19fb8549a5583c9d664274dd53`  
		Last Modified: Mon, 29 Dec 2025 23:32:30 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cc1abea61728a9946e31cbc992f1ad036f2ab2ff6863c0370ad0fb83ec1309`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292c3f992ca55f8d47857eb16faefe0035d3379244ae0984f0aac58889f1c3c`  
		Last Modified: Mon, 29 Dec 2025 23:32:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b324ad1742cda0a963c26ee8a802e471dc19d709cbf84b670754c64315d41cca`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ed3d32b59dca4d6e71d26718b8772531232025bf64683d1e9ffe0eed8cc9c8`  
		Last Modified: Tue, 30 Dec 2025 01:33:43 GMT  
		Size: 18.4 MB (18436435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afec064b7cdf9ead728de9b66c2be38ac54ecb720b36e8f748c435eb3491249`  
		Last Modified: Tue, 30 Dec 2025 01:33:41 GMT  
		Size: 1.1 MB (1104015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be09d379962bc4a08eb2759f779ed645c4cff9ce47a473b14492ec47c917f7`  
		Last Modified: Tue, 30 Dec 2025 01:33:45 GMT  
		Size: 35.8 MB (35846190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c85b6b59d0c1037cddfcb56d17c3180393e928f7d5fc7e421601eba1adef09`  
		Last Modified: Tue, 30 Dec 2025 01:33:41 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e6b0d6c9bf6b68b8755221e73b13323231ad9b4a168d1609f9504171bb8c2`  
		Last Modified: Tue, 30 Dec 2025 01:33:41 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ebc30141474d4b2f1a1fbfaf2fb8691a0defee2b1e2ea07a7b1eb361c0ef63`  
		Last Modified: Tue, 30 Dec 2025 01:33:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2514b3cde7df10142155b0d84ed0fd5be35b412d1070f6b79fd41dbcbe956b9`  
		Last Modified: Tue, 30 Dec 2025 01:33:43 GMT  
		Size: 18.4 MB (18367147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37f2061e333fbbad41ecfdb4b4ef7f18cb09f220bce74a708addf790cc27cb`  
		Last Modified: Tue, 30 Dec 2025 01:33:41 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479733362335ebdb739dd6ce7ff35054dd0b3d0f1867846eccfe08d9ef34c137`  
		Last Modified: Tue, 30 Dec 2025 01:33:42 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:1b567edef3f694195f9898a158edf9789df3a2e7ee3b382112ec9338e6a6038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f55afdc54b02407dd50c5355830c71788512a53964f052ee5178a842c54007`

```dockerfile
```

-	Layers:
	-	`sha256:731c20795c796cd853d567cad47307a179b04ef4f9d6ed865dc8b046c794bcae`  
		Last Modified: Tue, 30 Dec 2025 06:28:24 GMT  
		Size: 59.1 KB (59146 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:f790a23d840fe1a4fdcf087945333cda3f23461282eea0ffb3e10f5ec1d6bf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216174187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdac88ef0889fd55c84f1674ec6d7311ff7f54c509f43c208b54b43b1be3d622`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:31:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:32:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:32:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:32:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:32:12 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:40:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:40:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:42:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:42:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:42:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:42:44 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:42:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:42:44 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:42:44 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:42:44 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:51:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 01:51:20 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 01:51:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 01:54:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:54:10 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 01:54:10 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 01:54:10 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 01:54:10 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 30 Dec 2025 01:54:11 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 01:54:11 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 01:54:11 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 01:54:11 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 01:54:11 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 01:54:11 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 01:54:17 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 01:54:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 01:54:17 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 01:54:17 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 01:54:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea6dec140229ee6f56cd4c3bc31a5a4aca33c2b1756caeb88412f512897943b`  
		Last Modified: Mon, 29 Dec 2025 23:35:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9355988adfc5efea2d60214cbd51da763e86e46cd53ef1f1544ba1344b2864`  
		Last Modified: Mon, 29 Dec 2025 23:35:35 GMT  
		Size: 82.0 MB (81981445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578f6744d1d408cefeefdc63704f79a3db090310302bcf27c5816ca95afe7131`  
		Last Modified: Mon, 29 Dec 2025 23:35:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705e372b619e178ab0fe3c059989f86840767b0b87d226cfe7a08d5dc4e0a1dc`  
		Last Modified: Mon, 29 Dec 2025 23:43:06 GMT  
		Size: 12.7 MB (12710194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db6b7c01e761b1b32f2b83b6575ab355edb7b40e5f7cf25c716beede6d0c0cf`  
		Last Modified: Mon, 29 Dec 2025 23:43:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c70ec0f8fc0ae4e21d02e23250c3eeaeb513542949cd54b0d27494dceba6`  
		Last Modified: Mon, 29 Dec 2025 23:43:06 GMT  
		Size: 26.3 MB (26318951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35864d62015de1300636fabfbde325722c9bd7f2fe6924c9c7dcb9f3fd2728ef`  
		Last Modified: Mon, 29 Dec 2025 23:43:04 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449dfc5865314b61b067ec91dcb93ece9871b14782c0c7b1b0d1948613c883ca`  
		Last Modified: Mon, 29 Dec 2025 23:43:03 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4135f5db04643eb93667262dadb962b59636a59c7e8541651b9285e25b7ae1f0`  
		Last Modified: Mon, 29 Dec 2025 23:43:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d188752e5dcda704a126290fb21eef4a24f6144b73c71a2a6b041a3c487773f5`  
		Last Modified: Mon, 29 Dec 2025 23:43:03 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405229597a7241acb6aed9dd2b9de7479a98c44fc4f6dc256ae9be964b440b8`  
		Last Modified: Tue, 30 Dec 2025 01:54:42 GMT  
		Size: 18.2 MB (18173292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca667aaf396100f3c86964cb06c5ab1075c750d11e483a5bd792c5d99f8845f`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 1.1 MB (1079397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9ed21e5b3fd45ab2ffeb1cfdf402f13390c6dc50f460d9530cd063d2d85146`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 32.0 MB (32042745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77533e56d3630942ef35cb2538ec364b0990b70c31adb6532954fd0b64fc1ebb`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d21dbe6d842e1446f604f917a99987ad58598542685263488170cf5d009c7a`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aba9b2460a2fa9d8b869faa66d946bae6c871e738bdadb1473dc5a8a85216b6`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77584c72964d892a933383df087a8e107614f77fb143688efa7b095cc861ade`  
		Last Modified: Tue, 30 Dec 2025 01:54:34 GMT  
		Size: 18.1 MB (18091450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206af7e6693fd7b7447bfefe58f770f57a4c97bff49ca0e150043dbd73290f9c`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6209f2054727d3bc167548c4b897eb4f75275132eebb6bb91bbaab15eccb1efe`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:c4aa8792808eb2298ff8f694d5a550067de5db72a685823dcd79f9b94765775c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38e4ce1817157ffc02ce04b7c55d2b249a1a430baf2396c05f21da4ab351e35`

```dockerfile
```

-	Layers:
	-	`sha256:7b4d972dc24e93a4f71ff482ecaf12ac717229ffd7aaa986d628a83de005b3ac`  
		Last Modified: Tue, 30 Dec 2025 03:30:09 GMT  
		Size: 59.3 KB (59278 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:657e8baf7c82508dad387c16927e392e85b17e3cb9dd0ddb6fd0135bd3a4bedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205598862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35b3603ccaa453154b2030c8aba5846535f12cb05906ea7799294d61b44a0d0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:41:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:41:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:41:16 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:41:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:41:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:43:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:43:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:43:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:43:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:43:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:43:56 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:43:56 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:43:56 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 02:11:46 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 02:11:56 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 02:11:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 02:14:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:14:35 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 02:14:35 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 02:14:35 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 02:14:35 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 30 Dec 2025 02:14:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 02:14:36 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 02:14:36 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 02:14:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 02:14:36 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 02:14:36 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 02:14:41 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 02:14:41 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 02:14:41 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 02:14:41 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 02:14:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d161ab1908d98523684a5f2e2a810ccd6af2ad00fb32bd0cc6cb8e9a486bb4`  
		Last Modified: Mon, 29 Dec 2025 23:44:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709cbb7ecf7f29843b95bb2ece97cd2dfa11b00e615e5a60dba120229890fef`  
		Last Modified: Mon, 29 Dec 2025 23:44:29 GMT  
		Size: 76.1 MB (76148759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e94e95825d4a7bbc8295a9396b1d824c31d7133cb645b223b2c93d146e72f`  
		Last Modified: Mon, 29 Dec 2025 23:44:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e56afc59d3a4f33863448029a040bcd8da0fecfa654526836a0f4e08a8592c`  
		Last Modified: Mon, 29 Dec 2025 23:44:25 GMT  
		Size: 12.7 MB (12710125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082b5851f0a716c77f3b53a5174ae667c3b101f2b4e85091b84294534077c5f4`  
		Last Modified: Mon, 29 Dec 2025 23:44:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2894ab0e34d9f7d0a8948d1157659ce651a7de24619af978fba4093cb6e73014`  
		Last Modified: Mon, 29 Dec 2025 23:44:26 GMT  
		Size: 25.4 MB (25416982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb54ed5fd802463fb1f5f007a5ae6c1009721a0743f5232fe3486b74769fdeb6`  
		Last Modified: Mon, 29 Dec 2025 23:44:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad947bd8f3a2005e14fd51c401dec552ea2387e160ecd97e7010c1df0c221d8`  
		Last Modified: Mon, 29 Dec 2025 23:44:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46764a801dd981f6a467b32d72bb72071555a552b14a86539a05703bae9a493d`  
		Last Modified: Mon, 29 Dec 2025 23:44:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17098eae104445a1c67650894e9a855e48c8c9a3c5f57914b1bf2990d6edd024`  
		Last Modified: Mon, 29 Dec 2025 23:44:24 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99cd9fa2f5836e51112941289dfc4968e1ad34000beb5cb891eeeed5cdc7d0f`  
		Last Modified: Tue, 30 Dec 2025 02:14:57 GMT  
		Size: 18.1 MB (18073960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6de1dba894e1fe2256263bf168be08d6530a289158cf31491bd9a410675c886`  
		Last Modified: Tue, 30 Dec 2025 02:14:56 GMT  
		Size: 1.1 MB (1070058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d80711d738a4a92debcfce30449cb34652fcd12f7daa4a0b44b37e157e9241f`  
		Last Modified: Tue, 30 Dec 2025 02:14:59 GMT  
		Size: 30.3 MB (30299513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25ccee1d79a35a522d0b6545eb7fb6409b41b5d1c40b9816370a221d9f59cb`  
		Last Modified: Tue, 30 Dec 2025 02:14:57 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac300629616400e48cb91abce9c10414cc5f76546886b6ea095850fcb9b65cd`  
		Last Modified: Tue, 30 Dec 2025 02:14:57 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7519b54d66ed1d7f36802c0a7b55af39f614b8073f098b682979694920f47`  
		Last Modified: Tue, 30 Dec 2025 02:14:57 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb744c6a99c33fccc41ad442ca51f17cc7d1293eb1a7dd82ed72bdc77502edc8`  
		Last Modified: Tue, 30 Dec 2025 02:14:59 GMT  
		Size: 17.9 MB (17926285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad971dbba0bef48b7cb662831a653d361570e04c4d54da9164b2113f1dddc6`  
		Last Modified: Tue, 30 Dec 2025 02:14:57 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15f9154e6e9b323b20cc191d0dea178bf1de5fe6fbb9308984d131a49ce352`  
		Last Modified: Tue, 30 Dec 2025 02:14:57 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:d80356f7b3cd73e2fdf2b3b9e9733429d551fb409c27711da7a30befa03defe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d11ac5dcfb0cceeb7806109f72e58b8b359c8f7f93a992d01a85eb635c10900`

```dockerfile
```

-	Layers:
	-	`sha256:84e23c5bf640fb6bc5f81bc5530cf896e3f266bd5f1dd0cb23add5f1f96ea213`  
		Last Modified: Tue, 30 Dec 2025 03:30:12 GMT  
		Size: 59.3 KB (59278 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:72e57db6bd560cb4d6dd58eb4a45e68afdb5d75ee3a55ca10a5bb008d122172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237948852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f376d74949bf6d42395f763e3bd73ccb856498f2afd2fc4197b1c6c7f55552a1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:23:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:23:09 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:31:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:34:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:34:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:34:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:34:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:34:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:34:38 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:34:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:34:39 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:34:39 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:34:39 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:32:26 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 01:32:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 01:35:53 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:35:53 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 01:35:53 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 01:35:53 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 01:35:53 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 30 Dec 2025 01:35:53 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 01:35:53 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 01:35:53 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 01:35:53 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 01:35:53 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 01:35:53 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 01:35:57 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 01:35:57 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 01:35:57 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 01:35:57 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 01:35:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10ae782f240a11405e82545200391c3ba0dcb5411728997afb9fdcc2a973534`  
		Last Modified: Mon, 29 Dec 2025 23:26:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38f6f1ea5c4eddd40b241f4afb4d5bd6035d638842d3f0e78ad70f478f4d9e4`  
		Last Modified: Mon, 29 Dec 2025 23:26:59 GMT  
		Size: 98.2 MB (98165909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd4ef5aac020f35e4a1a1c1c0353ce00728bcbe0adb1ab78574c8abd6e25b4b`  
		Last Modified: Mon, 29 Dec 2025 23:26:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c7ee53305bd6e505651907fac3a9dfd565285c465b655b8055b9693c530aea`  
		Last Modified: Mon, 29 Dec 2025 23:35:00 GMT  
		Size: 12.7 MB (12711557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6baf2e77675a10155b28e44f170e94c50a8face023aee666d49707f51dbc10`  
		Last Modified: Mon, 29 Dec 2025 23:34:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3641d3eab70794345026b7e8597548b4e63565bf5a401da2c8a686ce7fc255`  
		Last Modified: Mon, 29 Dec 2025 23:35:01 GMT  
		Size: 27.8 MB (27834080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046adbd94182d54cfb3db8bd67c57b7e8f0f385a3c9c9a99d7fed1f8c636f383`  
		Last Modified: Mon, 29 Dec 2025 23:34:59 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cbc3a32585f3277bd88d0da08e828462a2db44334638ba0ad1dfae1e27dda0`  
		Last Modified: Mon, 29 Dec 2025 23:34:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febad47c69ce4f5a78e3ffadd330aa4a4baf4388e6ca082ff288e57a86e051a9`  
		Last Modified: Mon, 29 Dec 2025 23:34:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbbe00ee4d1e6bbd9ac146efc288e42572d4a440c60ccf2117a1bab2bf6f3d9`  
		Last Modified: Mon, 29 Dec 2025 23:34:59 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553b277ed8e5104bd37ef4375082269ce86b6daf2872e6f9661b49aab466ab9`  
		Last Modified: Tue, 30 Dec 2025 01:36:17 GMT  
		Size: 18.2 MB (18228057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e894c8ff2c945b40cfdeea11e1ceede617b54e8a2312da16d30c4e5483fe2b27`  
		Last Modified: Tue, 30 Dec 2025 01:36:13 GMT  
		Size: 1.0 MB (1036234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32a9122a5a780d51f73313cb6753e1821186e3558e2f8934862c2ee3b7b5cb5`  
		Last Modified: Tue, 30 Dec 2025 01:36:15 GMT  
		Size: 33.7 MB (33668811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a51633bca73488e782a4dd6b5712a573759b3b5dbc0e41c67165572520386f`  
		Last Modified: Tue, 30 Dec 2025 01:36:13 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c4669723b76b67b392c48c802dd3c252bbf8716d6c24f2a504f024ea62445`  
		Last Modified: Tue, 30 Dec 2025 01:36:13 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e806d96a8026e1cbae288498777b8acf257f9fd074c2bc952a84737e9019b2b`  
		Last Modified: Tue, 30 Dec 2025 01:36:13 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267f3c60c089b2cf543457ab895d22aa74c826557ddb2bd85377d654736b8c15`  
		Last Modified: Tue, 30 Dec 2025 01:36:16 GMT  
		Size: 18.2 MB (18182879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf46a92dec11ee7a1cfbec9a3f54779da50b068fff52177e76fafbb24901c3`  
		Last Modified: Tue, 30 Dec 2025 01:36:13 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7759719467ca2d165773efcbf592dd12f99da465729159ea698246982009f537`  
		Last Modified: Tue, 30 Dec 2025 01:36:13 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:a8a3a01d1338f22b9231019a42614573ef5d90dee5ab14e1d82bfd736d85cf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae97e54fccc1867b196e02f5d40bf27c0ae8285413a3776c19eddfec4a9086e`

```dockerfile
```

-	Layers:
	-	`sha256:a2a0a8dafffe219cb0895be570eed1530262928d46bba7f61cd1ab11a2eeb9fa`  
		Last Modified: Tue, 30 Dec 2025 06:28:30 GMT  
		Size: 59.3 KB (59306 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; 386

```console
$ docker pull friendica@sha256:c6cf30da7d9efb9c9e07d62797da58e7af20f561057c104469bf91296e013d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246047835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4d865e82cdf1c776a9f36a8aa229e7eda30620509d50e5ce5ed2f94e6fbedf`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:17:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:17:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:17:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:17:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:17:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:17:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:17:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:17:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:17:49 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:17:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:17:49 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:25:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:25:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:28:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:28:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:28:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:28:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:28:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:28:25 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:28:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:28:25 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:28:25 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:28:25 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 00:50:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 00:50:56 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 00:50:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:53:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:53:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 00:53:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 00:53:28 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 00:53:28 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 30 Dec 2025 00:53:28 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 00:53:28 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 00:53:28 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 00:53:28 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 00:53:28 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 00:53:28 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 00:53:32 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 00:53:32 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 00:53:32 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 00:53:32 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 00:53:32 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ba82b769ce8f2598a27836934f42c7870c1d5fa1bf472eae4b39f543e138f7`  
		Last Modified: Mon, 29 Dec 2025 23:21:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0042a4bea87de0aeceec4e800bf42c23a6edaf4b7d1aba766731d7554890ca7e`  
		Last Modified: Mon, 29 Dec 2025 23:21:26 GMT  
		Size: 101.5 MB (101518693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af498eac6a140eb77f4801ab71e5d362131da78363384e6e831ce47f41efc43d`  
		Last Modified: Mon, 29 Dec 2025 23:21:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701f232587520110a633344be493b65f2641236cbb6722c12fe182b578efc178`  
		Last Modified: Mon, 29 Dec 2025 23:28:44 GMT  
		Size: 12.7 MB (12711107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b09075cec57a9fd93d0455a29ac5bf873d1e015e67c55a60cba992fddc579a1`  
		Last Modified: Mon, 29 Dec 2025 23:28:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ac2d8740aec27f33b5a0e6c298e2f60755464ef2532972ac6896ea0bc9389b`  
		Last Modified: Mon, 29 Dec 2025 23:28:45 GMT  
		Size: 28.3 MB (28349751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72273ca1d84b4977bf5217b24cdb1dc8f500a40c76b37e0247bb8a9603bbbb5f`  
		Last Modified: Mon, 29 Dec 2025 23:28:42 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0619ab19dc114a1f215459fc5c0b45e1793100a88010a2fd5a70e3cc7419908`  
		Last Modified: Mon, 29 Dec 2025 23:28:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e4e8f1a921cb9d785d11e1c6f27b15c8b7c624da5579f9276e042fe8f70ed`  
		Last Modified: Mon, 29 Dec 2025 23:28:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2871f4e116c231a04d3dad5c7d11b44733ecbed54bdd730564ee00fb7ac67231`  
		Last Modified: Mon, 29 Dec 2025 23:28:42 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8ee79f54e3b7a42435b655a6d2d457fbd6ceac5c4b5ec709abd699b550c6b8`  
		Last Modified: Tue, 30 Dec 2025 00:53:51 GMT  
		Size: 19.0 MB (18959377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c9a829ac378ee58a5670b1f46c8f1e925bb91f3ed58f387a039511791c9a20`  
		Last Modified: Tue, 30 Dec 2025 00:53:50 GMT  
		Size: 1.1 MB (1078936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20010dc97b9ce548e40c335e61e124e6eb4776fdbc84a2730c09d9d60092471d`  
		Last Modified: Tue, 30 Dec 2025 00:53:54 GMT  
		Size: 35.2 MB (35161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e7842ef2bb3f6fdf7c02ac795be83a6fa067c20f9a33d8e8d7377e54102535`  
		Last Modified: Tue, 30 Dec 2025 00:53:51 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc3a27348638a169d1189153ec2fb5666b179f7af4cae4aecc35fc3440ed751`  
		Last Modified: Tue, 30 Dec 2025 00:53:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ac69ab6f9a5b38ba22b82cbd3f8b609a347949de2c184504d63d0f8dc4bb6`  
		Last Modified: Tue, 30 Dec 2025 00:53:50 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5500fa5517508e397c16a0341c4561f8cfe09b40407dd5c5047f0347411411a`  
		Last Modified: Tue, 30 Dec 2025 00:53:51 GMT  
		Size: 19.0 MB (19039603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c7754ec0a5d067e2d85575d0ee46471615f389bf4c114cbec891d7cd13d2b9`  
		Last Modified: Tue, 30 Dec 2025 00:53:50 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f0a6a9f7d3b596dd4a9eb2377926c9f097b483acdf7e236c843d151a01c08a`  
		Last Modified: Tue, 30 Dec 2025 00:53:50 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:8ed838c77242b35130760dc1d868669eb0e3cc3d86d22e04c5ec6a8e58b5202a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3dc567bd2641e7893c8dfba0b8563ed9d7c9d1d9c44c5da6db662b18a2fa85`

```dockerfile
```

-	Layers:
	-	`sha256:6e79b0e9f24523f3ab81e300ed392ce96b428bbdff59c139602ae490d7e66991`  
		Last Modified: Tue, 30 Dec 2025 03:30:17 GMT  
		Size: 59.1 KB (59112 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:478d0334d0dc93c65944fe422acc0cdfb966fb134d4ba7ac561402d8bd83b331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218340442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844dc2d575ba0aaba984ec9e0f82f0401b479ebfb0f040fbf83182aa505b6c35`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:57:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:58:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:58:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:58:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:58:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:58:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:58:58 GMT
ENV PHP_VERSION=8.3.29
# Mon, 08 Dec 2025 22:58:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 08 Dec 2025 22:58:58 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 22:27:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Dec 2025 22:27:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 23:17:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:17:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 23:17:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 23:17:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 23:17:11 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 23:17:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 23:17:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 23:17:13 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 23:17:13 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 00:59:42 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 19 Dec 2025 01:00:29 GMT
ENV GOSU_VERSION=1.17
# Fri, 19 Dec 2025 01:00:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 01:12:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 01:12:19 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 19 Dec 2025 01:12:19 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 19 Dec 2025 01:12:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 19 Dec 2025 01:12:23 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 19 Dec 2025 01:12:25 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 19 Dec 2025 01:12:25 GMT
VOLUME [/var/www/html]
# Fri, 19 Dec 2025 01:12:25 GMT
VOLUME [/var/www/data]
# Fri, 19 Dec 2025 01:12:25 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 19 Dec 2025 01:12:25 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 19 Dec 2025 01:12:25 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 19 Dec 2025 01:13:51 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 19 Dec 2025 01:13:53 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 19 Dec 2025 01:13:54 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 19 Dec 2025 01:13:54 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 19 Dec 2025 01:13:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2b054f3a77e8800c8f5fad5ed6594164acd9d6bbb1409af308aa485c7352cac`  
		Last Modified: Mon, 08 Dec 2025 22:15:08 GMT  
		Size: 28.5 MB (28513802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b325838704c44035c60a08caf80202da7e9b6014f2bc2ada325b353544b883e6`  
		Last Modified: Mon, 08 Dec 2025 23:18:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5777a625bb292a0da02d9d422a88d1939e4397bf228fbeb2fefc860d82b39ead`  
		Last Modified: Mon, 08 Dec 2025 23:18:56 GMT  
		Size: 80.7 MB (80670348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a6818d96f3e882078231f351e16d6777780caafed08b42f77f31972ace97d9`  
		Last Modified: Mon, 08 Dec 2025 23:18:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be958d9e51247a97da4412d95af04846fd109a82ce2d205438f02caa8d6f2b9`  
		Last Modified: Fri, 19 Dec 2025 00:20:03 GMT  
		Size: 12.7 MB (12709953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9abaf667fe31d052360082c82a608a8d1cdf170c0669b0cd6912b9c2df1ba2`  
		Last Modified: Thu, 18 Dec 2025 22:44:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93bcb10e81ab64a766fe7e7116db38719ce3cff6ba62ae6d8188d0ed7bdb6d`  
		Last Modified: Thu, 18 Dec 2025 23:18:14 GMT  
		Size: 26.9 MB (26932766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b1ee660a6fd7ca5cca1d3b3716d80fd5a7d346aaeec6d551c3fe5aa71ab450`  
		Last Modified: Thu, 18 Dec 2025 23:18:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586d1e7a585e49f4cc08f35d1e1f5c48dc48a3c2cf3c94d5939d5b38de9ce5aa`  
		Last Modified: Thu, 18 Dec 2025 23:18:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9399bbc91fa9e194f8f18d2f5d6ec0b6df112cc2700af835694bbf855c212dfa`  
		Last Modified: Thu, 18 Dec 2025 23:18:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3f43db001f6f23ddfddc97d0ddc81c44a79a6f26d239b5c81722fb0e45cd33`  
		Last Modified: Thu, 18 Dec 2025 23:18:12 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ba910a4d32417de97372ae852149f3fdb46ec2414dad4f43c02a1f72af60a`  
		Last Modified: Fri, 19 Dec 2025 01:15:16 GMT  
		Size: 17.7 MB (17715222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99f54ff4f82b0322181924ebb6666e7eede6323a0856bdfeaf74e8ad813f619`  
		Last Modified: Fri, 19 Dec 2025 01:15:15 GMT  
		Size: 989.6 KB (989573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a0117b81c573f22d610904d47a5fc7684f4b4207c6e15ad46b55ce81156a6`  
		Last Modified: Fri, 19 Dec 2025 01:15:17 GMT  
		Size: 32.9 MB (32912526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8caf4f15619fa18dd4102f36ff75e1f7ac593c74c977139754759810ade617`  
		Last Modified: Fri, 19 Dec 2025 01:15:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed25a915c9b0f1534aa36040bb8ecbcd3d3864e21803c185be26c4ad3880d015`  
		Last Modified: Fri, 19 Dec 2025 01:15:14 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c452872650a259598159bd047025c405b7b82ef8adf10b1aa533405428d5e00`  
		Last Modified: Fri, 19 Dec 2025 01:15:15 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f55fdafae130b9a6d98839e844670fbe628edda804b5db478592d4a48503456`  
		Last Modified: Fri, 19 Dec 2025 01:15:16 GMT  
		Size: 17.9 MB (17877128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3181131cd26cfe7ddba2cbf7f8a40b15b573a96aa3cf10b93f879e2eebb5b06`  
		Last Modified: Fri, 19 Dec 2025 01:15:14 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259a6f488957af616b087f001dd9a580a5d27d65e23c8855e164a38bd391b7e`  
		Last Modified: Fri, 19 Dec 2025 01:15:14 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:faf37837c915f5705ad1247919418f264a8b409b8075f8530615be186e6533d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4194496dae31e55266dfd7a809d355248d62b821092edf1b3517183fb508919`

```dockerfile
```

-	Layers:
	-	`sha256:c1c2e123d566b2e5fc05956092745fe2cc54aa01d537b2bebe2d5fb47b79b18b`  
		Last Modified: Fri, 19 Dec 2025 03:27:49 GMT  
		Size: 59.2 KB (59193 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:9d747713e5b535f101459a86a695e3bc9c463d20a829d9d44aaeb67f32cf56be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251081317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fb83b0f5ae5d3f7872d410c56e43c6d28e8a3657763bc4b06aee78f0c8a19a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 12:44:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 12:45:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 12:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:45:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 12:45:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 12:45:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_VERSION=8.3.29
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 21:53:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Dec 2025 21:53:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:00:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 22:00:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:00:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 22:00:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 22:00:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 22:00:55 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 22:00:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Dec 2025 22:00:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 22:00:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Dec 2025 22:00:55 GMT
CMD ["php-fpm"]
# Thu, 18 Dec 2025 22:45:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 18 Dec 2025 22:45:51 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Dec 2025 22:45:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:51:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 22:51:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Dec 2025 22:51:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Dec 2025 22:51:31 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 18 Dec 2025 22:51:32 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 18 Dec 2025 22:51:32 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 18 Dec 2025 22:51:32 GMT
VOLUME [/var/www/html]
# Thu, 18 Dec 2025 22:51:32 GMT
VOLUME [/var/www/data]
# Thu, 18 Dec 2025 22:51:32 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 18 Dec 2025 22:51:32 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 18 Dec 2025 22:51:32 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 18 Dec 2025 22:53:15 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 18 Dec 2025 22:53:15 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 18 Dec 2025 22:53:16 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 18 Dec 2025 22:53:16 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 18 Dec 2025 22:53:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7fbfa9a935f96015448b226c612416546538a1dcc52e55d20077b60dc138df`  
		Last Modified: Tue, 09 Dec 2025 12:51:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb33d06e000eb34d612247e4138286d5e898db5da65f963214e6d898b0fcd65`  
		Last Modified: Tue, 09 Dec 2025 12:51:17 GMT  
		Size: 103.3 MB (103329018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e40fa0c3ff80077d169fd45b8fbcf082c8de27581241e80d2c54a3edd2591a4`  
		Last Modified: Tue, 09 Dec 2025 12:51:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed42bffb6c56c1ca7d03571e625950980391bd0ca58d47cf0c374357167906b9`  
		Last Modified: Thu, 18 Dec 2025 21:57:38 GMT  
		Size: 12.7 MB (12711395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceb3abdb312fb88bf9d88fdfc258b2dc6394a78a9c752997da76c256769b81a`  
		Last Modified: Thu, 18 Dec 2025 21:57:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123c7656c69ae6f707a055d87bd44c36379d6beacfcf5852ab37b69707edfe7a`  
		Last Modified: Thu, 18 Dec 2025 22:01:34 GMT  
		Size: 28.9 MB (28907162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42c49e7cb58e2a703e42b800438484b1918e41a737ff54af5ec5109da98b761`  
		Last Modified: Thu, 18 Dec 2025 22:01:29 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9f40a86640bd414020c6f5baceb80b5bd82ac04bae3909ca6f73155b5342d`  
		Last Modified: Thu, 18 Dec 2025 22:01:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508a56399147d9b0c3b9039a6bb2f330e192cbf3ca0c917afae9c714f27565d7`  
		Last Modified: Thu, 18 Dec 2025 22:01:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729972326ecdbf01d288b7f8ba4c40ad3090ace26ccaf2a4faa913ba8ac46242`  
		Last Modified: Thu, 18 Dec 2025 22:01:29 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a617321a65c6313c9d2bec3eccd0b2ba9c8df2323e4333ac7d4e7d0561208e0`  
		Last Modified: Thu, 18 Dec 2025 22:53:47 GMT  
		Size: 18.6 MB (18555070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7509a15408e6340eb889e2723a9b63230f3d755ac36d2daeb7c360965dd1789d`  
		Last Modified: Thu, 18 Dec 2025 22:53:45 GMT  
		Size: 1.0 MB (1026342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3984682d4ee130e0b09c06d3de96faab7232e2591d109f3709bf5dc5d65f5a0`  
		Last Modified: Thu, 18 Dec 2025 22:53:47 GMT  
		Size: 35.8 MB (35815027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04aa00989ec0f1f99ed3d473c1c93142457ca328df070d79a4ab3121ef5839a1`  
		Last Modified: Thu, 18 Dec 2025 22:53:46 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd0e4032bf987701b553612e9f730c031d61bdfe41cb1eb55aa54c690f59c2a`  
		Last Modified: Thu, 18 Dec 2025 22:53:45 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891c705bb569c992233e2a957ae8f985ad83ed6501c1868d3521960c5b0045d5`  
		Last Modified: Thu, 18 Dec 2025 22:53:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd576d46301fa21745b7c26e1ced5c0b4584b4c14c87f47d3ff8f9d9f26770c`  
		Last Modified: Thu, 18 Dec 2025 22:53:46 GMT  
		Size: 18.6 MB (18649312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee7c1c41b113f3a6dc525ea38a78c4ba8dcfcd9d4819cceba6cc73e6ec1b485`  
		Last Modified: Thu, 18 Dec 2025 22:53:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61389d809d7924a18d7c5c16cef5567179a474409c681169cfe05d0f5bfacac5`  
		Last Modified: Thu, 18 Dec 2025 22:53:45 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:e283523231cf73ffc211bf2c3a65e19ce05cea7dc19cd5b6db023501b8597588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041ad571b9d809163824759491e8979a00a91e67cf762fa6206a885ed292f863`

```dockerfile
```

-	Layers:
	-	`sha256:c3e7575eba4a4e38f2c59dc2af78ac09a758c4eb9c5ae36d0e7a825c45f951f4`  
		Last Modified: Fri, 19 Dec 2025 00:29:22 GMT  
		Size: 59.2 KB (59190 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:a4fff4af73ae8e60ba4175e496b7e22e8d647a772bfcb0241bfaab88782c03c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215690663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bafa2a9061f7b5c8a0b5f99b5cdf752867b9e228b66050f746826dc66cf4ee7`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:24:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:24:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:24:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:46:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:46:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:48:45 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:48:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:48:45 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:48:45 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 02:32:06 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 02:32:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 02:32:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 02:34:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:34:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 02:34:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 02:34:16 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 02:34:16 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 30 Dec 2025 02:34:16 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 02:34:16 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 02:34:16 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 02:34:16 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 02:34:16 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 02:34:16 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 02:34:20 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 02:34:20 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 02:34:20 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 02:34:20 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 02:34:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb418c0e5abcefe16acbc6e83182df41a4844e89a661b7628f7b0852127c87`  
		Last Modified: Mon, 29 Dec 2025 23:28:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbed6618c1961e2a7b7cf2c87e46f37dd87a16548388c42e37807bf2ce70d12`  
		Last Modified: Mon, 29 Dec 2025 23:28:46 GMT  
		Size: 80.8 MB (80826406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdd0c0b33812eb4b7f25ae54473174aebd54cf322e1c27b866650bf4f1c6dc`  
		Last Modified: Mon, 29 Dec 2025 23:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5454c79ab339175b1e58b7aba039432a6e3cde6912e90dbdfb0a2aae5b5d4c`  
		Last Modified: Mon, 29 Dec 2025 23:49:08 GMT  
		Size: 12.7 MB (12710517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30329d3e70509a056a87e2121403cdd0e13204ddbb034c23a0272ecf1cf536`  
		Last Modified: Mon, 29 Dec 2025 23:49:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ca58aa48508a3140ec92017cff0598612e6519e69a41d95f1f4625183f38c0`  
		Last Modified: Mon, 29 Dec 2025 23:49:10 GMT  
		Size: 26.9 MB (26939726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5fece17d15a77447978abcba28c7ed3a2bbc73e93e6d812d70d9bea22abd78`  
		Last Modified: Mon, 29 Dec 2025 23:49:07 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0720dbe134174aac35c7d5ffa1ccae6b433ec81aafb97d40c7e6c79339c86fa`  
		Last Modified: Mon, 29 Dec 2025 23:49:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333ff4ec07125a8c39a6891863ab8f9e9623341a1b7ce746a353326053b234f`  
		Last Modified: Mon, 29 Dec 2025 23:49:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221505cc3f6e78a4c11a66485529e2778e6ab85da887c369d04c27f3e0b096da`  
		Last Modified: Mon, 29 Dec 2025 23:49:07 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bd28c43ccde1448be572fb548f72ab753b60b3426d2b75759435b694ac4318`  
		Last Modified: Tue, 30 Dec 2025 02:34:40 GMT  
		Size: 17.7 MB (17713636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f70a7cb0fa942f810f2ad31ddcedfda73c0328e12f130865041accf56a789f`  
		Last Modified: Tue, 30 Dec 2025 02:34:38 GMT  
		Size: 1.1 MB (1068481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301932d508c935bb81bed89da31457c881cffc3935c6fdbc71310a9bbdc108d8`  
		Last Modified: Tue, 30 Dec 2025 02:34:41 GMT  
		Size: 31.9 MB (31885318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca9af4341187a1d8403ad26e2363a8e9a326620e83245a16a6739b0a0142363`  
		Last Modified: Tue, 30 Dec 2025 02:34:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880bbda3d1261f84bed2cad18f0a73646edc623fd349c0312b8e901c37db0b29`  
		Last Modified: Tue, 30 Dec 2025 02:34:38 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ad674cc402154bae1f0898357068b62eff8fc6d021c57ddf25c56da471a677`  
		Last Modified: Tue, 30 Dec 2025 02:34:38 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77976df82a73e1663cf7d7c8afb13a39a3b1099bf17902ede30adcb096d1d31`  
		Last Modified: Tue, 30 Dec 2025 02:34:41 GMT  
		Size: 17.6 MB (17643062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868ff84c98f686b16bc8d5daa65da0ff82a7410bfd8cd1c086c58b21f50794f7`  
		Last Modified: Tue, 30 Dec 2025 02:34:38 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d07d9da7ea177176e08dfc406ef67a9162a36ba47c9df0fb61915776e4fe455`  
		Last Modified: Tue, 30 Dec 2025 02:34:38 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:40f5b45688d897ee76deddf5ab5664030e64f1107f558654a19af5938a00ca1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ea34d92369b7b83a14ea5c75f48c72098773b72fea65c66691ee2214fa4e7a`

```dockerfile
```

-	Layers:
	-	`sha256:04aba73ec330d48dd885903695660fff57b8dfbeab138e1cb8daec4d43e884eb`  
		Last Modified: Tue, 30 Dec 2025 03:30:25 GMT  
		Size: 59.1 KB (59134 bytes)  
		MIME: application/vnd.in-toto+json
