## `friendica:rc-fpm`

```console
$ docker pull friendica@sha256:594d893e8866adee3f36bca6f54e0741f70d99bb924ea5c53eb33db6e3f568c5
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `friendica:rc-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:334e7abcfe8437e1ab8deee053c82335b95d8353e5f934ce868bd98724fb6b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262594242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a501ecd1d401b8da30a48b23fbdd8ce546d0e525d75b8a75f6b2cd3316a290`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:16:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:16:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:16:29 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:33:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:36:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:36:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:36:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:36:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:36:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:36:23 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:36:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 02:36:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 02:36:23 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 02:36:23 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 03:32:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:32:39 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:32:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:35:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:35:14 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:35:14 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:35:14 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:35:14 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 03:35:14 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:35:14 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:35:14 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:35:14 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:35:14 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 03 Feb 2026 03:35:14 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 03 Feb 2026 03:35:19 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 03:35:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:35:19 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:35:19 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 03:35:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c90d928fb1e378f3e4d3ab784534fbf6aeb69af185339bd6e770fb79776931`  
		Last Modified: Tue, 03 Feb 2026 02:19:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4c5987d31091412825548ec355ea73dac4057ba0e67959c5dce41b99e94967`  
		Last Modified: Tue, 03 Feb 2026 02:19:52 GMT  
		Size: 117.8 MB (117839199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbc38aed789e872dfff4176660f5f351b4f087ad766b32746802755ee1d59e3`  
		Last Modified: Tue, 03 Feb 2026 02:19:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eef3f7d69479db54505c87e1ce99b840942931eb2cd7999af838f4c7cd48f81`  
		Last Modified: Tue, 03 Feb 2026 02:36:34 GMT  
		Size: 12.8 MB (12755518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdd72aea715d1e54829ee18f90b46d1cc0b191709d0c056680d0885c47b9ca`  
		Last Modified: Tue, 03 Feb 2026 02:36:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335d1a0a138632c06436d60985dd676203da95d46f58f35a4706a07d096607e`  
		Last Modified: Tue, 03 Feb 2026 02:36:34 GMT  
		Size: 11.9 MB (11898975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96afdc884cc3a490eeb6ceafd11af26eacb1d43c9ce8f19703fc1b1b9ac31ebb`  
		Last Modified: Tue, 03 Feb 2026 02:36:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b946c9892f3e87da82f256f9f8cfe53f4882e377e3f56cdbe20896c40b05fbe`  
		Last Modified: Tue, 03 Feb 2026 02:36:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8018e7354a190bcef314a7c1107c662ddc28bfa1e69a6a97a9f2624b10827e`  
		Last Modified: Tue, 03 Feb 2026 02:36:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0318e72cae7a9475fe31c0f71e05f17f5820e820d46abbbfff5cbc674e69fe`  
		Last Modified: Tue, 03 Feb 2026 02:36:35 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82c005822f0b0b1b82fa99b9ef7f43e37c2e24eb5ef65ab70c21a34cf4c8316`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 21.0 MB (21026909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e6896896114c741bf31df45f74d4abb65ed2fad187bc5b4bd99da512ab6d57`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 1.1 MB (1110992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c96d9465ba3012ff6f540bdec6044e28e5c921918acd3a50173bce4945f13ee`  
		Last Modified: Tue, 03 Feb 2026 03:35:30 GMT  
		Size: 49.2 MB (49207995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab3712a43a0db2833d2864d61a728bfe11d249bc54bf9fcf066bc75904b73d7`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bad0ab77908411f1027c5a98a5cf1d40b6522f0eb2a903816a6eddc305b44f9`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04272b30a84f3a7bd376d23dfba67b837404729128cb79052fba2f0f9bf4e51`  
		Last Modified: Tue, 03 Feb 2026 03:35:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb87895d52f90185789119ac2218f25af890cbe9593d359b625b8c7d58b157`  
		Last Modified: Tue, 03 Feb 2026 03:35:31 GMT  
		Size: 19.0 MB (18956916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b558b5d6e9875abd80b7e2b15320f336b74975a9a873af57daa86ed5740a0e6`  
		Last Modified: Tue, 03 Feb 2026 03:35:30 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079a9195dd62494b17ccd9f28e435213d8cb318ca44e37ff98e0c74816f2007a`  
		Last Modified: Tue, 03 Feb 2026 03:35:31 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:014bda19d7827bd63202dbc748819923af7760211646b089de7df5e603041463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2284e2a64daa7b6b4a6570d844f52e3d2c16258fcdca7aa4509290f64ae4e54`

```dockerfile
```

-	Layers:
	-	`sha256:e1ce7d3f43491a13a0430f017c8dfc163de34d5a9068fa1f8f9112ef9601fbfd`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 59.1 KB (59132 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:926f39d01de260b585157e0da741b4f7b192ad9e3adbd4cf37892c86f6006a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232699565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6a4db4777acd31efd803759eb78a4bbbc0ce1a48b3ce4d6ff40fd7ce37ae67`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:15:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:15:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:15:58 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:44:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:44:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:47:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:47:36 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:47:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 02:47:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 02:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 02:47:36 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 04:46:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 04:46:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 04:46:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:50:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:50:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 04:50:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 04:50:03 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 04:50:03 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 04:50:03 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 04:50:03 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 04:50:03 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 04:50:03 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 04:50:03 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 03 Feb 2026 04:50:03 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 03 Feb 2026 04:50:11 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 04:50:11 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 04:50:11 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 04:50:11 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 04:50:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c35f0a537e4d387b0697eed3cade81a8688fdfc2352e851fb2228e5824a15`  
		Last Modified: Tue, 03 Feb 2026 02:19:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c3b03904dfee8f4f28565c5d82a4e13e6117da96c7b26a786376085beac5e8`  
		Last Modified: Tue, 03 Feb 2026 02:19:49 GMT  
		Size: 94.9 MB (94876186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a10c115eb49c5c75ea3d9b5e88cbd50281e4ce3752937331c018f66b5219d1`  
		Last Modified: Tue, 03 Feb 2026 02:19:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a621860e0491e5b85364614387a354ed271f07e04554c0bde2fad8cb3eab3`  
		Last Modified: Tue, 03 Feb 2026 02:47:46 GMT  
		Size: 12.8 MB (12753312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed8c6f5980afd27dd6b89953e6f4391820d3a805a4aaa0b4ad62896ce5c0ed6`  
		Last Modified: Tue, 03 Feb 2026 02:47:46 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eb15361f6e0b45eb750c8fc185a8a58b1ccd1298a1386d991cafba4d87fd05`  
		Last Modified: Tue, 03 Feb 2026 02:47:47 GMT  
		Size: 10.7 MB (10692187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c497d484381fc830e90599329a5c4dcbb3dd248b291d2bd734b419cc716520`  
		Last Modified: Tue, 03 Feb 2026 02:47:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482f8d2f4f8efab73e7e7158ef78222e16286777adf83910f4cade59fab7263`  
		Last Modified: Tue, 03 Feb 2026 02:47:47 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786fcf990a0622c8ac682b8eb19c357d9933897f35843cd29bf8ef8a547a3366`  
		Last Modified: Tue, 03 Feb 2026 02:47:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b10b401627e9c348af8bf45ba1eddefac85c725621ac57292a6f7c54f74f95f`  
		Last Modified: Tue, 03 Feb 2026 02:47:48 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b754b545843fb85dcbf8692eb273de09024eea97c606a612525948990ea25e1d`  
		Last Modified: Tue, 03 Feb 2026 04:50:21 GMT  
		Size: 20.3 MB (20348428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06238391bbe5f3dbcbc66eeb9ff4a2542d0742f0ddd374f259e18303f0e0cef1`  
		Last Modified: Tue, 03 Feb 2026 04:50:20 GMT  
		Size: 1.1 MB (1085549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba72fc241253977e6a9086b0d7e41cc292a49424350bd2ed5ee3bee28499a46`  
		Last Modified: Tue, 03 Feb 2026 04:50:22 GMT  
		Size: 46.5 MB (46522219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6881eba56e6fde12c7de8f7d9620060ae74763bfec39328edccf30d23e432f1`  
		Last Modified: Tue, 03 Feb 2026 04:50:20 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7a568a8d17d1c988135683f7354fbae55cf5f8c55e7a41f322899016c9afe`  
		Last Modified: Tue, 03 Feb 2026 04:50:21 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ee6955b3f88788878362334b7466bda8d618733ab4240000aec02210965a72`  
		Last Modified: Tue, 03 Feb 2026 04:50:21 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2ccdc8eafbe19b6d3b1cc99f6509a93370cbc38a7102b3b154416e77040c4f`  
		Last Modified: Tue, 03 Feb 2026 04:50:23 GMT  
		Size: 18.5 MB (18454982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042fedb29b78d1e01cb7744f5b0b8c3d372188bcbeb27c3315421b5ad3112793`  
		Last Modified: Tue, 03 Feb 2026 04:50:22 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7f54b9687e4d65b5f839f96a84c500f405c2816d46f42a917cb21b5d504f78`  
		Last Modified: Tue, 03 Feb 2026 04:50:22 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:305cce94b08d60c7b103364de7b4123c2efd438e97ca767f66f55a510b9a7e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f83c477c359efbb56b669667877dfe6ee5b38284c8da00b2ec9ca8b7f937654`

```dockerfile
```

-	Layers:
	-	`sha256:a4464883a06c10e01d5706252c11f568c812f76ad76ffbe14d4c1f4e8eae9c4d`  
		Last Modified: Tue, 03 Feb 2026 04:50:19 GMT  
		Size: 59.3 KB (59263 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:6576a31ad88806212cf3871a76e2aaea86917201a3fce84f15811dd72472166d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221983812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774822db2a64b7fcd4225fc0ce486ea889c7b45aba0a68ae7bdab2a2c4a53ae4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Fri, 30 Jan 2026 01:38:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 30 Jan 2026 01:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jan 2026 01:38:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jan 2026 01:38:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_VERSION=8.3.30
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 30 Jan 2026 01:38:45 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 30 Jan 2026 01:38:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 30 Jan 2026 01:38:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:41:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jan 2026 01:41:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:41:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 30 Jan 2026 01:41:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jan 2026 01:41:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jan 2026 01:41:28 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 01:41:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 01:41:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 01:41:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 01:41:28 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 02:35:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 02:35:32 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 02:35:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 02:38:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:38:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 02:38:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 02:38:29 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 02:38:29 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 02:38:29 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 02:38:29 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 02:38:29 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 02:38:29 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 02:38:29 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Fri, 30 Jan 2026 02:38:29 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Fri, 30 Jan 2026 02:38:36 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 02:38:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 02:38:36 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 02:38:36 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 02:38:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6f573155381029bc5bcade931191c22edea2744a3d9f47361f43047f40f350`  
		Last Modified: Fri, 30 Jan 2026 01:41:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f0891274fd9082819cd1dd3bf023f74d4661990b78fafae353c06134484dc2`  
		Last Modified: Fri, 30 Jan 2026 01:41:49 GMT  
		Size: 88.5 MB (88455675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d324ca7c9a06bed722fa4671fc7e5625e31e26c5984f4e67c8ec99f88a0eec88`  
		Last Modified: Fri, 30 Jan 2026 01:41:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062d09e0d7e81e844820abc03e91b4fbc502faf6ff562a4e84b40ee0211d0c7c`  
		Last Modified: Fri, 30 Jan 2026 01:41:47 GMT  
		Size: 12.8 MB (12753665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a00167afb1f00c7f53af22f82db1489da82d8db0565cc6cead46fe7ea5bc427`  
		Last Modified: Fri, 30 Jan 2026 01:41:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868013034d9f68f36234c7059bdd936cd48fa8470d987faba7566dc54f35de9e`  
		Last Modified: Fri, 30 Jan 2026 01:41:48 GMT  
		Size: 10.1 MB (10082876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78016f3bb74adac8fb344a7e32e4252bb0236f0cf18006443bc75cf71a53f52`  
		Last Modified: Fri, 30 Jan 2026 01:41:48 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f254f181d7b314fb479ad0eed303078642789529df5deb0c48b521526540b33f`  
		Last Modified: Fri, 30 Jan 2026 01:41:48 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe63daefe6a33d54c3ae40448a15ad4d8a789390050d002680a1f7500f57114b`  
		Last Modified: Fri, 30 Jan 2026 01:41:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bae647f09b0fcaa24d01b2fef6b3f079d08cade54c21f44e3c713474dc4a737`  
		Last Modified: Fri, 30 Jan 2026 01:41:49 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e29392841615518362946ae8c65c6f7a553788a78528c434d79d84ab1c6a7ef`  
		Last Modified: Fri, 30 Jan 2026 02:38:45 GMT  
		Size: 20.2 MB (20177270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6bb2f7c06f17d4040a3fe75f17e9d17cded91336be55a52d7707f99d29cd6b`  
		Last Modified: Fri, 30 Jan 2026 02:38:44 GMT  
		Size: 1.1 MB (1076048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d9dc30573c57aa8886001634a1506f654f966754727f9454c1e3352642e658`  
		Last Modified: Fri, 30 Jan 2026 02:38:46 GMT  
		Size: 44.8 MB (44790065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc235e4133abb8781d01bb58ab0c96296e5758981ea35dfcf942389ae704e39`  
		Last Modified: Fri, 30 Jan 2026 02:38:44 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9177dda4b940e83ce1b2e62a76eaf4442ba76476e50cc28d40412a0829914f5a`  
		Last Modified: Fri, 30 Jan 2026 02:38:45 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e0c62fc7762cd230d2c03b2cdc33e39fc635ebd20fb28dbac70de695a89ae`  
		Last Modified: Fri, 30 Jan 2026 02:38:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24940aabd93f7b3dbd00b33f2300497d6864ca8f7933ac7a57a2575636c59a`  
		Last Modified: Fri, 30 Jan 2026 02:38:47 GMT  
		Size: 18.4 MB (18420501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dacae1c82cf4648cecf81e224a3f58874407767ddcde57b6181d167ba27e24`  
		Last Modified: Fri, 30 Jan 2026 02:38:46 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6729f12bd050d220da216a9f342b0dbea2a158949f6010c7d53500437a4d635f`  
		Last Modified: Fri, 30 Jan 2026 02:38:46 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:19475f72c438e1a01244f85c4a99a7b7950d7d6c4a8df4c3f9c968a29f437830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd5a8f58bad471fbb420c22911196da9c9e0e932a65bc6757716487a5d35d4d`

```dockerfile
```

-	Layers:
	-	`sha256:d78a685e016b929bb9fca178d4bed255c996e3830763e2a333e0465e05e66d05`  
		Last Modified: Fri, 30 Jan 2026 02:38:44 GMT  
		Size: 59.3 KB (59263 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:711b0ecc5793d240cc61d41997a84468ced289286d9d83a777a5e1191442e2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253969003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f291daeccc2f6168651103dcee6e3ff44a78c6602e60595a5030e418fee734`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:30:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:31:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:31:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:31:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:31:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:31:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:31:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:31:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:31:07 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:31:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:31:07 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:34:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:34:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:38:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:38:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:38:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:38:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:38:16 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:38:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 02:38:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 02:38:16 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 02:38:16 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 03:51:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:51:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:51:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:54:44 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:54:44 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:54:44 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:54:44 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:54:44 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 03:54:44 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:54:44 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:54:44 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:54:44 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:54:44 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 03 Feb 2026 03:54:44 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 03 Feb 2026 03:54:49 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 03:54:49 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:54:49 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:54:49 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 03:54:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3399aa7533488f51373a1e49737cf431abd08140c95643da9bf76eb36d79d3`  
		Last Modified: Tue, 03 Feb 2026 02:34:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b465c09213deda4a39c3200f99d5f4e521d6a4752d2a23b9478a245d1dfc09ce`  
		Last Modified: Tue, 03 Feb 2026 02:34:27 GMT  
		Size: 110.2 MB (110164602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803ef7ea6158a0a541ab55973615fc1140da51effe476b987c865cc6a220139`  
		Last Modified: Tue, 03 Feb 2026 02:34:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac03bd801868cdccb8daf8718dd86188fe394d89b3c63dc355b4e126c5b996e9`  
		Last Modified: Tue, 03 Feb 2026 02:38:28 GMT  
		Size: 12.8 MB (12755045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920fe5234d512706d033a83b2e04e4556073138b7332b9053edfb6f29c4e8a74`  
		Last Modified: Tue, 03 Feb 2026 02:38:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c4d5b33a2267bc816c8ed52a6da0e24256564aa13485f778424e234127ad51`  
		Last Modified: Tue, 03 Feb 2026 02:38:28 GMT  
		Size: 11.9 MB (11924524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c0b62d4b8d142e828b29e60d2f44899a1efb88934c204f1383c172b8e707e0`  
		Last Modified: Tue, 03 Feb 2026 02:38:27 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f06396a9672d2061a662e1eeeb76f1f2d0bba85ada687fdde63fd89cf21510`  
		Last Modified: Tue, 03 Feb 2026 02:38:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6c0fc2ec8e067551ce279e243e54443f33166d446f466bcae4a6e6c910bf51`  
		Last Modified: Tue, 03 Feb 2026 02:38:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ad916b3f318bccf1a01521f1dc399d7d19a3cc42504d970d6974bfd7193cb`  
		Last Modified: Tue, 03 Feb 2026 02:38:29 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4f9425f4345b2dbba29614fc8acddb9170a096b8405fcc1638586f13e5710`  
		Last Modified: Tue, 03 Feb 2026 03:54:59 GMT  
		Size: 20.8 MB (20773520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa29968cb6e067b4411ea6a969ebe5462a28dcc7deb3b8b9399f8e77d5b89f4`  
		Last Modified: Tue, 03 Feb 2026 03:54:58 GMT  
		Size: 1.0 MB (1043230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3be4216c1d97821a6c9393b63012835d0f279ce99e59d4a237b976bec4cef8c`  
		Last Modified: Tue, 03 Feb 2026 03:54:59 GMT  
		Size: 48.3 MB (48330422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527d776f44b0b15a30a269a4896a777c0a5ce8b5ed76421f7adaf518075ff2f5`  
		Last Modified: Tue, 03 Feb 2026 03:54:58 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb56ed024616bd12053622c82635074189678b34915d90f1ca4a097712f4e34`  
		Last Modified: Tue, 03 Feb 2026 03:54:59 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237204b1172c0becca5f33973661b98e425720ce647e956e9f8dbd288d7719d6`  
		Last Modified: Tue, 03 Feb 2026 03:54:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2051f2217f4cf5c5eeeba662be88bb3134b759a5b1dcabc8ff0d20c21ea2ca`  
		Last Modified: Tue, 03 Feb 2026 03:55:00 GMT  
		Size: 18.8 MB (18818463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69ad26455fe1c3a57203100a13c82c2219facdac67c7547e10ae67c1d8ffbc4`  
		Last Modified: Tue, 03 Feb 2026 03:55:00 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b46012ceb6c47a7dc3945eaef9bbcf0d4c90816fe3266f48cddb9b2e759b3c`  
		Last Modified: Tue, 03 Feb 2026 03:55:00 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:8392d28005fccdb8de11c8a280742c3beefb020fdbb649284f84b4387736859b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea096dbdb3370140602d114c8ad13cfbd8d3b53745f60b1d2dbce75747ec3ff`

```dockerfile
```

-	Layers:
	-	`sha256:04212a8b3d3722fa3c380c72dbae69803f2af91e0f7194c93c4e8d8f0379923b`  
		Last Modified: Tue, 03 Feb 2026 03:54:57 GMT  
		Size: 59.3 KB (59302 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; 386

```console
$ docker pull friendica@sha256:dd4f8ddd3e5c5a806d7d1ad75ada68e8120e7b806766ecae44bbdaefab3e7814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266333583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16d68f37f79d5bb8ecd5c78397dd29529b59a6d278a0814d93774043a4a23bb`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Fri, 30 Jan 2026 01:10:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 30 Jan 2026 01:10:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jan 2026 01:10:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jan 2026 01:10:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_VERSION=8.3.30
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 30 Jan 2026 01:10:28 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 30 Jan 2026 01:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 30 Jan 2026 01:22:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:25:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jan 2026 01:25:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:25:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 30 Jan 2026 01:25:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jan 2026 01:25:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jan 2026 01:25:33 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 01:25:33 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 01:25:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 01:25:33 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 01:25:33 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 02:22:26 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 02:22:35 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 02:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 02:25:15 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:25:15 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 02:25:15 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 02:25:15 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 02:25:15 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 02:25:16 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 02:25:16 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 02:25:16 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 02:25:16 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 02:25:16 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Fri, 30 Jan 2026 02:25:16 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Fri, 30 Jan 2026 02:25:20 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 02:25:20 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 02:25:20 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 02:25:20 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 02:25:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa3153b428d75901a41f50ee6b71bfb8be06cb7a905fa04ab10f86d59118ab9`  
		Last Modified: Fri, 30 Jan 2026 01:14:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e089b41f23437dd234df79c0e8198d01da54118c30c4906a050e1af506a0b13c`  
		Last Modified: Fri, 30 Jan 2026 01:14:09 GMT  
		Size: 119.0 MB (119026918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b09a305ebf42f95614f578a83709cd46149db248ba7aa9de2e692c5c1cf16a5`  
		Last Modified: Fri, 30 Jan 2026 01:14:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508ef68b8dbcc1028384bbf70e5862a14e79316d9e7a7f75e1200f013054ad2`  
		Last Modified: Fri, 30 Jan 2026 01:25:43 GMT  
		Size: 12.8 MB (12754820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614782a82ba1b615670e3b6af1cf9bf4eac8477c098a5138f0b194b2cdad3e2f`  
		Last Modified: Fri, 30 Jan 2026 01:25:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d03e3d594e267cf9163414f59f0ace5c8d7613c070c116740a54dadf8ca08ac`  
		Last Modified: Fri, 30 Jan 2026 01:25:43 GMT  
		Size: 12.1 MB (12106443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce0f69c20f444026e211ad9cf6b8531fb4a339d24d03c4ea26a61f8ef0ed5c1`  
		Last Modified: Fri, 30 Jan 2026 01:25:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a7007cdca41a0050e71514db114bc957cbd4fd942d1e8baaf566f5f5641cf8`  
		Last Modified: Fri, 30 Jan 2026 01:25:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14857ca5a1b74d5002a63fd8d00d0bf9b9f6cc004ea8cdbee981aa991c8cafd8`  
		Last Modified: Fri, 30 Jan 2026 01:25:44 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0c336b1390098475493e35cc3daf024345be8411c5d453f4e83608c1117711`  
		Last Modified: Fri, 30 Jan 2026 01:25:44 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cce8ba2c1041b37d74f0ac2d3600d3d85dd4cb8ad30002c75bb092c2d9aedb7`  
		Last Modified: Fri, 30 Jan 2026 02:25:30 GMT  
		Size: 21.3 MB (21272542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a94726ecfc4ceea7ba3841633cf1de39960d2ef876cf78ec25e7811fbf0ba1`  
		Last Modified: Fri, 30 Jan 2026 02:25:29 GMT  
		Size: 1.1 MB (1086138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83450f15e443a42913db08da27dd4d767dfd0b65d0aaf27cab93fad5e0aec63`  
		Last Modified: Fri, 30 Jan 2026 02:25:31 GMT  
		Size: 49.5 MB (49450187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1381fb4e49786b1ccf1cdce5ff0a997f54ca6d1bcbd0f93990f6d41d0481f7b4`  
		Last Modified: Fri, 30 Jan 2026 02:25:29 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d4bf61bc8da1d5e4262ac2e29b7935c3022f7b94f34975e5390d076985dd4e`  
		Last Modified: Fri, 30 Jan 2026 02:25:31 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e860ad3c9a257788f61839f5c08ec49a83d5dd04859cd5c347c6dda99893c8d`  
		Last Modified: Fri, 30 Jan 2026 02:25:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bf9b601d7119d13314ede2b94f49adbdbe62c335013e112808e41867f9bbf7`  
		Last Modified: Fri, 30 Jan 2026 02:25:32 GMT  
		Size: 19.3 MB (19328930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74015f553db225b633f61e0abaf26785e9f4816590ac1d598636f3c97d2d7a`  
		Last Modified: Fri, 30 Jan 2026 02:25:32 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b29ae8c308afbf0784e87037033bb1df25c8406ab5580d57365c55e49beaa`  
		Last Modified: Fri, 30 Jan 2026 02:25:32 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:f573f0269e22d590f6e3093599cb86a62c0006152f01f37a4ecb991eaedeb0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de2e5cdbd03b62b85e8ea438c32545ee1a9ab11f7f0ae969c98bdc769aaffcc`

```dockerfile
```

-	Layers:
	-	`sha256:57c33b94ad8ae86ea012612cf89db2e0902ba8fbf93a2f1003ad35f3781b1d17`  
		Last Modified: Fri, 30 Jan 2026 02:25:29 GMT  
		Size: 59.1 KB (59098 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:dea1a38b3e660714977cb74b4ef15da639b58cf85b7befdd4d656ef0536089dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264265278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5e282668c5634b14727db511b1851f3ca87d179986973dd347cb5d39eba6e0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:49:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:50:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:50:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:50:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:50:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:50:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_VERSION=8.3.30
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sat, 17 Jan 2026 00:07:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 17 Jan 2026 00:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:22:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 00:22:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:22:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 Jan 2026 00:22:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 00:22:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 00:22:04 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 02:16:53 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 02:16:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 02:16:53 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 02:16:53 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 03:51:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 03:51:46 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 03:51:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 03:55:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 03:55:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 03:55:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 03:55:59 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 03:56:00 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 03:56:00 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 03:56:00 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 03:56:00 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 03:56:00 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 03:56:00 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Fri, 30 Jan 2026 03:56:00 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Fri, 30 Jan 2026 03:56:11 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 03:56:12 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 03:56:12 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 03:56:12 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 03:56:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729c2d5c144b66bc0a7de79ce37a807764c298349e33d3b4d2b9ffc6e4f86da`  
		Last Modified: Tue, 13 Jan 2026 01:56:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5312002cd976a0822f64d1b71b8a785c0ab1242111634934907ad0ff8cd084`  
		Last Modified: Tue, 13 Jan 2026 01:56:07 GMT  
		Size: 109.6 MB (109597601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c320c737217d4d4f5283740cc3e07729118082922eab5fedf369acbd762089c`  
		Last Modified: Tue, 13 Jan 2026 01:56:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6011d98d463415f4d5b067760ccddd9d607e2e18f8b0f144a9970f0bbfe58ef`  
		Last Modified: Sat, 17 Jan 2026 00:11:59 GMT  
		Size: 12.8 MB (12770331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f8964b5b3c8f07df5cb2093449834ffde1c13d7b8fa5ba61165456bc89aa78`  
		Last Modified: Sat, 17 Jan 2026 00:11:58 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bb13b6ca193bdf7d9bce5c748fdd0869d3a52514cbc2a3ab9cffc27d77a1b7`  
		Last Modified: Sat, 17 Jan 2026 00:22:33 GMT  
		Size: 12.4 MB (12439071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e814e2b7714556a652aff2670c22cebc577589bb5acc9b809ec73a4265a7904`  
		Last Modified: Sat, 17 Jan 2026 00:22:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043196ac15f9aeb959ac654f2f8fd9666787d152c5e03f0362e13062c299c8ed`  
		Last Modified: Sat, 17 Jan 2026 00:22:32 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0135cdbf61330e7abfa697b5bd5e6a13df1a49872a00df5e845779ce90b4cb`  
		Last Modified: Sat, 17 Jan 2026 00:22:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f4c7cef386b92ff43764a4adc108cdb637dbf22e3f8bd6356cc09368b46fc6`  
		Last Modified: Fri, 30 Jan 2026 02:17:21 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea2e040695721e280e45f60f43bc3164b78e20c9bc250344dea542be712417`  
		Last Modified: Fri, 30 Jan 2026 03:56:34 GMT  
		Size: 21.3 MB (21287155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c5117038a76f7dad471a193845b108e6521f2232ffea35b47e9674b1904dc`  
		Last Modified: Fri, 30 Jan 2026 03:56:33 GMT  
		Size: 1.0 MB (1033051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c54c81057b212c296ab63c8fc06a6e3a05e9d0fdf603bf7e14c561c8e4a91`  
		Last Modified: Fri, 30 Jan 2026 03:56:35 GMT  
		Size: 54.5 MB (54461971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c6ed817b4bdef00183d4c1d5f765259d595d937fe8fbec67cbca5a227815b`  
		Last Modified: Fri, 30 Jan 2026 03:56:33 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c94ec32d21db5a3aec7436a8705f486f46db6ae7c656bcf2d9c878dbc5154`  
		Last Modified: Fri, 30 Jan 2026 03:56:34 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a084e608cecb2f74c923e15c6d5e27095c1a50191ab85dfda51762147f9d421`  
		Last Modified: Fri, 30 Jan 2026 03:56:34 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb40b7bd30280b68777e36ff7d48c3b6fb6a791fdb0b5708a046a7b415de13`  
		Last Modified: Fri, 30 Jan 2026 03:56:36 GMT  
		Size: 19.1 MB (19061372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0153d88d759f168f24d659c62e04189226da9f4485069c72afd14d6c48c468`  
		Last Modified: Fri, 30 Jan 2026 03:56:35 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7953b406874e83785128d4f75ee9bf86e96a58a22b562ea53d7c80405f3ec8cc`  
		Last Modified: Fri, 30 Jan 2026 03:56:35 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:26cc902d9b93a2d0cdd461b5f4bcb59f2242d211d6c7a6cb54d29834ea05f1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589b040124584048abec325e16d5bc59353461d56637355caf6827eea2bcb17a`

```dockerfile
```

-	Layers:
	-	`sha256:053ffed8e3d30faf856dfe64ffb2fb1f74a54bb3a988103997fe504c948dc93e`  
		Last Modified: Fri, 30 Jan 2026 03:56:32 GMT  
		Size: 59.2 KB (59175 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; riscv64

```console
$ docker pull friendica@sha256:dafc57c18dc670c5e024a0b243d6135294926f17f264d7f12299270c75a34245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295382430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967c1af451c0ca2cf2312024a6ffa49a4f62fd0f1a78a76c29e1cd802104ccd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 16:40:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 14 Jan 2026 16:42:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 14 Jan 2026 16:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 16:42:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jan 2026 16:42:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jan 2026 16:42:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_VERSION=8.3.30
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sun, 18 Jan 2026 12:37:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 18 Jan 2026 12:37:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 15:13:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 18 Jan 2026 15:13:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 15:13:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 18 Jan 2026 15:13:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 18 Jan 2026 15:13:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 18 Jan 2026 15:13:29 GMT
WORKDIR /var/www/html
# Sun, 18 Jan 2026 15:13:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sun, 18 Jan 2026 15:13:30 GMT
STOPSIGNAL SIGQUIT
# Sun, 18 Jan 2026 15:13:30 GMT
EXPOSE map[9000/tcp:{}]
# Sun, 18 Jan 2026 15:13:30 GMT
CMD ["php-fpm"]
# Mon, 19 Jan 2026 19:43:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Mon, 19 Jan 2026 19:45:16 GMT
ENV GOSU_VERSION=1.17
# Mon, 19 Jan 2026 19:45:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Jan 2026 20:11:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Jan 2026 20:11:20 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 19 Jan 2026 20:11:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 19 Jan 2026 20:11:20 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Mon, 19 Jan 2026 20:11:21 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Mon, 19 Jan 2026 20:11:21 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Mon, 19 Jan 2026 20:11:21 GMT
VOLUME [/var/www/html]
# Mon, 19 Jan 2026 20:11:21 GMT
VOLUME [/var/www/data]
# Mon, 19 Jan 2026 20:11:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 19 Jan 2026 20:11:21 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Mon, 19 Jan 2026 20:11:21 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Mon, 19 Jan 2026 20:12:08 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Mon, 19 Jan 2026 20:12:09 GMT
COPY *.sh upgrade.exclude / # buildkit
# Mon, 19 Jan 2026 20:12:09 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Mon, 19 Jan 2026 20:12:09 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 19 Jan 2026 20:12:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5316a37adfe759942e176fd7f10a29d05b3a11f1e1ee941f4e57475f602a088b`  
		Last Modified: Wed, 14 Jan 2026 17:45:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4446eab7b758c11057a2a24af5250e361ee957c8bbeefbbfe2d0589362c88b78`  
		Last Modified: Wed, 14 Jan 2026 17:45:59 GMT  
		Size: 146.6 MB (146578411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdab7a0d39d3c969a3d5797534890fb011b1e36b12815336c2b2920d0b178acf`  
		Last Modified: Wed, 14 Jan 2026 17:45:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42a622adfa91394ae6400e697d2e5745a17d93ac9a4fdfc807ff08d99e6ae87`  
		Last Modified: Sun, 18 Jan 2026 13:29:36 GMT  
		Size: 12.8 MB (12769998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc91a59e12f6496dbf7a07e4c22c9623a530892a50dfde98fa2252110af9db1`  
		Last Modified: Sun, 18 Jan 2026 13:29:32 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c6d454fd557bfb4a59e6f31e1786b456b632c3abfaaaaea5560001c2260c2f`  
		Last Modified: Sun, 18 Jan 2026 15:16:26 GMT  
		Size: 11.5 MB (11466747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72b2223893d8c0aa8020b4b78c3619611fda85508f631c842403dd564926549`  
		Last Modified: Sun, 18 Jan 2026 15:16:23 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51688d79d57d4618a307caa2896c82b5e07e7a202f18049756dcec09a5e4a1`  
		Last Modified: Sun, 18 Jan 2026 15:16:23 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f969a02da4cb5c54c6c8bbb2250b22820e88d3110f713ed46699d9f6ea596801`  
		Last Modified: Sun, 18 Jan 2026 15:16:23 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0082e33565633d28340807c4f58d0d794d685045acba75feae87d58562aec673`  
		Last Modified: Sun, 18 Jan 2026 15:16:25 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd5bcff5f7aff92610f48d266aaf1d2f43ee45d849b7884369be011a3bcf71`  
		Last Modified: Mon, 19 Jan 2026 20:14:28 GMT  
		Size: 20.4 MB (20389637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e2da22d4a83e91144c0bf6d8f4ef5a67181e9aca518cbbdc9e18f772f6481`  
		Last Modified: Mon, 19 Jan 2026 20:14:22 GMT  
		Size: 1.1 MB (1081274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d8a3177b83bd9700198397f12e1246254fa97842fac4afe56abc8b9711a714`  
		Last Modified: Mon, 19 Jan 2026 20:14:35 GMT  
		Size: 56.4 MB (56413737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10beb69434a5bd552db429763ed4e75b54246f9351efe596f99d4d8951ceeba7`  
		Last Modified: Mon, 19 Jan 2026 20:14:22 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cd2d1cf7e66d103249fb027dbbbc4207dfec7692af24c666a724904b2a8924`  
		Last Modified: Mon, 19 Jan 2026 20:14:24 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a206bb6f0022f38d513afdbcfb2da02d00b7376dbd7a52c761760a2b85dbd90c`  
		Last Modified: Mon, 19 Jan 2026 20:14:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a07445c157e18ecded719523b1862a2c0f7ecfb67f09d392f83ef2d94603a2`  
		Last Modified: Mon, 19 Jan 2026 20:14:32 GMT  
		Size: 18.4 MB (18391802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa051ff1992fb7602e7eb306b8c523329828ec4c7a0a49b5f9090cdff2d67d2b`  
		Last Modified: Mon, 19 Jan 2026 20:14:26 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e124481f8d95061ee40f249a5206516ba0635ec16316a3a68a6dbb6a3377c5`  
		Last Modified: Mon, 19 Jan 2026 20:14:28 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:ac4587d0338393632987aa043de140a6abde3d02d135cfc418cd0d7d3585429d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3008caa290e46ad38b442c45e31c8c2ef5f018e19e8467287c716a94d551fa2`

```dockerfile
```

-	Layers:
	-	`sha256:2531eb66208bf2c4f6d734331b9329d7914a7c3bb5a7fa8406e14e7028394919`  
		Last Modified: Mon, 19 Jan 2026 20:14:21 GMT  
		Size: 59.2 KB (59176 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:8866cebd986d7ce549fece0720491aa07d24a4fbd1c7e30e483f4ee073ca0a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234921985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0318f2491fb0c73417a1e098bb4b4d90f7e1376081cb8f7bb30a7212db0e3807`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:21:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:21:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:57:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:57:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:01:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 03:01:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:01:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 03:01:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 03:01:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 03:01:05 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 03:01:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 03:01:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 03:01:05 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 03:01:05 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 05:41:19 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 05:41:28 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 05:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:43:38 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:43:38 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 05:43:38 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 05:43:38 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 05:43:38 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 05:43:38 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 05:43:38 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 05:43:38 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 05:43:38 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 05:43:38 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 03 Feb 2026 05:43:38 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 03 Feb 2026 05:43:43 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 05:43:43 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 05:43:43 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 05:43:43 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 05:43:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7e198ceab28d440d37bc9b2389ec84e5069402425c16e365d75cd20da313ea`  
		Last Modified: Tue, 03 Feb 2026 02:25:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfce049a7f31ebe3bbbea4249b3c047493e29ee727178adf1abbcf363d500955`  
		Last Modified: Tue, 03 Feb 2026 02:25:36 GMT  
		Size: 92.6 MB (92567679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e74625cb46a02aab18b786df1acf328a052bc24afe5610ef71d2e912d1f36a`  
		Last Modified: Tue, 03 Feb 2026 02:25:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edb8bfd9cce5ca5db3cfa578ff60a0e286cb4da248b544d615ad835d04f9ccd`  
		Last Modified: Tue, 03 Feb 2026 03:00:18 GMT  
		Size: 12.8 MB (12762798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631626b4b3c67c725b0c53b805863ed135558a3c2929fc63c305c4a6a523dc7d`  
		Last Modified: Tue, 03 Feb 2026 03:00:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4da49254cfb45081df5fe5596190fa69de87067e157b979e88070229b93dbf`  
		Last Modified: Tue, 03 Feb 2026 03:01:21 GMT  
		Size: 11.8 MB (11771171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f82434f15ffebc6a1323d9ac1900a464e269ce2a105ea55896609ae4ce0834`  
		Last Modified: Tue, 03 Feb 2026 03:01:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb4350e42c96f8b72585c5f1c77fd412107831dd2f0da0e1438b2b97ca8e9df`  
		Last Modified: Tue, 03 Feb 2026 03:01:21 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e370db62340792d5786eb77f96b8edc137c458a9813b96496f682d2020b73c`  
		Last Modified: Tue, 03 Feb 2026 03:01:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10748bba01a53ff011f1fd652a22cb99663f4d1468e9d1de96852d3ac137964`  
		Last Modified: Tue, 03 Feb 2026 03:01:22 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e0aced42ed751177d542a6c9bc673755d140cf9aa8db60b6755b9e7ca66ead`  
		Last Modified: Tue, 03 Feb 2026 05:43:57 GMT  
		Size: 20.3 MB (20310878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc843a3a37aaefd88de687d8d57a85af1135e254ff319db52dd63a6319dd4ff`  
		Last Modified: Tue, 03 Feb 2026 05:43:57 GMT  
		Size: 1.1 MB (1075669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de35d66388599c3246964ef5e7f54c20aa2ba3e9af77c474a21a847feb218c65`  
		Last Modified: Tue, 03 Feb 2026 05:43:58 GMT  
		Size: 48.2 MB (48226984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e617e28dd2ec48655238c17f3b4012895edd24248e357e24fa011318570e47e3`  
		Last Modified: Tue, 03 Feb 2026 05:43:57 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a798d788b07d56a2f0ed9da070248d57a7acef647923378854ed728ff6e91dd`  
		Last Modified: Tue, 03 Feb 2026 05:43:58 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af51242101af1ca22d44694615a39de3e776e6024d5d8dc18b1f4e28d1c1a58`  
		Last Modified: Tue, 03 Feb 2026 05:43:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396ac2b98d1643866fd2b6374f5bfbf5b1607405023adf59a6ccd5dd331bcc8a`  
		Last Modified: Tue, 03 Feb 2026 05:43:59 GMT  
		Size: 18.3 MB (18349519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee2aa625fc51b6f521ef8daf07ae1fa30ee063dac92beac83fd20f478a312a0`  
		Last Modified: Tue, 03 Feb 2026 05:43:59 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3ea5246b33d2595f3235df122666fe524768a45cb05c86ddbfad9c95ca8cfb`  
		Last Modified: Tue, 03 Feb 2026 05:43:59 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:64ff0b4f86d3e586faeb874b9ec3020c4318952ddb413af545d213778e837591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0663c380e92f4b4b1d6b36cf83028ed1961b91cd29aec303184ca4d30274a7c`

```dockerfile
```

-	Layers:
	-	`sha256:a752671e047b499574b2b2a2addc515bfe0e1f0546152d58b78a9da10fe62f87`  
		Last Modified: Tue, 03 Feb 2026 05:43:57 GMT  
		Size: 59.1 KB (59122 bytes)  
		MIME: application/vnd.in-toto+json
