## `friendica:dev-fpm`

```console
$ docker pull friendica@sha256:b70a98cdc778a6689a764e6d664311e0af937e602056a47c35c5118f208263c1
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

### `friendica:dev-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:307de1918524a1660bf11f560b65e808a0c0ba47f2c5b51adc38a3f3d2021f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212771915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e17a21c4d6378daae7545c16cd5746988e619f30a6f92fc7938a3052a5220bf`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dca462c8fa05d87a85eac989d130ea8f318a1d2418378bbbb96d5fb8413061`  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6141c85109a3f8338dd2b4fa761f7c301ed622d5d1b8f83f02c3eea71deedd8e`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 91.4 MB (91447922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaffb1dff77d041b80e66ee11f9a4e71b172888edf322c9b0448c3a0536def2`  
		Last Modified: Tue, 24 Dec 2024 22:27:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8caf356828dc89bbe7b589e50b19f960d5109f5cd616ed474ff029773cc8c87`  
		Last Modified: Tue, 24 Dec 2024 22:27:49 GMT  
		Size: 12.3 MB (12254372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13abdb17f2d3e7f3a3dc6ceecc371df5bebdbfe5bfe5761d32ca897b71eab83d`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80873f49b5128110d806b94ca8ae1a0a6335458010691b172946a4e6ed67694`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 26.3 MB (26319797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965c54bd56093e712769ae42362ec226e2b1c31d2276340535695a3f21994deb`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e9b6b83012482e94c2e058e9860c30671e19e53e89a5e691977962324d92ba`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e584ab7958fb1ce6023297cf6aa87444af616e806bd0d54156c4956ead3c8de`  
		Last Modified: Tue, 24 Dec 2024 22:27:51 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9c26d2a95373b2772fc51a6f48557500dd4e939a1f57d240a2de2e5409e62d`  
		Last Modified: Thu, 02 Jan 2025 19:31:25 GMT  
		Size: 15.7 MB (15695259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d3f99927e5534887ab8ebd6568a5fc5a71e28e9a0dc8ef57753f255d4f199`  
		Last Modified: Thu, 02 Jan 2025 19:31:24 GMT  
		Size: 1.1 MB (1096897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5964f6eaad4542b8cf9b79f672c54bab84ed380ca164926424d73e956545abf`  
		Size: 18.4 MB (18429726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64986b378b5ae4af6285e8eef34e2658a19c2d73ab46fc1e8874688c1276c0b`  
		Last Modified: Thu, 02 Jan 2025 19:31:24 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eccc98d29e5a0bc3c794126586497c86536363e5264cfac66a67e1ef88a0e7`  
		Last Modified: Thu, 02 Jan 2025 19:31:26 GMT  
		Size: 17.3 MB (17257071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c904d9009a3727922dfa55d2cd7bf67f9a9c7969086bbaa6ecda12513fb6aebe`  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87516557241742c2f8888fb4a2fc3ab38bc8a65aef04117a8144c38f12f1de46`  
		Last Modified: Thu, 02 Jan 2025 19:31:26 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:b17e76de8674665830bf5599b1d797bb1a5b7c4d02047068596aabf32245fba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 KB (47938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88707cc67cda0e388d474f891ed7ae7237c88992af4d734115814e7521583c70`

```dockerfile
```

-	Layers:
	-	`sha256:235c65e9eecf5c828ebbc5eec78adb997b63e28cca06c4acbf194f7cfe7f3157`  
		Last Modified: Thu, 02 Jan 2025 19:31:24 GMT  
		Size: 47.9 KB (47938 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:1551e2d8b4a8d0d4d685d0d68c473bdd7753f73949babeda1c336a855b45640f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179545099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896a1112d5b6ff4d38442b018c91426152cd4166512ef29c356edf509b24616b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0989fbbfc5677cb7ba281af4449917eb6aa0771685fd9d9c06b43b50ece3bd`  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed7b1b9105789e8dcb4a70b1bca07a9fdba709e47328dbbaea9c5b4bf87290`  
		Size: 69.1 MB (69119370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a233e03098e618374485da8fda6624c4ced95642637d019537cc640d4a81df`  
		Last Modified: Tue, 24 Dec 2024 23:02:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd20bf310d4db64389bd1bcbb9ca514916d98e60d4153f77ff49a98aa081002a`  
		Size: 12.3 MB (12252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2438f5fd646532c094d36de996753f3268765b445d99b43dd45a15a95c30800`  
		Last Modified: Tue, 24 Dec 2024 23:58:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3587f6e71f840efbd25de97fb8c2c62bc149b06f0aa310cc21b6364bf8290`  
		Last Modified: Wed, 25 Dec 2024 00:03:53 GMT  
		Size: 24.0 MB (24034797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295dc89e905d04d75bee42cd257ee7078876900b147573b9daa13ff7924cefe7`  
		Last Modified: Wed, 25 Dec 2024 00:03:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7b7ab557d032ab00a217aa969b8bbcebd52dd83fcea8d4aa77f21414a17339`  
		Last Modified: Tue, 07 Jan 2025 22:32:57 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9336c30adb036b486aaa09471bd3c2f01cca12ea938eeffc56a72b4b23bf5038`  
		Last Modified: Wed, 25 Dec 2024 00:03:52 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcbe1e367b56a51d6f11c3ce0acfb680262eebddc9f940ed8dff88d1cb647f`  
		Last Modified: Thu, 02 Jan 2025 19:45:45 GMT  
		Size: 15.7 MB (15655988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0462bc3ed34ef4f6b46a30561b003412e21377bcca1733300052ec2011a6f879`  
		Last Modified: Thu, 02 Jan 2025 19:45:45 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bad5bce9c08e4eeeb88d6827e5596e2e1be6a9c63bae170d427bc196525aa3`  
		Last Modified: Thu, 02 Jan 2025 19:45:45 GMT  
		Size: 15.0 MB (14982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8cd42e0de963e745a33f6032f13eb890e8710256169ebcd2d4442a5c8efd85`  
		Last Modified: Thu, 02 Jan 2025 19:45:44 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc653231395ab9395a1949fc82122afa6bed982959caacaa7d770c7bfc34ff8e`  
		Last Modified: Thu, 02 Jan 2025 19:45:46 GMT  
		Size: 16.9 MB (16884295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc8a458387158d19b5bc5b2210a01de9dadcb99b00f1c19dfaf46c5abea9e3d`  
		Size: 3.8 KB (3819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfa3da63d80835aba7e1f9cd29b7b0e2c24725cec96792422bc09c0df3f2588`  
		Last Modified: Thu, 02 Jan 2025 19:45:46 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:f9ee112ed5f61ea7abe3f4acbc48f12d0dbae0ac056d75caab699298cd20b894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abdc759de23f5bd22b9e6f59d62a2898e246081d8b89098f720ab545f42e1db`

```dockerfile
```

-	Layers:
	-	`sha256:0c53f964a3a7e61965ce49d1d0b4dd07ab6515078842b14d58badbaaf1000c1c`  
		Last Modified: Thu, 02 Jan 2025 19:45:44 GMT  
		Size: 48.0 KB (48050 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:bd956656730e000bd919902be0c658bf2386b50245ac2e2603e2467fc6a6b907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204322023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baba54564b61e389c0d389abd06a8342f3e0acebe6b881921abcaf4c3542dde3`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d60e98531329a411a90bc750803a988fe332fd46e0c9f626164216b0bf9ed`  
		Last Modified: Tue, 24 Dec 2024 23:21:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6518b047c296e77da2d983476df278091b3a6a373547505d5dfb7d5b8a0c2699`  
		Last Modified: Tue, 24 Dec 2024 23:21:24 GMT  
		Size: 86.7 MB (86734336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea19be978e0cfada36d5340360118f62486323ea1dabdcf29354c30974b84789`  
		Last Modified: Tue, 07 Jan 2025 22:30:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815fae4d4bc528423119ec6e89cad144675500e06bfb56ddcce38e8410f44efb`  
		Last Modified: Wed, 25 Dec 2024 00:20:22 GMT  
		Size: 12.3 MB (12253732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f2e6df4d0deb0d12109da95e379aeb7b0495d9cac818ec689423c54b43ba52`  
		Last Modified: Wed, 25 Dec 2024 00:20:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdab6c54cbeef49d1a249b2693fe5e40b532907f4c5b483f9929d57c1cb8e8e0`  
		Last Modified: Wed, 25 Dec 2024 00:27:11 GMT  
		Size: 26.4 MB (26380060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c55035f96dd73fb7863e36989a96dc1bf852684e16894e464ba919b615591b`  
		Last Modified: Wed, 25 Dec 2024 00:27:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ab5cf11c0326e3ded7e11569b5726f0a6e5a25b97d693a6d4ee254377257a3`  
		Last Modified: Wed, 25 Dec 2024 00:27:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f0899caa6cf1cc806829bd62409f8f850fd076215de96d3a730099b44c3584`  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e05cee6863ef7ccd8c74728f2670fbfecefeb8d84f518bb64648c282bd6d60`  
		Last Modified: Thu, 02 Jan 2025 19:46:39 GMT  
		Size: 15.5 MB (15456421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f472cb1572285de64d00b2a8fdaa9079a7ebc46a560332b6af73ff7d544087`  
		Last Modified: Thu, 02 Jan 2025 19:46:38 GMT  
		Size: 1.0 MB (1027619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542c20752eff68c14d559995e7c11b654017a98280228b4b6c24eb92bb6f3383`  
		Last Modified: Thu, 02 Jan 2025 19:46:39 GMT  
		Size: 16.7 MB (16658298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe81488c3368ee95b776b5bf8a08dc9d074ded5978f41270831aeba71c2b5f`  
		Last Modified: Thu, 02 Jan 2025 19:46:38 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8ec8b19ba64a952a8e152d55a66edfa1940387df2d56ff01f5c1326f6987cc`  
		Last Modified: Thu, 02 Jan 2025 19:46:40 GMT  
		Size: 17.0 MB (17048477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464144bedad8633308fb54bf5ddc0cb668b024a50d3a6e1cf4901200b89fedff`  
		Last Modified: Thu, 02 Jan 2025 19:46:39 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7369341c2e502da0b196c1855d9a0aa1358bc19646cd13a438a545376f42d5d`  
		Last Modified: Thu, 02 Jan 2025 19:46:40 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:77cc14f490cee39e4ea9dea4253bed6103b32440f12838ebea77069bd435e77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c509eed444bab38b4273b9f34845a5fe3139ad761155f00fbc009a4981adbcb0`

```dockerfile
```

-	Layers:
	-	`sha256:39ad1c3134bb351273b9457552e5643662605d2196bdd2ebe25b20afe89975d8`  
		Last Modified: Thu, 02 Jan 2025 19:46:38 GMT  
		Size: 48.1 KB (48077 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; 386

```console
$ docker pull friendica@sha256:7a9c95f9ade59c51e2acb087e02d4ff74c0ea39da38070bda856298f97826688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215733195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d0d460852a55601c9e618e6e76cdb2a904c8554f13a864663e77a28dad6a1f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
CMD ["php-fpm"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68106d819ae2c7e2cda05862cd2c8dea6f51dac6f07ab3e8d112b21169cf2bd0`  
		Last Modified: Tue, 24 Dec 2024 22:24:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1897ce3b1558d331b30d69fc69ec0c1ed45fb43ae0a869a9835ab31d932ec4`  
		Size: 92.5 MB (92521547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debb32b58ab6c2ffa870db5b27fcd1097a9acd1ba69f07b382ca8694544fe4f9`  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae26301d5c375c8f2d2c39eeb01c2a0a5fe2388231917e814b0c4264565a0a2`  
		Last Modified: Tue, 24 Dec 2024 22:24:20 GMT  
		Size: 12.3 MB (12253672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231165937dc146c9447fe0ab2c71fd78246612039b7bdfe5649741075061ead`  
		Last Modified: Tue, 24 Dec 2024 22:24:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31407547f8f475a98ba4e899a8f5bd0956ca229ddaf5a03528db6eb647c9f601`  
		Last Modified: Tue, 24 Dec 2024 22:24:22 GMT  
		Size: 26.8 MB (26814155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93ea70cd61df174dd95246fe25ebecd0647a34f857eacac6584407d547c6ea`  
		Last Modified: Tue, 24 Dec 2024 22:24:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab01e3a5f696452eb15e9a24d3d2ba29264aa68cb03e2a13be3363e69a7518a2`  
		Last Modified: Tue, 24 Dec 2024 22:24:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab7ef1b2953bb1ad114216f689ce3d87505ff61b6493e67a7d7d2bba15a873`  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f2a803b3a0fd5c90f90bd6c73b24061d68fb0fb113f0f1e0f1fe98c484019d`  
		Last Modified: Thu, 02 Jan 2025 19:31:47 GMT  
		Size: 16.2 MB (16166236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ac856b67030bd873586b58d0ba89d48aa5b57865d9279fac3e10ea87dc8438`  
		Last Modified: Thu, 02 Jan 2025 19:31:44 GMT  
		Size: 1.1 MB (1070359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8625903037b3355b79fcfdaa28044184fde5d14b459c847bda65a21fa21912`  
		Last Modified: Thu, 02 Jan 2025 19:31:45 GMT  
		Size: 17.7 MB (17697895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91fc48ba2bc4b356be88917d419e7a3c0fbd4c72d8a9147e696edc8e0cf6d83`  
		Last Modified: Thu, 02 Jan 2025 19:31:44 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efbcf4c3d74162e57bc0717af8022f995faef454397b751c209886b8aabcfb8`  
		Last Modified: Thu, 02 Jan 2025 19:31:46 GMT  
		Size: 18.0 MB (18012153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64c47304bea2433e082dc06ec5ca7dda1cc72d67c6531ddff5c307f335ce3ba`  
		Last Modified: Thu, 02 Jan 2025 19:31:45 GMT  
		Size: 3.8 KB (3817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755f6550037d1352ab586795be40f92cf824406af3b5abf084f4e657b64ed58c`  
		Last Modified: Thu, 02 Jan 2025 19:31:46 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:4d0962c72c1ac603a53aba5df0057fe206e7d8904ecf8e3b5a66c852cec350c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 KB (47908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d096939793035746050eb41f8bc98efde050d5e7b692aa74ec3fcf9e17165e7`

```dockerfile
```

-	Layers:
	-	`sha256:034e933a5226899c874b9dd2cdb7d3033cb5ec3ace69f9ab6fb5cfd199f102a3`  
		Last Modified: Tue, 07 Jan 2025 21:34:57 GMT  
		Size: 47.9 KB (47908 bytes)  
		MIME: application/vnd.in-toto+json
