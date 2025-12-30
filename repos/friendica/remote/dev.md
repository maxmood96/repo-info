## `friendica:dev`

```console
$ docker pull friendica@sha256:24c92ebfb552f81f8c58a619647838c6c412b8c8fdba9d7ce61c9f8f75305a90
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
$ docker pull friendica@sha256:bcd585613f9d55007b387d6bd5b59e4b7eedd465e7e5bdb3f81fbb1df2a16aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250606464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e012e0bedfb633bd51d338c24801104d4b983a879dff33dc812702619465b1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 18 Dec 2025 21:11:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Dec 2025 21:12:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Dec 2025 21:12:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 21:12:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:12:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:12:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Dec 2025 21:12:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Dec 2025 21:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Dec 2025 21:12:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Dec 2025 21:12:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:12:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_VERSION=8.3.29
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 21:12:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Dec 2025 21:12:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:15:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 21:15:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:15:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:15:08 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Dec 2025 21:15:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:08 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 21:15:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 21:15:08 GMT
CMD ["apache2-foreground"]
# Thu, 18 Dec 2025 22:08:40 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 18 Dec 2025 22:08:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Dec 2025 22:08:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:11:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 22:11:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Dec 2025 22:11:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Dec 2025 22:11:16 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 18 Dec 2025 22:11:16 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 18 Dec 2025 22:11:16 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 18 Dec 2025 22:11:16 GMT
VOLUME [/var/www/html]
# Thu, 18 Dec 2025 22:11:16 GMT
VOLUME [/var/www/data]
# Thu, 18 Dec 2025 22:11:16 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 18 Dec 2025 22:11:16 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 18 Dec 2025 22:11:16 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 18 Dec 2025 22:11:21 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 18 Dec 2025 22:11:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 18 Dec 2025 22:11:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 18 Dec 2025 22:11:21 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 18 Dec 2025 22:11:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfe25a912f5ab05cbb20494844dd61ebb15dc892181c263581af50f47133a1`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076365cdea37296d5f771b9a0b4d3076450af5a93d4ae278850fa785d1d2b51d`  
		Last Modified: Thu, 18 Dec 2025 21:15:51 GMT  
		Size: 104.3 MB (104330765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04612d4ac7de8ac0784bb9936a2f160a919c7391151b1d6a2c58480b1fea1e1e`  
		Last Modified: Thu, 18 Dec 2025 21:15:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dab85d2dad9be2b7f94b40aa337fe0fe9bcfcc588a2fb576b39426ca0f392c8`  
		Last Modified: Thu, 18 Dec 2025 21:15:42 GMT  
		Size: 20.1 MB (20131840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4324ba2c98ed296eaa276bafc8a649b8c450c4d897b64aae5a94d1646b2ee7bf`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0fada9ee2d3b9266822f6862b63e6932d33d1099d9dc5c4ec894c51ae8831`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95566c0c5f2d2a6ecd560ef066c38d64747fb041bf026e0892e9244036a426`  
		Last Modified: Thu, 18 Dec 2025 21:15:41 GMT  
		Size: 12.7 MB (12731101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e1fde7a4949bb320a12d01638e3565f115660704ad8c878d4d7ef77f676374`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e448cec5715a3d302053a86acfe24082f145c067bca1f8edc4657e74fd0f1f07`  
		Last Modified: Thu, 18 Dec 2025 21:15:42 GMT  
		Size: 11.7 MB (11673924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b71eced8bbe90d88746e4b15fe724b17c623112b13dbc2d089866592ab4999`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5418bcc314407a224e819e31f0c4c192604dbb1d1407e01165678ad09932cd`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce325de83eb02fd5dbb4fb9dbe69460e546b464073006120516aba5838f29e3`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296b9cfd39f85740e478db5bd079b1253c466a97c53808329e339c044125e8da`  
		Last Modified: Thu, 18 Dec 2025 21:15:40 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e236e6a7f42d8feeaa15d89be806fd1e24cd2adf82258fc7f92a4d6b9945b3`  
		Last Modified: Thu, 18 Dec 2025 22:11:39 GMT  
		Size: 18.5 MB (18460107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6b473068a98a187bc6288549ad0912be83c336239c5900fb9fe5cb71d65039`  
		Last Modified: Thu, 18 Dec 2025 22:11:36 GMT  
		Size: 1.1 MB (1127328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17057ce1a29888bd4b719ca3b65a518ae20c4930d1e2ad69947148da8ee00cef`  
		Last Modified: Thu, 18 Dec 2025 22:11:40 GMT  
		Size: 35.5 MB (35523370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca765c1d45b8ac3a8e7f5363b0b44035b905ebbd10633a45943db37465f0bef`  
		Last Modified: Thu, 18 Dec 2025 22:11:36 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c4f482f50dcfe074aabe0a828cc29a16d76b8bc51e5af12954d5bc13bee37`  
		Last Modified: Thu, 18 Dec 2025 22:11:36 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f088cdc009d94242fca58cac02939da9a09592b89f279e139cdf9293a87e393`  
		Last Modified: Thu, 18 Dec 2025 22:11:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2812534c5d55d4df514197c8ecc7eac0ecfcc892bf17afe0dca2bf17c07305`  
		Last Modified: Thu, 18 Dec 2025 22:11:39 GMT  
		Size: 18.4 MB (18387790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535b4f3fd58cdd17fbbf757132ebcc24d66c1f1b97a5eb766ad03aba171c0d8e`  
		Last Modified: Thu, 18 Dec 2025 22:11:37 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9d73fe2d18b7ca3f3a4d64cd20ea5dcb6fd694ce9f512719441afe77ff20f3`  
		Last Modified: Thu, 18 Dec 2025 22:11:37 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:c49217d21cfc3066335f0659c8a1f0f0b3cf3ea8ee0227245cded86a1e9084e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120af45ccf7647ad089878a5b06754655366b5a61c256ed96566e7b6ee31e610`

```dockerfile
```

-	Layers:
	-	`sha256:accf3be2b86acc023ab969ba43ca0236764b8934d141889928cbf369217a3f44`  
		Last Modified: Fri, 19 Dec 2025 00:28:11 GMT  
		Size: 65.8 KB (65824 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm variant v5

```console
$ docker pull friendica@sha256:cf07286d65c367b6d9076fb7cd888f513f897283b6d98aec89f2598b16613534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4460b13df98540d0eb327570355cd06bc255a4f2b5f61c7dbf82eac330ce9d1f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:27:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:27:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:27:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:39:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:39:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:39:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:39:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:39:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:39:25 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:39:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:39:25 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:39:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:39:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:42:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:42:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:42:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:42:12 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:42:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:13 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:42:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:42:13 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:51:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 01:51:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 01:51:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 01:54:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:54:13 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 01:54:13 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 01:54:13 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 01:54:13 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 30 Dec 2025 01:54:13 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 01:54:13 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 01:54:13 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 01:54:13 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 01:54:13 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 01:54:13 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 01:54:20 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 01:54:20 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 01:54:20 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 01:54:20 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 01:54:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f97031cc0903f8827aac976789084398aadbed7f99e435ce3de7cf606030`  
		Last Modified: Mon, 29 Dec 2025 23:31:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67fe54ec01fe179525f1b1df639481f49413431aaadd290ce3e255a1d969a35`  
		Last Modified: Mon, 29 Dec 2025 23:31:16 GMT  
		Size: 82.0 MB (81981639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e20529c73c782359388eb687cf687f058ae85ec46f9347f68197f5cc25cb2c`  
		Last Modified: Mon, 29 Dec 2025 23:31:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be03716a46ecb780b0f8e329d120446ef4ccd632313fd6ecb73e297d47c13f5`  
		Last Modified: Mon, 29 Dec 2025 23:42:33 GMT  
		Size: 19.4 MB (19422422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f86cf66437b24228ac4b65f8016dffb16199292e68e833359c5646fc9c6be80`  
		Last Modified: Mon, 29 Dec 2025 23:42:32 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fdfb80f306f36659ed980b021af27c6f95cfebff3fb305f0061d5a730c5660`  
		Last Modified: Mon, 29 Dec 2025 23:42:32 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcd8f5a782471ce4c72794cd00ad7da81f49d7d8a0dbb1e5261c83e4257001e`  
		Last Modified: Mon, 29 Dec 2025 23:42:32 GMT  
		Size: 12.7 MB (12729315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e074bfaa3cc6be00e85f8bdd4c10ef01d26b841fc416b06db55eabde86e038cc`  
		Last Modified: Mon, 29 Dec 2025 23:42:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfedde8b850285f4b426e5dc1d2858f15a31c48f60074404c5cfa4c76c8d025`  
		Last Modified: Mon, 29 Dec 2025 23:42:33 GMT  
		Size: 10.6 MB (10632090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9189882e5177eed6621369d2f4dacb3ab6f072f92db937e98c18e376f390b128`  
		Last Modified: Mon, 29 Dec 2025 23:42:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4506bd13134734a706b33a6c1d9923308d037f04c4030d8a367bcb8ce69efcf4`  
		Last Modified: Mon, 29 Dec 2025 23:42:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af489da170f87e2428d09c6853adcb8e4fc4b6a724c5ddda6ff1229ae54c036f`  
		Last Modified: Mon, 29 Dec 2025 23:42:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c345161d1baac1ae10f0fabd720a1f17bbd1fcb5431bac8404f785db239f280`  
		Last Modified: Mon, 29 Dec 2025 23:42:32 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208bde9db1be0836c7a9593ce60351942cf71ad59f5500ce8699ea46221ee5a4`  
		Last Modified: Tue, 30 Dec 2025 01:54:38 GMT  
		Size: 18.2 MB (18196376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a389b656009c49b43a31948a17fe16fbb6280dfc33537970b9b9d70398001c`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 1.1 MB (1102769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1fe63022529da35c4deb71bef5ba2a249d9f6d4911d30f8995bf64800302d1`  
		Last Modified: Tue, 30 Dec 2025 01:54:39 GMT  
		Size: 31.8 MB (31768941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a958d5a4e058535cd18202c8ee88d339d5247eecedef773e984b17f48307e9`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9257758f644457bde5b6b1c5e833eb4bf654bf3455d1f8957a9d69c5864a9ea`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85db73f616f6114d92e0f1f02c015cc20f84698b9a53a5972be00107c75fc1a`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ca03347e889bb9b540eb102664b7624f792b49147bf61ec651c108357d7b3f`  
		Last Modified: Tue, 30 Dec 2025 01:54:38 GMT  
		Size: 18.1 MB (18111777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206af7e6693fd7b7447bfefe58f770f57a4c97bff49ca0e150043dbd73290f9c`  
		Last Modified: Tue, 30 Dec 2025 01:54:33 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111df85f8c143e534fee135c820b6eacbf675e899186d33fa4a1c278d1a71242`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:4994b156b2ff51535b68cce85fa7d3a756de8f77f01d4d8c8bc60abc23659888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937fecfdc6f0fa860d93c65655eaa8725c0881ecd9a5e3c2dbc4bb74ffd9e6b1`

```dockerfile
```

-	Layers:
	-	`sha256:bc52ac51fc08be1f1b71ce203d7315a2c737927c7c7f45d402f228325efffc28`  
		Last Modified: Tue, 30 Dec 2025 03:29:44 GMT  
		Size: 66.0 KB (65972 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm variant v7

```console
$ docker pull friendica@sha256:f574cc2f5afb8ef0ce79e35af6f2c47150e6294e7a8b19b37877a095b49116a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208943425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1463487f441bd367b75db9d6e84bc9a09d50ff352d4e25444b83fd48c102fa5`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:40:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:40:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:40:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:40:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:40:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:40:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:40:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:40:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:43:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:43:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:43:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:43:19 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:43:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:19 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:43:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:43:19 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 02:11:20 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 02:11:31 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 02:11:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 02:14:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:14:19 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 02:14:19 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 02:14:19 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 02:14:19 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 30 Dec 2025 02:14:19 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 02:14:19 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 02:14:19 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 02:14:19 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 02:14:19 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 02:14:19 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 02:14:24 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 02:14:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 02:14:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 02:14:24 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 02:14:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dc54cdce217b9954ad67bbb3ad27c4e3bc5c648c366c49405b5888f7b393`  
		Last Modified: Mon, 29 Dec 2025 23:43:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3c27645a380ab3527501d49a6633b054d4857e0a19e4cb1e0978f4faf593eb`  
		Last Modified: Mon, 29 Dec 2025 23:43:52 GMT  
		Size: 76.1 MB (76148835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d58830b6b6ec9f074ba36aa3cf48f4f46100ebd3a0a648cd6c2cd01ef0f226`  
		Last Modified: Mon, 29 Dec 2025 23:43:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff87f2da8d3b1e101a06c22d740f9476207a98c60e5e194de28d05c54788db25`  
		Last Modified: Mon, 29 Dec 2025 23:43:47 GMT  
		Size: 18.9 MB (18860005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8cbfc0d2e51aa0b4fcaea0d6d1b9e635ca933c893dcc380a7003de40b6c4b9`  
		Last Modified: Mon, 29 Dec 2025 23:43:45 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3747beb91bf129824912cab0335ceb0c545eba4b92cc3efd5ca96252f78949b4`  
		Last Modified: Mon, 29 Dec 2025 23:43:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d845005dd2ce77f5315156d8d78381762c5892407ad0bb6d03f03eabfcd8e69`  
		Last Modified: Mon, 29 Dec 2025 23:43:47 GMT  
		Size: 12.7 MB (12729192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f9bc7dc1f66133323e44ba67769fa63e8a063790f9fdcf6be28fd43a149`  
		Last Modified: Mon, 29 Dec 2025 23:43:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c1d440d879e6a111dfc53058bc576621f06f1128842c02e5e440ab0c96122d`  
		Last Modified: Mon, 29 Dec 2025 23:43:46 GMT  
		Size: 10.1 MB (10066871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf723f6617fe69f6c139a718a1ec48add5de3032e9bf313fc40b50073f2f7a0`  
		Last Modified: Mon, 29 Dec 2025 23:43:45 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546b5dc1f088bc0062169c088bce41676eef2bccbfbef75969d65476414a9381`  
		Last Modified: Mon, 29 Dec 2025 23:43:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc591fcb16be3ebf6976451990693a082242b4452f991369fe8801d75f7d5f10`  
		Last Modified: Mon, 29 Dec 2025 23:43:46 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eba14f573d200340a8c1aee1d226cff3e0fa08347f000b80eb8a57c91c592f`  
		Last Modified: Mon, 29 Dec 2025 23:43:46 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5600ad0b66f975d4500f904393f4fa8e5592fffcce19029a8a25a497a4ebb49`  
		Last Modified: Tue, 30 Dec 2025 02:14:47 GMT  
		Size: 18.1 MB (18097369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34add7b37f3e3fbdbbc4cb6c9187e950c026033d842168e2159387656a88a963`  
		Last Modified: Tue, 30 Dec 2025 02:14:38 GMT  
		Size: 1.1 MB (1093244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6dd3cc2d40ac301623d839dbeda4d12f23a76ca74e3e654fe6b2d4211d33ba`  
		Last Modified: Tue, 30 Dec 2025 02:14:41 GMT  
		Size: 30.1 MB (30054753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e0a4c2a887323eeaa90f1f9bfdd1ee722763c2b65b43e1aaf94a9f7aab90a4`  
		Last Modified: Tue, 30 Dec 2025 02:14:38 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86afb2ee8226b21af3aa41278d59a811264ee19f2766894f630dbd040081d76`  
		Last Modified: Tue, 30 Dec 2025 02:14:38 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccb21c1dbbc4181388a445826c343500e9f19d3438a938cee72d54dfbdc2b33`  
		Last Modified: Tue, 30 Dec 2025 02:14:38 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb8f32f5876774f4187b0c126e9cbbf561b641fd1256a764fa97eccfba6a43`  
		Last Modified: Tue, 30 Dec 2025 02:14:40 GMT  
		Size: 17.9 MB (17947284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453ec139f444d322df1cab2a1ffbfac4d47d48ee06f06c14730f09ff56a782a3`  
		Last Modified: Tue, 30 Dec 2025 02:14:38 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098b839ae547d055771d17ae4a3c53fc8823177d3de511310db3adcba829f4c1`  
		Last Modified: Tue, 30 Dec 2025 02:14:38 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:4fcd83894701be107ea417e1445675f3485feed84d303fa8bfe96dd11f333a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaf0f237eada2c531a6092eea633d789a2d4b028cf500c224a929a21d7d62e8`

```dockerfile
```

-	Layers:
	-	`sha256:46bc0335d4d49ebd421651321e9e33fc05dd31d62bd6a7679856bdadb09b03f7`  
		Last Modified: Tue, 30 Dec 2025 03:29:47 GMT  
		Size: 66.0 KB (65972 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:5a14b81a2da4ab6e91a702cb5487cc9bcaef7d52f7d10ed28cb8178afddcac30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241742607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f838d9063613de7b7bf6c275021245d1dded595215ee0426cc7c106a1c98441f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 18 Dec 2025 21:12:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Dec 2025 21:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 21:12:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:12:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:12:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Dec 2025 21:12:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Dec 2025 21:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Dec 2025 21:12:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Dec 2025 21:12:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Dec 2025 21:12:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:12:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:12:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:12:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Dec 2025 21:12:26 GMT
ENV PHP_VERSION=8.3.29
# Thu, 18 Dec 2025 21:12:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Thu, 18 Dec 2025 21:12:26 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 21:12:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Dec 2025 21:12:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:16:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:16:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:16:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 21:16:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:16:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:16:02 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Dec 2025 21:16:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:16:02 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 21:16:02 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 21:16:02 GMT
CMD ["apache2-foreground"]
# Thu, 18 Dec 2025 22:11:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 18 Dec 2025 22:11:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Dec 2025 22:11:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:14:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 22:14:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Dec 2025 22:14:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Dec 2025 22:14:23 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 18 Dec 2025 22:14:23 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 18 Dec 2025 22:14:24 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 18 Dec 2025 22:14:24 GMT
VOLUME [/var/www/html]
# Thu, 18 Dec 2025 22:14:24 GMT
VOLUME [/var/www/data]
# Thu, 18 Dec 2025 22:14:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 18 Dec 2025 22:14:24 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 18 Dec 2025 22:14:24 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 18 Dec 2025 22:14:28 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 18 Dec 2025 22:14:28 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 18 Dec 2025 22:14:28 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 18 Dec 2025 22:14:28 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 18 Dec 2025 22:14:28 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47998c11af45f43eb6b8cb899fa25be11b5ebf9d635def9471b117c6a92aae3c`  
		Last Modified: Thu, 18 Dec 2025 21:16:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bbe9a107057fe42ba932b9c218f9657f3687f98ad67535889417fff6f22b25`  
		Last Modified: Thu, 18 Dec 2025 21:16:44 GMT  
		Size: 98.2 MB (98165937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae15ad323afcb1d435e806638d780f8dd6f377268bb44e277e08f90d12138b7`  
		Last Modified: Thu, 18 Dec 2025 21:16:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3cf6418c5513a51a2077bd4d17be705817f27eaa13f688bcc059ea9b525f0c`  
		Last Modified: Thu, 18 Dec 2025 21:16:32 GMT  
		Size: 20.2 MB (20159057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075b13550ee7ed125347df0b60e91f7ed561e133842a1be11b8cbc30f14b2f3`  
		Last Modified: Thu, 18 Dec 2025 21:16:29 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41226107032e256bcd3f619773d924b60e486e8f1b523d068feae43cbcc6a71`  
		Last Modified: Thu, 18 Dec 2025 21:16:29 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b44c16f9a1c2c92a47b8e595bc954c0cf103ac3afd96eebcfd32776ad6acaa`  
		Last Modified: Thu, 18 Dec 2025 21:16:31 GMT  
		Size: 12.7 MB (12730702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e70a20e8b13e3a865c94732160cf3d81a94d7431561369be9c2c585768a03a`  
		Last Modified: Thu, 18 Dec 2025 21:16:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373644a0e162ae51546ad78b0b6b4d0763baf298b9d26bfdb91e4809d0009b0d`  
		Last Modified: Thu, 18 Dec 2025 21:16:31 GMT  
		Size: 11.7 MB (11689338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a26a873f135b31ae2cf80ee3654679e10dc105be1349b5213a2051f42cfb58b`  
		Last Modified: Thu, 18 Dec 2025 21:16:30 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be95f3af5a4f3859237aa4f148ae47ad3c8c2ddf6ae6b432956969e507eb13d5`  
		Last Modified: Thu, 18 Dec 2025 21:16:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82930184443a746b8e792d1b30daca2746be35938d135737a449ac3716cd5c0`  
		Last Modified: Thu, 18 Dec 2025 21:16:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa161be9b44e5defec1e29e4d1d6a1094e6387e2a5450e35a3ad20cbeb9971`  
		Last Modified: Thu, 18 Dec 2025 21:16:29 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658366397bc4ba71f4548c4a4c14c9d5a928ed60a39f59a706e8b15f7beaa525`  
		Last Modified: Thu, 18 Dec 2025 22:14:50 GMT  
		Size: 18.3 MB (18251478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa14ac67e267063238f04a770b532e2b71abc355bb9b0309b8ab89d2e5053db`  
		Last Modified: Thu, 18 Dec 2025 22:14:46 GMT  
		Size: 1.1 MB (1059309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4190914e15f6c153b05a62da40096a31dc8ffc6b19eb6d184aa18de0bf2424`  
		Last Modified: Thu, 18 Dec 2025 22:14:53 GMT  
		Size: 33.4 MB (33369027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8663557b9f6516824272907287406ad66ca26999d899758d4912cc028c9e8e09`  
		Last Modified: Thu, 18 Dec 2025 22:14:46 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53016c248386d0d43e0bb2e8a8d3c27ff93b86c66bf4a99e252dd2059a488a5`  
		Last Modified: Thu, 18 Dec 2025 22:14:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60940b087b195d8366c3335fd171204c96ce7534e5fae758e44e9a12b7ef208`  
		Last Modified: Thu, 18 Dec 2025 22:14:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a9e185e9d827fbbe7db852e164ad8a8d8a427b8f64a748c990f8eda018603a`  
		Last Modified: Thu, 18 Dec 2025 22:14:47 GMT  
		Size: 18.2 MB (18203696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c96f5dde65b25fa529f2e2352f4801239f0ac4f709bf6b5c0d0edfa0375a14`  
		Last Modified: Thu, 18 Dec 2025 22:14:46 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e975edb6ef1c37fff0e07d52a25d5c86fc70fd2a1f43cc807bddfef10a666400`  
		Last Modified: Thu, 18 Dec 2025 22:14:46 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:ede2dad9c3d3a010929b24dd2cf4b006653d369e65c556c1f680efb07311cbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (66008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710e142993f767549c368729c024d7a8c737a2a6518b953827027dff63f6b79c`

```dockerfile
```

-	Layers:
	-	`sha256:f54dac589cb636a88e0e84d056537d9b57e41bf0e71bbc2c120cf657bbad4623`  
		Last Modified: Fri, 19 Dec 2025 00:28:20 GMT  
		Size: 66.0 KB (66008 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; 386

```console
$ docker pull friendica@sha256:2d49db92a32318893aacfaba7b47deb97205180bc60eb6ecf9a4e97b21da18fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249981324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f1e674125cebfee391ea8a9de2b0747fece84d26b5246a292f67da14d62003`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:18:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:18:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:18:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:18:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:18:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:18:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:22:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:22:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:22:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:22:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:22:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:22:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:22:01 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:22:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:22:01 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:25:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:25:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:27:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:27:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:27:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:27:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:27:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:27:58 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:27:59 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:27:59 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:27:59 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:27:59 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 00:50:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 00:50:41 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 00:50:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 00:53:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 00:53:29 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 00:53:29 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 00:53:29 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 00:53:29 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 00:53:29 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 00:53:34 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 00:53:34 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 00:53:34 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 00:53:34 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 00:53:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c715900a5d017f41f71c0c6e219ce29d2f5e1a21dbf382d916de0d125aef6d5c`  
		Last Modified: Mon, 29 Dec 2025 23:21:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f8f6118f615575ac56dc47a08286989f4706e9cb6d7dda7f49db2212b67baa`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 101.5 MB (101518864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfc9f4eab72249ce1f07c4452e8453a84e61d792a08c8cdf6e5d856a5ba2c19`  
		Last Modified: Mon, 29 Dec 2025 23:21:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b236748cc51f0e359546b88be1cc30b44d78d2d7cb8f96565bbc82e7e22ed58`  
		Last Modified: Mon, 29 Dec 2025 23:25:04 GMT  
		Size: 20.7 MB (20658447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfad74fcbfd6ec99cf04640ffab9f0389b49d884338cf380f63af2fc42c28a1`  
		Last Modified: Mon, 29 Dec 2025 23:25:02 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414dd7c34cfcd0b3d6cc354730c57253b9667fbd5e40ae7effd913e0a9588a`  
		Last Modified: Mon, 29 Dec 2025 23:25:01 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c155bbf1f52408d3af9aae57152135e250c1e8442b09ec308ef66caabdae3`  
		Last Modified: Mon, 29 Dec 2025 23:28:17 GMT  
		Size: 12.7 MB (12730150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dcbf11e27df3e6729d3ee86f4a5c8c8eedf5c9d1a2675e3c38b7a07253f93f`  
		Last Modified: Mon, 29 Dec 2025 23:28:16 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b816bb1302da21ef364b1fb5b7fe4e4ab564d381d36fadda896dc62ad796c`  
		Last Modified: Mon, 29 Dec 2025 23:28:18 GMT  
		Size: 11.9 MB (11885117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dbcf038852ab5b3d13438c83b6ec8347e2cceec7494feb5bd8dd9cc443dc1e`  
		Last Modified: Mon, 29 Dec 2025 23:28:16 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618bfd47d2d77383c68b33d9ee2b8cf23389c6cd57b7a4ab51ebe77667adede9`  
		Last Modified: Mon, 29 Dec 2025 23:28:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146b2ccdf6e746042213aca8d3dd5fa504b87d6f2d98ed53bff97445398c3168`  
		Last Modified: Mon, 29 Dec 2025 23:28:17 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e112ed12c6522a7c10c3538f023a6dce1a9f8233be42b65867331815146fb8`  
		Last Modified: Mon, 29 Dec 2025 23:28:16 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f062fcc0b9affe90aa8773ebd4a5079b2c61f48ffc552ff098f87c63236a19`  
		Last Modified: Tue, 30 Dec 2025 00:53:52 GMT  
		Size: 19.0 MB (18982781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c230f518728aedec25d1ce5914b398beb240524e88c2be6cf7aa93e60236e0`  
		Last Modified: Tue, 30 Dec 2025 00:53:49 GMT  
		Size: 1.1 MB (1102048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a76312f158f407342230a4f4730a86fd46a7404b5d665f18febf384e2135d86`  
		Last Modified: Tue, 30 Dec 2025 00:53:53 GMT  
		Size: 34.8 MB (34822085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21ac584ec1d59c1d0c0840ed7a3103f7375d3aecbd65923276effcf0bd2940`  
		Last Modified: Tue, 30 Dec 2025 00:53:49 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4200128ff4acb02e5c9a4981fc35e2f750232c9506eabec57dbc194feeed20e2`  
		Last Modified: Tue, 30 Dec 2025 00:53:49 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99609fb334ab28cf1baaf9911c536f11a83caee88deed2073048529cd651b593`  
		Last Modified: Tue, 30 Dec 2025 00:53:49 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15859f87ff579aa2528508ffff78bfe6e92d055b90029db903eb43148f23a1f`  
		Last Modified: Tue, 30 Dec 2025 00:53:51 GMT  
		Size: 19.1 MB (19060253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52587ddfdd1aae5620c6aaf3a293420eacf9e6d99e0f3deb22744a6c5814b19a`  
		Last Modified: Tue, 30 Dec 2025 00:53:49 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c46bc3c449f1a9ef9ce466201f93c6fd8badaf8b2eaed05178a10ff20e4bcc`  
		Last Modified: Tue, 30 Dec 2025 00:53:49 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:7eb72584800a7541955aa8a965e96e82253de6ee695351a6aebd32d2f82b5dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5502eb7312e8d0b435295f21d5aac365546be6bff55b2a288c9a1debfd9704ab`

```dockerfile
```

-	Layers:
	-	`sha256:fe81b02dcc92cac0c4b9283c9b8f400b440e8071468714bea6a8f355a67aa449`  
		Last Modified: Tue, 30 Dec 2025 03:29:53 GMT  
		Size: 65.8 KB (65780 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; mips64le

```console
$ docker pull friendica@sha256:4dbd5cc6be0064603109921de68474f89bd07c4c9d0a17e89b7e96d099cd0976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221986397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0f88610abcd0b0d2145a10cdbe5f9e76cf3a629b4ae9a52f84b149c07b6ed4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:58:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 23:20:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 23:20:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 23:20:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 23:20:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:20:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:20:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 23:20:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 23:20:14 GMT
ENV PHP_VERSION=8.3.29
# Mon, 08 Dec 2025 23:20:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 08 Dec 2025 23:20:14 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 22:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Dec 2025 22:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:00:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 23:00:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:00:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 23:00:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 23:00:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 23:00:47 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Dec 2025 23:00:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:00:49 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 23:00:49 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 23:00:49 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 00:42:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 19 Dec 2025 00:43:18 GMT
ENV GOSU_VERSION=1.17
# Fri, 19 Dec 2025 00:43:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 00:55:26 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 00:55:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 19 Dec 2025 00:55:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 19 Dec 2025 00:55:28 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 19 Dec 2025 00:55:30 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Fri, 19 Dec 2025 00:55:32 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 19 Dec 2025 00:55:32 GMT
VOLUME [/var/www/html]
# Fri, 19 Dec 2025 00:55:32 GMT
VOLUME [/var/www/data]
# Fri, 19 Dec 2025 00:55:32 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 19 Dec 2025 00:55:32 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 19 Dec 2025 00:55:32 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 19 Dec 2025 00:56:49 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 19 Dec 2025 00:56:51 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 19 Dec 2025 00:56:52 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 19 Dec 2025 00:56:52 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 19 Dec 2025 00:56:52 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:61bd5d75181e25f5f5e3531619059f6e37f78adcbb00ca9d39313b7ba4b3c2e1`  
		Last Modified: Mon, 08 Dec 2025 23:40:06 GMT  
		Size: 20.1 MB (20077351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acad867ef5880c8aa4e1725835cf466a40113f3ec2b863a0cae3dfbe79a0f10b`  
		Last Modified: Mon, 08 Dec 2025 23:40:04 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d934d8cd17a29ec9009d709e1832f30cce38e0acccdd7574ba199b5a2b38c2`  
		Last Modified: Mon, 08 Dec 2025 23:40:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d070e871e483619a48ade6d3d570fff342b787e6c6063dae19f4f5fb880a9`  
		Last Modified: Thu, 18 Dec 2025 23:01:42 GMT  
		Size: 12.7 MB (12729163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65d0016537035b5dd4399bea71e7964c1b24a007b6adf3096ac424df9d4e3cf`  
		Last Modified: Thu, 18 Dec 2025 23:01:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3207909fed146aca724ced2b6319ec8ce35c9c8f0bc9ee4a63c13a60cfaf33f3`  
		Last Modified: Thu, 18 Dec 2025 23:01:40 GMT  
		Size: 10.7 MB (10747194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de78fb5d5f8882b3f451be5ac37bae98b6e8b2702422eba32547a98c6f294c`  
		Last Modified: Thu, 18 Dec 2025 23:01:39 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dabc57e8986265d06686ec60161d9f0abcdc52ca22067d8ff9730c30aae297`  
		Last Modified: Thu, 18 Dec 2025 23:01:39 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75972474dd59cfc4b176139983ce81338d2016d79293940e1bc48712c60442f6`  
		Last Modified: Thu, 18 Dec 2025 23:01:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a064b467b290d9b7c08ea91db67ceb8ce9546c95757f70a2e7695320b479436`  
		Last Modified: Thu, 18 Dec 2025 23:01:39 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300da4b0d5eaa61cc12f50ebadd7127c86d0a2c855a7cdf87ea5ddded479d804`  
		Last Modified: Fri, 19 Dec 2025 00:58:08 GMT  
		Size: 17.7 MB (17738472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721f4f7a9a92446f282ab80675b627c4064bdd1db796b09867c1213e9e32ce9b`  
		Last Modified: Fri, 19 Dec 2025 00:58:06 GMT  
		Size: 1.0 MB (1012594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b796fdbd64bf5048053af566dd64d1a06bfca3e9ef4f85f878c1608ae0c7e5ee`  
		Last Modified: Fri, 19 Dec 2025 00:58:10 GMT  
		Size: 32.6 MB (32587382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef7472ff5abad0262746b0e1230d7a8533cbcd2bd9b366b3839b50f40c548a`  
		Last Modified: Fri, 19 Dec 2025 00:58:06 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07d174c7a34091eeaf5602f5e37cdb5b4f13de1e40a9c2a02b61e857dc9fa6e`  
		Last Modified: Fri, 19 Dec 2025 00:58:06 GMT  
		Size: 603.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febcec8d05dfc51713d3afcda1d2ee6d04ed0d159c41cf3b37d3840ed0f2d7a0`  
		Last Modified: Fri, 19 Dec 2025 00:58:06 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d13ab38baf3df4508bc36c2516c9e0d1a24a2785e4395dd41f8fa21e6bad79`  
		Last Modified: Fri, 19 Dec 2025 00:58:08 GMT  
		Size: 17.9 MB (17898223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4a076e86f7246a074f4f06d0f70863bfdabc5db8a72c29d869fac25f8bedd1`  
		Last Modified: Fri, 19 Dec 2025 00:58:06 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6e6e1ae8cecc742288b01b5d07fb80c205d43a8acbd91686430d62c061d7`  
		Last Modified: Fri, 19 Dec 2025 00:58:06 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:14098fd447e914da21f0df7d31913e8bd46f402706741d81d8c00e1b1a6f8eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ffe3bd02a471c7d19938940f1ae42817693e65167945cbc990ff372244b98d`

```dockerfile
```

-	Layers:
	-	`sha256:b4904ae77ac59b227fe3b8a57b9a3f9e5d354c228ca3e536c2eaa735939b1d23`  
		Last Modified: Fri, 19 Dec 2025 03:27:37 GMT  
		Size: 65.9 KB (65898 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; ppc64le

```console
$ docker pull friendica@sha256:c2eed8621a8d75531111ca23f25c3f32f3284354b5de309b1d9608aad091c38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255292253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbf58fb24c3920b9bc407b298b3af9aa8b97490d0342075800c7cebc5d03864`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 12:45:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 12:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 12:51:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 12:51:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 12:51:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_VERSION=8.3.29
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Thu, 18 Dec 2025 21:55:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Dec 2025 21:55:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:59:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:59:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:59:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Dec 2025 21:59:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:59:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:59:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Dec 2025 21:59:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:59:44 GMT
WORKDIR /var/www/html
# Thu, 18 Dec 2025 21:59:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 21:59:44 GMT
CMD ["apache2-foreground"]
# Thu, 18 Dec 2025 22:45:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 18 Dec 2025 22:45:45 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Dec 2025 22:45:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:51:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 22:51:32 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 18 Dec 2025 22:51:32 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 18 Dec 2025 22:51:33 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 18 Dec 2025 22:51:34 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 18 Dec 2025 22:51:34 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 18 Dec 2025 22:51:34 GMT
VOLUME [/var/www/html]
# Thu, 18 Dec 2025 22:51:34 GMT
VOLUME [/var/www/data]
# Thu, 18 Dec 2025 22:51:34 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 18 Dec 2025 22:51:34 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Thu, 18 Dec 2025 22:51:34 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Thu, 18 Dec 2025 22:52:24 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 18 Dec 2025 22:52:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 18 Dec 2025 22:52:28 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 18 Dec 2025 22:52:28 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 18 Dec 2025 22:52:28 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:231e39ac6179aacbf25d364d78fd814c69de366cbb654ba168ce29a3f513972f`  
		Last Modified: Tue, 09 Dec 2025 12:56:55 GMT  
		Size: 21.3 MB (21318007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dee34846779660512ad78cede3a13043397aeb2b2107d9017b6078a6d00b3a`  
		Last Modified: Tue, 09 Dec 2025 12:56:54 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4798c347c2e1d6893d691bab3a8901ee08329f6292693da798fcac91fb1cd45e`  
		Last Modified: Tue, 09 Dec 2025 12:56:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5c8e8b1d8bfb353ba8d94e462fa1f40bd42ef8a836296c7a64fb2e328fc26`  
		Last Modified: Thu, 18 Dec 2025 22:00:25 GMT  
		Size: 12.7 MB (12730550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441446a99ef4c6760c324f82e44d02b50cf9554a051fa0058463b5f4c42a9fb8`  
		Last Modified: Thu, 18 Dec 2025 22:00:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f12d37e543bc892d438e2dec25918525a1f461933b075cb024e734ab6966051`  
		Last Modified: Thu, 18 Dec 2025 22:00:26 GMT  
		Size: 12.1 MB (12086601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cbc4329e8e9616fb00200163cf38d6f7cce0ed40895e0c5a135ec3ca053b14`  
		Last Modified: Thu, 18 Dec 2025 22:00:24 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c539edcc190ec59705b7f6229c3c73b6a58180b1dfb0e4568322a8d14f16ca`  
		Last Modified: Thu, 18 Dec 2025 22:00:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d090e5fcf9910964459a1b6635981c4f4167cb655107f19c8a00a8d05a9e8`  
		Last Modified: Thu, 18 Dec 2025 22:00:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45bbdaaa6761fe885dd0367ae378f4eed27762366749b34c85af8eeacac10a7`  
		Last Modified: Thu, 18 Dec 2025 22:00:24 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301d63b1a3cdacce8e886bf987dd475002c5b0072f71a9640c5bbf6795c3eea`  
		Last Modified: Thu, 18 Dec 2025 22:53:03 GMT  
		Size: 18.6 MB (18578932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afb112df43eab4cadf85e38ca632a6e7fe38fa70be67179c1dd9eda6bc01868`  
		Last Modified: Thu, 18 Dec 2025 22:53:01 GMT  
		Size: 1.1 MB (1050327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdbf75dda7451ca1041221492eff241c4780105df7450801737aab79c8efcf7`  
		Last Modified: Thu, 18 Dec 2025 22:53:04 GMT  
		Size: 35.4 MB (35447651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9318339d1ecd5b020c2ae6c08fcb56d15c15b8a3b6df44686d9459c0fad2a4`  
		Last Modified: Thu, 18 Dec 2025 22:53:00 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d942781a87325c644a6af09597d6ec197bbbc1710cc8e2e5933a90fced762327`  
		Last Modified: Thu, 18 Dec 2025 22:53:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89e68b8e1b4b4239f06a6187017a25df5d619293cbf560a680ebea561672a61`  
		Last Modified: Thu, 18 Dec 2025 22:53:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567802bcc868b75a626f30643052f041de66f2256790a49d67760e6b7553c94`  
		Last Modified: Thu, 18 Dec 2025 22:53:02 GMT  
		Size: 18.7 MB (18670457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385d28cc7189f93d9ddfff4b7272d4aa55340a6864e967ec7f82b26e31c0d19`  
		Last Modified: Thu, 18 Dec 2025 22:53:00 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353c39381000cadcea4f897b40ae15791a1c72eda732d9c86b672dbf95ecded`  
		Last Modified: Thu, 18 Dec 2025 22:53:00 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:c7eef0108267d135afaeaa233cb053280498adf4d2df10e5e9f7b449b8dc638d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f2e8c71c7b28d0834ca9e0556bd694b60309d4122268dbf5f8f98221491dfc`

```dockerfile
```

-	Layers:
	-	`sha256:dcc3f3a047a2232a6f292d99dd5e41e44fec0f394a8e5c3833551aa430ff342b`  
		Last Modified: Fri, 19 Dec 2025 00:31:55 GMT  
		Size: 65.9 KB (65880 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev` - linux; s390x

```console
$ docker pull friendica@sha256:98d2c63f4a8fc1ac32984170879068287642ed502630fddf5e07e8e813a81f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219315639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907d9e0a9038e0bd84bd7c50f5c138e09f0e18c52fda08ec26106e7b5e1e5618`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

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
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:24:36 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:36:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:45:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:45:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:47:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:47:36 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:47:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:47:37 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:47:37 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:47:37 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 02:31:40 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 30 Dec 2025 02:31:48 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Dec 2025 02:31:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 02:33:54 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:33:54 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 30 Dec 2025 02:33:54 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 30 Dec 2025 02:33:54 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 30 Dec 2025 02:33:55 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 30 Dec 2025 02:33:55 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 30 Dec 2025 02:33:55 GMT
VOLUME [/var/www/html]
# Tue, 30 Dec 2025 02:33:55 GMT
VOLUME [/var/www/data]
# Tue, 30 Dec 2025 02:33:55 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 30 Dec 2025 02:33:55 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 30 Dec 2025 02:33:55 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 30 Dec 2025 02:33:59 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 30 Dec 2025 02:33:59 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 30 Dec 2025 02:33:59 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 30 Dec 2025 02:33:59 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 30 Dec 2025 02:33:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:222bc849e1b19371c05dc68d739ed0f184d73bbb8532c19f810ba988bef7b2ab`  
		Last Modified: Mon, 29 Dec 2025 23:40:12 GMT  
		Size: 19.9 MB (19909960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89757ebcdcc864a57a0e2a372eb3540fbd9b10f5a4de7457f350eaeae6a38b35`  
		Last Modified: Mon, 29 Dec 2025 23:40:10 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd1a00aff1b003f8f4201db4bbce376688e04da2e77809b06123ea3d73eaf17`  
		Last Modified: Mon, 29 Dec 2025 23:40:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd44b0edc854d4c70a677e49226387ab8ab9acbded814f93b65cfa17e7e4afb`  
		Last Modified: Mon, 29 Dec 2025 23:48:00 GMT  
		Size: 12.7 MB (12729674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bd2fb9f05a92d50a1166ca11246d04f8b63c3a052843ed21a62f5a938e3e7`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92837e7b7816d6304f61d0dc50ec6758b8e9974983f882ec5e232642d63cf9f`  
		Last Modified: Mon, 29 Dec 2025 23:48:00 GMT  
		Size: 10.9 MB (10884488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a28d6cfdc56a2859bb5d55bcd8c8b27b6b699034b63d35ea1bbbe9f2db8d9c7`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451c705d0e164c6bb4a92fb7bdf949720e11306521f77cb911511d87b637b541`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f0b8efb52202ff4cfd94ee9e69f33d30ee5167f891269bc14848f2666cd89e`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab760fdd040ff526035c85b08facf962133fc67504ccc5ca8f5206505605f72`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c353b36f3278ea973ef33945b5f137eacbb832a1bc97e232adaa690d3e9d06`  
		Last Modified: Tue, 30 Dec 2025 02:34:19 GMT  
		Size: 17.7 MB (17736997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f0b42ccee89bfb10718934fe2ea43e10d61ee14583cdc3e0d51e936f4bc015`  
		Last Modified: Tue, 30 Dec 2025 02:34:18 GMT  
		Size: 1.1 MB (1091896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c698ef68b87e50d6870bd50dc3782f9223177035ea19e6b92204c879505ff`  
		Last Modified: Tue, 30 Dec 2025 02:34:21 GMT  
		Size: 31.6 MB (31576000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6ed69867f921b3dae84a9efc71937872cae07b2aa3de1d213d13e83e5c3033`  
		Last Modified: Tue, 30 Dec 2025 02:34:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53063fe31e0398e45a620251c90f913e46c5370001a734310c950a66160062e`  
		Last Modified: Tue, 30 Dec 2025 02:34:18 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d0334d902e6bdc7f19c5fd3246bcee5ccbfe08a9fba92ae38f27959ea8c868`  
		Last Modified: Tue, 30 Dec 2025 02:34:18 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685ede5934c56c8cdeea190b6a7634135d22af65ee3a94ff394c65a7dffcbd84`  
		Last Modified: Tue, 30 Dec 2025 02:34:20 GMT  
		Size: 17.7 MB (17663987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8c93cddf0a690e30e4f15983532b4ec2ae852e1ca69337609c2ba42495cf97`  
		Last Modified: Tue, 30 Dec 2025 02:34:18 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866d9033fa92d5455ceab571617b139a90b7a14de7aa57834d21d3d07015c2b8`  
		Last Modified: Tue, 30 Dec 2025 02:34:19 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev` - unknown; unknown

```console
$ docker pull friendica@sha256:f05d9a5a67818c18eaf45d5c10bdd4023aa182c429e4eb4b0df466a917bf5866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca7f3f92544dfb34587b3f00a200ee93c10f1e12bcd8380ed39150d03f2cf72`

```dockerfile
```

-	Layers:
	-	`sha256:0d683ccec981dfe9b8384b97ce3f7fed5e4f8d7cb130dec16527a09b9608a03f`  
		Last Modified: Tue, 30 Dec 2025 03:30:05 GMT  
		Size: 65.8 KB (65814 bytes)  
		MIME: application/vnd.in-toto+json
