## `friendica:rc-fpm`

```console
$ docker pull friendica@sha256:a15692ce3cf8e4fb1f05491fe8cc09fd8bc4a8540e430e1ed5ef23068e3e0eb3
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

### `friendica:rc-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:f93ea79a43566c0338e094c5f87ae9a803adde8904f12d3a94d75f33fd72e50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246712247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c451efc0d9178246fd768ed12fb2a47d415d0874c19bb096ab3008e9595574b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b986b853c7d68a21200eb17378b1ca8d0a57da767bf7fdbf916191b0a2d8633f`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295a75a3a91ff5f91f34813195a00644615dabcbdc8f30cbf8b03cc8630f4dc1`  
		Last Modified: Tue, 01 Jul 2025 02:24:14 GMT  
		Size: 104.3 MB (104331414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb72165b0b8e94fc9fad05eea2c3a4087a92a3bd0e4c866d595dde9d4192c49`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c01f77a2a658fa343656433f231651db8467c242861a9208fd098083f02e743`  
		Last Modified: Tue, 01 Jul 2025 02:24:08 GMT  
		Size: 12.7 MB (12664684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c1a91367e569651114a78a6ff0ade0c3c140a99b1c3b8aec68db2cbe41a70`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b46f190097194a6dc87cb5cf5a29045dc322bdea0cd170b2d77866aeca2ef`  
		Last Modified: Tue, 01 Jul 2025 02:24:09 GMT  
		Size: 27.8 MB (27827470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02da033c551838608e675a692849a97bee0806d4b21228d80ed703af8c018f`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eda985a7091d402a5c5c562b3606cec3c4eaf73470ebf832190b740bf414e4f`  
		Last Modified: Tue, 01 Jul 2025 02:24:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a967c5de143dbe20425ef844a3647654e96ea8a8ec85996673624d00699bf`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb04038cc4a9b13940a242856f2881f7ec666347560085c664b1ba8adee5d8`  
		Last Modified: Tue, 01 Jul 2025 02:24:08 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d24ff7851b296ccbfb660cdfcb1dc8550bb9f2bf6a92326f87c27faa0768c8`  
		Last Modified: Tue, 01 Jul 2025 03:24:55 GMT  
		Size: 18.4 MB (18384049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006b6dc7aed198c05eb7c4068d731033c1c482063905d8cbde32a9532acd1052`  
		Last Modified: Tue, 01 Jul 2025 03:24:53 GMT  
		Size: 1.1 MB (1103709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d58138090bf5b20b674f7c88581490e67d5c54cbcf8ea6bfaf66a4be1ea458`  
		Last Modified: Tue, 01 Jul 2025 03:24:56 GMT  
		Size: 35.8 MB (35829797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af890b47d06de92374096f7a5ae1dc224fcad5bd1bc63bf8d6b485ce652e204`  
		Last Modified: Tue, 01 Jul 2025 03:24:53 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47f0aa40a93021124b75473bf8a7eed5bb5b2eb1fb810eea5c4c6e092d3da0`  
		Last Modified: Tue, 01 Jul 2025 03:24:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4913219a4b1286c908697c5f0853980095dcd2a7b06ff357fb10fe7b5d25a73`  
		Last Modified: Tue, 01 Jul 2025 03:24:53 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9396d346382b5e612471e32d3a442e8501ee65865ac3dd28be137672e5dfd1`  
		Last Modified: Tue, 01 Jul 2025 03:24:55 GMT  
		Size: 18.3 MB (18321854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4924eac277b1a377ed17e46e6a0ecee7a78c759326ed0f92c94bb226d3335d64`  
		Last Modified: Tue, 01 Jul 2025 03:24:53 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8449074c304e0c24d5f9689760f3a79feb8ebb6e2f5dcd161c942f4a02161b`  
		Last Modified: Tue, 01 Jul 2025 03:24:53 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:b523b72c107c8388b49beed6ae7d7d0bf7eaf53883e57256cf8fb5b87ded7c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d0274cfec6aa4f41c43712f3db36e4f23bd2a04185b76e57014c8c7b048d84`

```dockerfile
```

-	Layers:
	-	`sha256:85e2630bb0f991aed630d3be3387a8cb8a7ff6a8f2d31e37a3d947ae69fc18a3`  
		Last Modified: Tue, 01 Jul 2025 05:28:48 GMT  
		Size: 59.2 KB (59176 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:0e3660ca43a2bc026979c609597ac9f6203b2f4aea4daa97e03c5a7c52faf240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215990793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fabed517ba09557cab22eb63d08cd9fe82524cc3513b80bc35ca1878180c68`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b05322491f7f224fdb6afd1a4feb0c269fe0910bd44e82e37a846aec3e465c`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b493a89b33667d984de07320c027ba0599d73427f434c8ec42c944a6bd4aa`  
		Last Modified: Tue, 01 Jul 2025 03:03:27 GMT  
		Size: 82.0 MB (81973614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef43b7ed80f2af53848f0179316741b5f6d73203876a5f0f62b038d570f6c8`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae01bf44a186a5dd593e5200a008bf6d3ea34fba3a2efb813c75da57508eb8e1`  
		Last Modified: Tue, 01 Jul 2025 03:48:34 GMT  
		Size: 12.7 MB (12662659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1db2166fad4250aea738304d0ad773d3afd3c1e644b85a83a5da6896db76c0`  
		Last Modified: Tue, 01 Jul 2025 03:48:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c17af07d401cbac6b90f5b289bd8047ae53967637b1b24212375368b115b719`  
		Last Modified: Tue, 01 Jul 2025 03:55:31 GMT  
		Size: 26.3 MB (26305723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c38b6318d6dd4ec441fef57444a979a28b0f52ba9818e1177c7d010087a50`  
		Last Modified: Tue, 01 Jul 2025 03:55:29 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e4042670e33bc4a8b95ad9a36c00fd2543a22bed5d4a9e7286fd97b36ab34`  
		Last Modified: Tue, 01 Jul 2025 03:55:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b62317e4e5dd829f11b615c476ffa064b4f802014f299c5d69923acc20a587`  
		Last Modified: Tue, 01 Jul 2025 03:55:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab49dc222c7d606ca874b858a843e30c4c626a36b310112308c1960e87f26b9b`  
		Last Modified: Tue, 01 Jul 2025 03:55:30 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f9fbbfe396abe26b3fc06518d2d2c43b514120c8e9370f7fbe76e437849800`  
		Last Modified: Tue, 01 Jul 2025 09:38:28 GMT  
		Size: 18.1 MB (18105149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4fcfe10fea09bda5b6514e22244fd9587edf63bf6f12c38793d474ea3a9a9c`  
		Last Modified: Tue, 01 Jul 2025 09:38:27 GMT  
		Size: 1.1 MB (1079195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4f3075bfda1b1b2b96ac566caaa4a4452e097aa19107c58a3743366f388008`  
		Last Modified: Tue, 01 Jul 2025 09:38:35 GMT  
		Size: 32.0 MB (32038533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470a83bbfa409707f97897d6b60bb380d571de5b9db10961735b24ea9b8daa86`  
		Last Modified: Tue, 01 Jul 2025 09:38:26 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed003aeaafaced0c0ee537edfe0f93448f51e5cc418c4cd11ad6d8c8d67889a`  
		Last Modified: Tue, 01 Jul 2025 09:38:27 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8babaacf2a255e2c00f4883e3ca399f91d23c9cc2d88e9a5b8dd8b2533e6cc37`  
		Last Modified: Tue, 01 Jul 2025 09:38:27 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bbf0b3849289b81f1b3646a1e48a18e995cac6c7780a7348ed264ce3991dfa`  
		Last Modified: Tue, 01 Jul 2025 09:39:56 GMT  
		Size: 18.0 MB (18044322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73435423a5b264c4a200a9bbec01dfe2e92191bf9b5ee0d09dabba96dbea67ab`  
		Last Modified: Thu, 26 Jun 2025 19:09:20 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be36c49bebdeb630e75638668dafafd9f00bed6d557b89b709873423700230be`  
		Last Modified: Tue, 01 Jul 2025 09:39:55 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:f34d29fa234bbcf3e3e6562fd0ebf490bf06a28709e28f31fb8022555e5f559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c49e345d46fa5141af1d6236d937def3ac523bbba526ab37fdeb15da20c64c2`

```dockerfile
```

-	Layers:
	-	`sha256:dd09730a299a77639bfa57098f2a617e18d93e568fe3932e054a8a8dedcc261a`  
		Last Modified: Tue, 01 Jul 2025 11:29:06 GMT  
		Size: 59.3 KB (59304 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:7ab50fa983369ea2d5c2bf90db351b0d85d47ae1d27bf9d9e5ac23df247b2ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205431233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ce607f0aa6200fca9eb900e1bd8934fd41502056afbbfa801c1a5e345b09fa`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd8dd9272c2deda3fe0036b7d36309c16f89e8e7e27eccc8a03fb68cdd395d`  
		Last Modified: Tue, 01 Jul 2025 04:00:35 GMT  
		Size: 12.7 MB (12662620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d0825cfe99539098b6cae5cdca3c89bdbe27b5d79d449068433330dccc5ce2`  
		Last Modified: Tue, 01 Jul 2025 04:00:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892a49c324b105a0450f4f731e40be52375945f984f84ba9b3dcb0eba714caf`  
		Last Modified: Tue, 01 Jul 2025 04:07:50 GMT  
		Size: 25.4 MB (25405949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a046cead5c72b8df9aebf052241961b2424d2232ec90665e9a5c23e6f046108`  
		Last Modified: Tue, 01 Jul 2025 04:07:39 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9983fc55315a3fa43b57af631cf207858b1c8704023bf7c39eb15eec17ad04f`  
		Last Modified: Tue, 01 Jul 2025 04:07:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f932421f6dd295486c1d874ed60d136db8b585a9479442005d0a011c01f48`  
		Last Modified: Tue, 01 Jul 2025 04:07:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4982234eaf27e3b41ab1119bc802204b1c01e913f2b32091fbca08118e7bf01`  
		Last Modified: Tue, 01 Jul 2025 04:07:43 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af817e94ddf8428eaa7582819a44e92f6c02ccbd8e1f5dea9bcd9414d04616c`  
		Last Modified: Tue, 01 Jul 2025 19:11:05 GMT  
		Size: 18.0 MB (18011291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a47a2697b4d9537deb832a07a3b7041a16a04872c785a890b718cb88e302fab`  
		Last Modified: Tue, 01 Jul 2025 19:11:01 GMT  
		Size: 1.1 MB (1069995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc0595593b1914c915a4264c543ac5899f51db49f151105e3c7575640a74ed`  
		Last Modified: Tue, 01 Jul 2025 19:11:05 GMT  
		Size: 30.3 MB (30295608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7136659935881403e609e39bf3c4e3989763cea43ccd6dd7e47c37748595a`  
		Last Modified: Tue, 01 Jul 2025 19:11:01 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559abd41387ae52a2d8d8cda661ad6c74696203fe4449f7fc8acddf44d3a3ef4`  
		Last Modified: Tue, 01 Jul 2025 19:11:01 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0c7724bd54f45a7551c3d4da91da621729e1306dc316f4a315ab6ec74c1a10`  
		Last Modified: Tue, 01 Jul 2025 19:11:02 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90b2b622a3b4c314a28db03b220e46c19b3dace9121b9e5cf723769bddf4a7f`  
		Last Modified: Tue, 01 Jul 2025 19:12:29 GMT  
		Size: 17.9 MB (17878269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e661f2fc71596eab097878a1c2cfa514ab0f1aeea7ef1d5a24afbfe84bf3ef`  
		Last Modified: Tue, 01 Jul 2025 19:12:23 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18704301fc08fea80d3c97e5ed16d374ac7566bb96344972c5c745ab24f822e`  
		Last Modified: Tue, 01 Jul 2025 19:12:23 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:e0e29f2636e740009fa4a80a84a18f306794a11e2488b9c7f6b05c2ab00d21d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f5a21fbfb2474170c63829a9194ccd6364283b9c1c13941274c0fd6cd7a312`

```dockerfile
```

-	Layers:
	-	`sha256:9a662cc6f882d408d6f32b5f327edd8c5c6575355f73eda4f3c4752fa4e3bb84`  
		Last Modified: Tue, 01 Jul 2025 20:28:14 GMT  
		Size: 59.3 KB (59304 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:e8ad6458fcd77bc5075ae06db7b5f63070d3915867d54f6fe1b1997235ab9f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237666381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae347ab1761f40b92c86d02f46bf6b48ce230c29a8e7c3c74034c650a0bd61c`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d77ea42fe176a612fa325478c432fd60345a9d1c25cfd2596bb9f769deddb`  
		Last Modified: Tue, 01 Jul 2025 04:40:35 GMT  
		Size: 12.7 MB (12664531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381f88af4e5bb2188e1c741e7fa55a98fdea51611706fd139998ec449626593`  
		Last Modified: Tue, 01 Jul 2025 04:40:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6733ce2400d959dc9de9319c809e7c9367861cc3e7f0d83c93c03cf596249`  
		Last Modified: Tue, 01 Jul 2025 04:48:57 GMT  
		Size: 27.8 MB (27815721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46232951dcae3827b80a484c987955a7f63f2db2207bd332b96a013d2a294c8`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35e5c8c4524ad3a2aaa8b03892ab1b5537a981a0f51aa8c095b17e9407e05a`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf3dc2bdfbd742fb067e2890e93aa40783c69ece95f52d45325df80b43849`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00adee5529ea98b4886bce6e9250cadd330cc16d7e4822fc72835cf28d07d83e`  
		Last Modified: Tue, 01 Jul 2025 04:48:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168cbc633c54909b5477c34602838166b724285ffb3c3185cd548da9d4d84d9a`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 18.2 MB (18153450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3049bdd992c1e3489cf31a1667d59845101087c9d6c7e4bf2fa15f0550fd8bd0`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 1.0 MB (1036020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f51d6e7355e7ffb4b0ce851f0b3e409ce3a132ed4ba2e2a4618f8d2aca5dc`  
		Last Modified: Tue, 01 Jul 2025 14:22:26 GMT  
		Size: 33.6 MB (33646346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20d25ea391ec8ffa14d8e735bf9f814553e7fd525bb4b1cd8e12d0af861f2e4`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07271e0f64aed8cd1781b99034e9107415f718f600a141822f7271f3a4bf0d07`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdd7b8fe4b19c205fa226c2ed2d289a2b9bfb4a5a5039d2bf9d4f97ba96d950`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558f965bab6ff43c937dcde9eccdeb2b2f1aefb4d7f29ed608b67a19a809277f`  
		Last Modified: Tue, 01 Jul 2025 14:22:25 GMT  
		Size: 18.1 MB (18122855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a923acb7ca4bfd2ae770a6c826937f320366f1d4c47104d6398838b3ac6d7d`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cb946b2b1c229a9c28b1ab2ca385e9a3a400db38d5d04ede5617c8b1b16bc4`  
		Last Modified: Tue, 01 Jul 2025 14:22:24 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:86205071af3b91dc04218002a612ee7ffae9a6b82bda542eed259583a7a22015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1631cdb58ffb97f938e62645b44ede9afa91ce83ba25bec71b2fe605dbfbf3e`

```dockerfile
```

-	Layers:
	-	`sha256:4fcf444a3959124c682064c4b4abb3b99b5c6100710f0a23ed4792d30717c077`  
		Last Modified: Tue, 01 Jul 2025 17:28:03 GMT  
		Size: 59.3 KB (59336 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; 386

```console
$ docker pull friendica@sha256:463485e658da9793852fba018a0bd28c6d2580349d5f8e31d52a272a49a866fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245870347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80a256a25311b9b45b90ecd67824ad52f3b09edba07b2c828769183b0d37e46`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208d45de7dfd917ed8f40d4093b493768c4b0cbcf35577fe1ac13fdbde5b18c9`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b51fe9cca38fc5f045d0e6194c628fd9a8ddc008549837701f6a4fac3fed9e`  
		Last Modified: Tue, 01 Jul 2025 02:20:04 GMT  
		Size: 101.5 MB (101515122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a98c8659e1991fd6d00c45097475da18db9e844662a8b7e8770c42227abe64`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d195a01c27282f0402501b094be9b79c346a1d1916c690336cec605c0f708b9`  
		Last Modified: Tue, 01 Jul 2025 02:20:00 GMT  
		Size: 12.7 MB (12663750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b9f51c243086ac493b9f8fd60802178a550a854f59c82de039bcc2e2e2d1c`  
		Last Modified: Tue, 01 Jul 2025 02:19:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29845d7b28a1879fe589cf9305eb39744c1003bc131fb9382134fc1f037986a`  
		Last Modified: Tue, 01 Jul 2025 02:20:00 GMT  
		Size: 28.3 MB (28337321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31f3912fb44c5493fb0452eafb243b2c426ef5e622ec08f6e9adbcc4451c8bd`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0743a834d375589bd01c1e82fc50cb558e95114bed621713235dae1ae0ba3`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dff81f7275f0fa98afc1eb8b1119fd1e01696bcc01bd5c0b4a90fedd959e72e`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4344be67fdc968ae25fdde02e2c6c17f3b07ee12b0f5761b8dface7a336c1db7`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec8695c66eaae60cc002069c9be6b16dccd0a4164a00bdca53a9381e7a031be`  
		Last Modified: Tue, 01 Jul 2025 03:24:41 GMT  
		Size: 18.9 MB (18888288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a42ee2f214c0b4e37efc6683661025e6fb72673d9b8f813260f1b21fd92d4`  
		Last Modified: Tue, 01 Jul 2025 03:24:41 GMT  
		Size: 1.1 MB (1078632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b51c1822d8c9c1a5ee2439a7f295cb7a92986dfb420f43ea5a9392ffd18f84`  
		Last Modified: Tue, 01 Jul 2025 03:24:43 GMT  
		Size: 35.2 MB (35161860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e67cd372e78f600ff9d7b7ecd44e7bd5402027731c99eca381524c23a3f7a5`  
		Last Modified: Tue, 01 Jul 2025 03:24:40 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3595b8b28a0f322dcd75720882d495a9cbac97f3007b2389b5c56e53f3637fc3`  
		Last Modified: Tue, 01 Jul 2025 03:24:40 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d49ca978d6e862c6c957de843083fdefaae10408fae1ca0613c09c7f24b644e`  
		Last Modified: Tue, 01 Jul 2025 03:24:40 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e843ccb65221777716765eba69908322d0b3f1b206b7a9ed503e2840ff1b04ad`  
		Last Modified: Tue, 01 Jul 2025 03:24:42 GMT  
		Size: 19.0 MB (18993817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e49915b1b521696b77a0c35c84a0a11e4a0ea552a8eb21520fdad8465cb2582`  
		Last Modified: Tue, 01 Jul 2025 03:24:40 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67ac4ac9c463e6ed2b280bdc8ce601e2525d3cd712bb11f6f8c9a795447cdd4`  
		Last Modified: Tue, 01 Jul 2025 03:24:40 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:dfcd5ab575598a041464ee381f217b391696dd2c31515983343e771d144b69af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118599a91d8818f2f6f391f66ffc8a9a4cd8de5eaeeeb3f9671325aecff26977`

```dockerfile
```

-	Layers:
	-	`sha256:8606a4674b808dc3d516483d9779c143073efa530e682a206b70c9c6b29764f4`  
		Last Modified: Tue, 01 Jul 2025 05:29:02 GMT  
		Size: 59.1 KB (59142 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:c89c070c35cb0701f596ff8b70fd6d67e1dcb3f24392f80ae06c98e202b23055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218128305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597747cb3dd138ceadff99ee345d62ef5ee9643d3dd793488df536d36d58b96f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5e69eb612928f2b1edb8b79310fa7eb01b97eda1179aabfcea5395120a404`  
		Last Modified: Tue, 01 Jul 2025 04:33:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c6c65191f30a3311d0f913382becc510cfefba81063f7617c9b537f70c6f7`  
		Last Modified: Tue, 01 Jul 2025 04:33:43 GMT  
		Size: 80.7 MB (80668384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bdcd15545dd72fcd7e549e199c0795e04a22a395d9ecc76e94dbc2d57e32d7`  
		Last Modified: Tue, 01 Jul 2025 04:33:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92df7f7537be112e92e4e717ea513c5ce5c39569a633c6b2dbf90528f6ab070`  
		Last Modified: Tue, 01 Jul 2025 08:08:28 GMT  
		Size: 12.7 MB (12662216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745d8f1c45194c73eed831ab67d1b34bc45917fb45e814d0b5cbaad59630319c`  
		Last Modified: Tue, 01 Jul 2025 08:08:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c45320afca05a86f635b5f2241a416eb436645ec3cd24ee71231a3ecdebcf33`  
		Last Modified: Tue, 01 Jul 2025 08:42:28 GMT  
		Size: 26.9 MB (26917080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbf6619be3f17b44edf44a72c4438876c1e2f7c519fcb524066144f2dc6e565`  
		Last Modified: Tue, 01 Jul 2025 08:42:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed71572d2a4b56500c4b309654504dbc5de0227d07596b0b8ddb377f1c4e54df`  
		Last Modified: Tue, 01 Jul 2025 08:42:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510479dc4837ae3f572dffc4e55c26e544003569eb7686a69b053d786d1d3817`  
		Last Modified: Tue, 01 Jul 2025 08:42:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f47ea60fe44235e9397e13999f6e6c08a7b767fcffa97d50e56d1756bef464`  
		Last Modified: Tue, 01 Jul 2025 08:42:26 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9dcc40a680ff9ccd1f03e73dcb046bcb1f386f31ea1c9eb11775d2583777e`  
		Last Modified: Wed, 02 Jul 2025 03:39:43 GMT  
		Size: 17.6 MB (17634000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f43edf69bd03ae627014cd40e309b5eb2614122b07271c32afa13affb4aa2`  
		Last Modified: Wed, 02 Jul 2025 03:39:43 GMT  
		Size: 989.5 KB (989491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae265983c49c597c4e93c5d49ec8072facff81dfe757c213b17f246ee0f4ecaf`  
		Last Modified: Wed, 02 Jul 2025 03:39:45 GMT  
		Size: 32.9 MB (32907679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743bbbea7e26aa8fce4d8d0525475315fa979b2c56123ecd2b2f8d2224fe2e31`  
		Last Modified: Wed, 02 Jul 2025 03:39:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a034bd88d6158085b4dbb1a8087222bf49123095729956bed9082221b77757`  
		Last Modified: Wed, 02 Jul 2025 03:39:42 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06bdb99ffb4223e65886fdd49e6a2860580edb92f9d0b7db01994bd5195cb15`  
		Last Modified: Wed, 02 Jul 2025 03:39:42 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36baf330c06d6a92ef97c81937c62960ca1971b41054031b225b66365a1232d4`  
		Last Modified: Wed, 02 Jul 2025 03:46:12 GMT  
		Size: 17.8 MB (17813577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902246db8e1f95c3758336333fe559675928f9bcdf5d3ed98fc2b53b9498bc25`  
		Last Modified: Wed, 02 Jul 2025 03:46:11 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c555926be6bdebe5f30d2e216a906f57ab3cae8cb4564f31a3f14b22a0bb4733`  
		Last Modified: Wed, 02 Jul 2025 03:46:11 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:afba5317fe6cea95274c144cee57050f038d0e34a9a1a666d6d6a6a89e9081fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92276e9920e3f10f1bab16792914e76674c4a674cb32d988d3c9277e8519feb9`

```dockerfile
```

-	Layers:
	-	`sha256:eaf12806d51c34cdc218ee786fcc895b99ab9c835d55d30a230d0361903aa76d`  
		Last Modified: Wed, 02 Jul 2025 05:28:21 GMT  
		Size: 59.2 KB (59224 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:d0e64a58c634daa613ca7a50762d66c11d85f164c17dcd834cc937ec6e9faf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250877588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6810f9ca1962cae1b4d893437a8b9b554b2f8a536f90576625acd6c8d29587`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceff3d73088eb90a29a3888d344cedd86858df29b36df7932d3fe0d16eda4e7d`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08259e2c7cacc0405f0da4ea7142f0be36234c1b63d584779538944c8319235f`  
		Last Modified: Tue, 01 Jul 2025 02:58:21 GMT  
		Size: 103.3 MB (103326709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fcb5df575fa0806e458d09147e66250dc80c744fe65c46881d5d2395c98374`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed11498eee63906d06a0d4f4eb4f2f82fd8c136b83c10cf0ff318d8f1842d4`  
		Last Modified: Tue, 01 Jul 2025 03:46:05 GMT  
		Size: 12.7 MB (12664075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bd8237575b0bc18f7c1a004275025cdfebf43c3f6280a2a7a6222d6ac2053e`  
		Last Modified: Tue, 01 Jul 2025 03:46:04 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9057d3e1b39a6343b4e2c6ef433175c143f6bf367a4f20ef79de7d9b29b320b`  
		Last Modified: Tue, 01 Jul 2025 03:54:08 GMT  
		Size: 28.9 MB (28894401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e480cee0386b2ef518dc619d80b651cfae5171bc6fea791d47f270723b7bf9da`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702178c015d87efb844dbaff0d3aecd971dd92f3342296d38fdbc2fbce8bba41`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2381189dee0ebf13131823e08eb6a1cf8c43cce44e49869b7188b4c040ac5`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbdca9dfee4dcf2604ef3810826a5e568264b320a38cc110c668a4b12627d6`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f0cf3d78364c19647d0f0470789e06b3216bcb613e9ae3cca6eccc4ebbfbe5`  
		Last Modified: Tue, 01 Jul 2025 11:14:00 GMT  
		Size: 18.5 MB (18465912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832213dc6cac13ff0858119bf89a200e47cf24c6458360b0e287086ae5f77fa1`  
		Last Modified: Tue, 01 Jul 2025 11:13:58 GMT  
		Size: 1.0 MB (1025981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcdd4b130da54613956c2d2eae68f791f19ff2cf74276349878792727e87c01`  
		Last Modified: Tue, 01 Jul 2025 11:14:03 GMT  
		Size: 35.8 MB (35802652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f0956241f32735c47745bcd01512f44d95cb617c2beb9ebd72fc42f713070`  
		Last Modified: Tue, 01 Jul 2025 11:13:59 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b399f691dad418dbd2880c91ec818d65f00a2e2cc5d3ae538307bbe5d32725da`  
		Last Modified: Tue, 01 Jul 2025 11:14:00 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ea7590a9433ba746f7835fdb488cd751133a24f5f394171e46502cbf868c4`  
		Last Modified: Tue, 01 Jul 2025 11:14:00 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a27155f828e808cc8fabef41e285193d4ea3e3472302e6dfcef03a5250eeac`  
		Last Modified: Tue, 01 Jul 2025 11:14:02 GMT  
		Size: 18.6 MB (18605910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a109a197ba039f47c71c58233d41cbe166558446bd79aef87a2090d5091e5`  
		Last Modified: Tue, 01 Jul 2025 11:14:01 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadc5e8ee2f2de925bdbb5bfcdb556655d59169f88ae85a3f45cf2613ef30733`  
		Last Modified: Tue, 01 Jul 2025 11:14:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:d541fe071e24f652a5cf4a9c8f62e8cb4ce2dd43ce2ff82fa83df187fdb3b93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d02e438761967b0a36991ffba64ee971da304eea873992f58b9e0e0c33b67a`

```dockerfile
```

-	Layers:
	-	`sha256:c4972d3768c5913887e9cdd409c7268ed9fbc9f7914fd2b7f6bbafc342e3ccdf`  
		Last Modified: Tue, 01 Jul 2025 14:28:18 GMT  
		Size: 59.2 KB (59220 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:7042e1cdeef68a306e2d22b493bb9107e4fbf488d7c4473aa473c57ebdc27172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215522057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f2c0014d8f5a18573451ea367bba4e201881f723b61c8877964bfe5ecfb9e1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9c297e4e0ff6968c351ba2bf1e5702e339d74da6d2ee401d883eb8eac205b`  
		Last Modified: Tue, 01 Jul 2025 02:42:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2414908a592d42e715071983fa5a673dbdbf81c963b83bc36a868149c796848a`  
		Last Modified: Tue, 01 Jul 2025 02:42:09 GMT  
		Size: 80.8 MB (80825948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f41513cce80c0dd493bac0e1dfabcb8d66fd1eda3cc802fee9e00d745a700`  
		Last Modified: Tue, 01 Jul 2025 02:42:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a710affcdf491a329bc925c8c87aa62de4b3bd7d946933c08973b1caced9d3a7`  
		Last Modified: Tue, 01 Jul 2025 03:23:31 GMT  
		Size: 12.7 MB (12662980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe47688d0e94200a5b4cdc46404b2fd582481e8e83dbbbe7873b0c5a42e5e53`  
		Last Modified: Tue, 01 Jul 2025 03:23:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a562dcf13254244ee1693ecd265dd678746774c7994fb9b5dfb7ddb312d8237b`  
		Last Modified: Tue, 01 Jul 2025 03:33:35 GMT  
		Size: 26.9 MB (26928296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf827c18b3aaea085cf26d29bde281c198b7db1b12f24d1687a0731f0f795a52`  
		Last Modified: Tue, 01 Jul 2025 03:33:34 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4f7db203f56678bfe531b40b5ac8d8f5a471e9a4a601fdf36c5981bb9c6e69`  
		Last Modified: Tue, 01 Jul 2025 03:33:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6416e77ac7c89b8026d07ddc7dd6b6428a1aab64e126cb955a45f5b4af7365ca`  
		Last Modified: Tue, 01 Jul 2025 03:33:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e524b6e5230c48621e2a229f1aec11a8b9c902274c6daf8fe7a59c622bc4ee2e`  
		Last Modified: Tue, 01 Jul 2025 03:33:33 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2cc2525373d3a072a89924a4af6618d02ea792ba8860d5f72fdf5c063ba98b`  
		Last Modified: Tue, 01 Jul 2025 09:29:10 GMT  
		Size: 17.7 MB (17651614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b275dd160db2d27ad6f031ef06950f7684c900bf17c710f3952dd590b9b1`  
		Last Modified: Tue, 01 Jul 2025 09:29:09 GMT  
		Size: 1.1 MB (1068361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5617aa71f1c386b7859901b0b3ff3a958f86127ed95e0f555a51a86a1fb11c01`  
		Last Modified: Tue, 01 Jul 2025 09:29:13 GMT  
		Size: 31.9 MB (31877743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6360c84eca4ca472507ca8c96ad70abbd5ba2c245f9827c7b7290027799a`  
		Last Modified: Tue, 01 Jul 2025 09:29:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f8a000db036bdce1a5cea07b5ade1802d9ad37906d8dcba2a0f5114ef541a4`  
		Last Modified: Tue, 01 Jul 2025 09:29:09 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fc25b71f9c027fd13c2a87bb3625cee21ff946b8e83a72e6cb249474d221e1`  
		Last Modified: Tue, 01 Jul 2025 09:29:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f143dad4c30ffb769fd45f3c6b00e4f014f78412258dc158e4c761997d81642c`  
		Last Modified: Tue, 01 Jul 2025 09:29:11 GMT  
		Size: 17.6 MB (17600182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0bd92424e2ef6da99d044f335ec73c477d23c96ba4d5273bda3e44bbe27dab`  
		Last Modified: Tue, 01 Jul 2025 09:29:10 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8407a35d9dad70db2f9f450c6942d455871e0a09b1eb4d50cb51b628b7bf32cb`  
		Last Modified: Tue, 01 Jul 2025 09:29:10 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:7a94288991165b7b63f5cdf154379eeb31c23d3834aef19c87db6122d4f7a49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6e066008f31227564f43167ca6d3b0e3729df3e6b832916d48665f21814d25`

```dockerfile
```

-	Layers:
	-	`sha256:1943d88e101047c6ce28ed7f7d3cc0f572ec82c162799081a51cc41f7c63eb92`  
		Last Modified: Tue, 01 Jul 2025 11:29:19 GMT  
		Size: 59.2 KB (59166 bytes)  
		MIME: application/vnd.in-toto+json
