## `friendica:dev-apache`

```console
$ docker pull friendica@sha256:e03bc7c9cdbe60bb9fae9669e54e8eb6431093dd575b3b7aa5a4b7371bbf13c9
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

### `friendica:dev-apache` - linux; amd64

```console
$ docker pull friendica@sha256:674c870924dffa085f5fed941d5f515885fe9cf6253c18e4922acb7ab21c14cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250610595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab555e6dc6c5a8c1ba6e2ec0e8df53a109eea4976a6b71b304da922caf9cf15`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:24:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:25:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:25:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:25:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:25:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:25:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:25:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:38:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:38:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:38:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:55:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:55:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:58:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:58:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:58:04 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:58:04 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jan 2026 23:31:49 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 09 Jan 2026 23:31:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 09 Jan 2026 23:31:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 09 Jan 2026 23:34:15 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 23:34:15 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 09 Jan 2026 23:34:15 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 09 Jan 2026 23:34:15 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 09 Jan 2026 23:34:15 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Fri, 09 Jan 2026 23:34:16 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 09 Jan 2026 23:34:16 GMT
VOLUME [/var/www/html]
# Fri, 09 Jan 2026 23:34:16 GMT
VOLUME [/var/www/data]
# Fri, 09 Jan 2026 23:34:16 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 09 Jan 2026 23:34:16 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 09 Jan 2026 23:34:16 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 09 Jan 2026 23:34:19 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 09 Jan 2026 23:34:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 09 Jan 2026 23:34:19 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 09 Jan 2026 23:34:19 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 09 Jan 2026 23:34:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963630ac40700bca53277eac42f465504ac98f81be14a88a0ecad9835241f32c`  
		Last Modified: Fri, 09 Jan 2026 22:28:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c50afb09b54e62b4d8e5a38037baad6f35c548251cf0d49306da6a94cb3ed`  
		Last Modified: Fri, 09 Jan 2026 22:28:50 GMT  
		Size: 104.3 MB (104330337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b6633b600b23c0808c1efce6e7949d9ebbd0f5b0d2a199b50974357fe82f73`  
		Last Modified: Fri, 09 Jan 2026 22:28:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187d48cd69bd460ad44f92168f8e0f9265bd35f50b20536a343e6e8079470d0`  
		Last Modified: Fri, 09 Jan 2026 22:41:36 GMT  
		Size: 20.1 MB (20131837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5042a6ff2d3d1aada0d0344194e31f0ce0a28ddb2d82e42e75d919d1db363`  
		Last Modified: Fri, 09 Jan 2026 22:41:34 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23c1e5a0c4aa79f7e93c7e42c70ef8e6795a4f55fed039fc1fd37870d510a99`  
		Last Modified: Fri, 09 Jan 2026 22:41:34 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1dcab4d4953c82e3735c5406c78ccd2f218c0a073ac41541200d5d2bc02057`  
		Last Modified: Fri, 09 Jan 2026 22:58:23 GMT  
		Size: 12.7 MB (12731090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458f18d1bb6790948e26c649b639c3d1e6bcee59547d48f4df88dadf2e776ed`  
		Last Modified: Fri, 09 Jan 2026 22:58:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653c840b869b5480526b156be8d39dde37f5eb666c9574d0246a6e6c7893cfcd`  
		Last Modified: Fri, 09 Jan 2026 22:58:24 GMT  
		Size: 11.7 MB (11677853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a39f8bc106fb62c475b084739ca56baa5d9e8c012a753e2e59c5073a7de37`  
		Last Modified: Fri, 09 Jan 2026 22:58:21 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1838d5d0a05c23e9a823d4624b4b8f9bf68594819e3c09178b5c7319a47922e6`  
		Last Modified: Fri, 09 Jan 2026 22:58:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf39573595d85cd25a776d142a44e8b5b7525df070de4a4f9479237478e4d1d`  
		Last Modified: Fri, 09 Jan 2026 22:58:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c58fae825ea6ef592a578b1fa197b6d648b55e0d8afced18d4370bae18b076`  
		Last Modified: Fri, 09 Jan 2026 22:58:22 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da81801b1fbf072f14711d9d2f104d8a6e0b38522c6238b25457e749150f6e80`  
		Last Modified: Fri, 09 Jan 2026 23:34:39 GMT  
		Size: 18.5 MB (18460342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d07f8cadfdaad418ff36593ebf1df16481dcfc4a199424e337488f416d356b4`  
		Last Modified: Fri, 09 Jan 2026 23:34:36 GMT  
		Size: 1.1 MB (1127355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d745fea58018dbf9901c95559fbde82d8ad5e70af18a0cae2054895c533f4513`  
		Last Modified: Fri, 09 Jan 2026 23:34:43 GMT  
		Size: 35.5 MB (35523571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432c137271a4477bed5ecf23d50d7439c0d21f3c46f25bfc0923e0114515188c`  
		Last Modified: Fri, 09 Jan 2026 23:34:38 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854d3ba0f011bcc341c16f0d835431a9d542b6eabb6917f6ff6fe8f9cb7a6273`  
		Last Modified: Fri, 09 Jan 2026 23:34:36 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f09d6f05989213fddaae121d576e124dadfda093da22cd7a0b6ee3a67e500a`  
		Last Modified: Fri, 09 Jan 2026 23:34:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09ec41a625fd0bcd22d7e0224817de0efd82f5940f508768e986cdfa974a737`  
		Last Modified: Fri, 09 Jan 2026 23:34:37 GMT  
		Size: 18.4 MB (18387974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af355596ffa9478ca36705d76f636b6809702f7aa04d9c5c318e22ea5a1f932`  
		Last Modified: Fri, 09 Jan 2026 23:34:36 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac92032bb8430c6d89ded84f9c12e828ecadbacd935b9c34b321a7ae3af2fda`  
		Last Modified: Fri, 09 Jan 2026 23:34:36 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:f6541ee19290e8bf3e418e2a7166685ceeb648874cacf3786b991bbc3247698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4fa44a22d6eeed6f4bbb1971f30aee795634f347c3a73a3559fc0fcee39a91`

```dockerfile
```

-	Layers:
	-	`sha256:e913bec704512206a889015ed404ebecb9961629faba59c1cb2ed0621a849164`  
		Last Modified: Sat, 10 Jan 2026 00:30:03 GMT  
		Size: 65.8 KB (65823 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:e7a119252dd28229e2d5070bad6e4a949277c5605b83cbe132400bde43f1639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219698945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c265246ee0e41a5a826e4bf47c2f219c55a7116860857b9d5dd9f83d64f46`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:47:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:47:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:47:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:47:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:47:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:47:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 23:03:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 23:03:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 23:03:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 23:03:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 23:13:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 23:13:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:16:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:16:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:16:11 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:16:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:16:11 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:16:11 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:24:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:24:15 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:24:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:27:07 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:27:07 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:27:07 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:27:07 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:27:07 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:27:07 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:27:07 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:27:07 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:27:07 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:27:07 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sat, 10 Jan 2026 00:27:07 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sat, 10 Jan 2026 00:27:14 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 10 Jan 2026 00:27:14 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:27:14 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:27:14 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 10 Jan 2026 00:27:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26aa0b573f142f9b0f172c963bb3cbd2fc47e006c7aba719760051d7862300c8`  
		Last Modified: Fri, 09 Jan 2026 22:50:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd55753e09c84743b992e07648ef45d19d821ef2443eb62a1518579258d07461`  
		Last Modified: Fri, 09 Jan 2026 22:50:54 GMT  
		Size: 82.0 MB (81981482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b2deb0888c40ecce1a2d4f14cfa2b3b9ab027e9be6398bbb78832a1045d88`  
		Last Modified: Fri, 09 Jan 2026 22:50:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5b4e9f8abf6f58978bd390affe54a84725c4c948d49555ef731535c5fab7de`  
		Last Modified: Fri, 09 Jan 2026 23:08:17 GMT  
		Size: 19.4 MB (19422410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbb3831246ac801fd770c30e11dbd431601659326ba42866a7335be05e5be2b`  
		Last Modified: Fri, 09 Jan 2026 23:08:16 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f75ff59eec261bb69f1fcb8c405a51984640ac7f93a33f577816d878d1dc5`  
		Last Modified: Fri, 09 Jan 2026 23:08:16 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8c9aa150e82881d4a1a0fa55a091b0c6349c3578247da0c7f8277fb0e23895`  
		Last Modified: Fri, 09 Jan 2026 23:16:31 GMT  
		Size: 12.7 MB (12729301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80ffca7217a93e370b297e9b8e4547d6bb261b0b46c0721ef5a669a3742dc99`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0521963e3ebb6bc50e77d1168307215fa51dcd65db232e465ce21a6401f40a`  
		Last Modified: Fri, 09 Jan 2026 23:16:30 GMT  
		Size: 10.6 MB (10615630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c750ada00f77073fa28faeb927de92132185959efd681cf0b42cc3699a4e34c`  
		Last Modified: Fri, 09 Jan 2026 23:16:35 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3b1265c16694f6ccee473b28c6ece16a4f2464bbc7f2ca6974ccf4e3b06224`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b091b576569913305d71f05cf0bcca3476388dddfb028a265a41a019949e596e`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf54b90af778ec2d6492b02c8de85774d19c6109e22e51778db5863d9e28628`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a176555dd5a208aa6b9d6c656f6cff23c1385ed6d6c6e40c0fd8df208fa7cd`  
		Last Modified: Sat, 10 Jan 2026 00:27:32 GMT  
		Size: 18.2 MB (18196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54113f5feac898eb0274db8bef2f1da7967c66adda9be50e343cfc0ffa596860`  
		Last Modified: Sat, 10 Jan 2026 00:27:31 GMT  
		Size: 1.1 MB (1102743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f601802e4d4b5803362cde1328f30298e0714046812785a1eba95f66f39a042`  
		Last Modified: Sat, 10 Jan 2026 00:27:33 GMT  
		Size: 31.8 MB (31768948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fb991ff97dfbec09407f3db24ec8aca8e98b87185c6a76c24a55146ede7036`  
		Last Modified: Sat, 10 Jan 2026 00:27:30 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc9e64aea7bab910d7c3ffff8f0dae1c2a05781454eebe2c3b095a860f7561`  
		Last Modified: Sat, 10 Jan 2026 00:27:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdfbe64030d9e1ab7853e4ea52e735ca32207e4ba846c09e9d37e6fd72b01e`  
		Last Modified: Sat, 10 Jan 2026 00:27:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8a89c685e4675d305d15ebeb6666ba77354d5be2949bd709a7f0742a4086ef`  
		Last Modified: Sat, 10 Jan 2026 00:27:31 GMT  
		Size: 18.1 MB (18112606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132febac209693d1fda61fb706fc9a2f0e9725142c20bffc25785c55353041f9`  
		Last Modified: Sat, 10 Jan 2026 00:27:30 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b509e5ae6d36074f41eff45500215643c8628a8026bba09cc99a18a0230aac09`  
		Last Modified: Sat, 10 Jan 2026 00:27:30 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:7ed265c047fc54549bd31ba8af677a94354581235aa05ebcbf41156cab889532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442c203953db3e455b72cf8dbffd2390bdfb5feb9c60d6edd914e9dc926a141`

```dockerfile
```

-	Layers:
	-	`sha256:a6609e8ffdd59201ba31f15a4f767c50654f010e03ed2b30762bf6bd8916f55f`  
		Last Modified: Sat, 10 Jan 2026 03:28:37 GMT  
		Size: 66.0 KB (65971 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:cc67edfadac8fff2b74eee2496d0c1ea087946bee9e8fb590ef86603529dc200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208927500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4516ec1fc002723549a20478504f56d0939d93a33692a157f193d34bc9ccc4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:44:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:44:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:44:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:44:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:44:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:44:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 23:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 23:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:37:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:37:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:37:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:37:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:37:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:37:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:37:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:37:13 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:37:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:37:13 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:46:37 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:46:46 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:46:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:49:25 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:49:25 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:49:25 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:49:26 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:49:26 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:49:26 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:49:26 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:49:26 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:49:26 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:49:26 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sat, 10 Jan 2026 00:49:26 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sat, 10 Jan 2026 00:49:31 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 10 Jan 2026 00:49:31 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:49:31 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:49:31 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 10 Jan 2026 00:49:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb090f1d21d6c9cf3d4937306130af775c6b8f77b7015bbc3aeec7831e00cd`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6bcf417f4c97734fc37095a7f4c9b4cfa7d5b09bfe0c3da212d45e63079a7b`  
		Last Modified: Fri, 09 Jan 2026 22:47:58 GMT  
		Size: 76.1 MB (76148731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b714c6e3ee2e505ebbf8085d3c232291b10a74563d8e2886cc4677b5c8b7fe`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba97861883a05a5fe227b13559b8b9477552ccbce71a196429fdd7ba71d8c4bf`  
		Last Modified: Fri, 09 Jan 2026 22:47:53 GMT  
		Size: 18.9 MB (18860044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f877b2e5c7edf9f5fd98f943e52013a9ee513903917ac0e6697d9b819d07350`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cb1bd16c15ea76aea5f1cd5ec4c5f28d6739045d25f1fdb092673752891b9`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc8bbd8b22b2399367d574ae631ed3a6e044da705a84027e865f4b7ffee65da`  
		Last Modified: Fri, 09 Jan 2026 23:37:32 GMT  
		Size: 12.7 MB (12729266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa399bff53edbd66d0678ec48b2d99436e567f84059e4b96c88dd59b5fda5`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c3d8fdbcc4335f3898391a47378469d4e93d61f7303565425f5fa69091c822`  
		Last Modified: Fri, 09 Jan 2026 23:37:31 GMT  
		Size: 10.0 MB (10049759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577b47bc7ef386d5004a4df01a841f82fe6dcc2ca8d2412725d02b75203cd7b4`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be21a00827f7ca0124aeebbd2d30c8d3aa9aaea16cd45000ef758ae5e6e1622`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c20abdd97be432f13737033bbaa7badd860a10e81f73a74b45cc4c7a071d8`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa01db12881d90b659d89bda994b860374fffdc9488ebe6a51f311a74056b45`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2905d30f1f6b9604af831c1005ba1e49d287cf5aac039d54b4055d0ce25c485`  
		Last Modified: Sat, 10 Jan 2026 00:49:47 GMT  
		Size: 18.1 MB (18097763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b8d797f044c7d11f6da48b0adacce834280155cd45a9f6c46592b80cb1e74a`  
		Last Modified: Sat, 10 Jan 2026 00:49:46 GMT  
		Size: 1.1 MB (1093341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c7c20809a12a62761e7dce59079a1e3d485aa075dfa861a1b08cd2bb3429a`  
		Last Modified: Sat, 10 Jan 2026 00:49:49 GMT  
		Size: 30.1 MB (30055055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a75fe4f89f57c24676ec28e2e79d3fc51e91f11d511a82c3a9b71af90d9d7f`  
		Last Modified: Sat, 10 Jan 2026 00:49:46 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7750bfa2ea589ef548b13cb9413f80a4193dbb4de221cd70fb7fe4250e8c3135`  
		Last Modified: Sat, 10 Jan 2026 00:49:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c0f4d497375a9bf7200f021a41ed56eebda6e00be04b02edc48d2f9c83ecb3`  
		Last Modified: Sat, 10 Jan 2026 00:49:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d3ac12b2522324a1bb90caaa8acaafa6a59413d0b4633594601d72d3ff11d3`  
		Last Modified: Sat, 10 Jan 2026 00:49:49 GMT  
		Size: 17.9 MB (17947651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20899987317c9f0fe58d2415209f7a0f38e1e39bfe0bf9e8b4ecd2a8e157da80`  
		Last Modified: Sat, 10 Jan 2026 00:49:47 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03739d1c8b4c744714f1e7a8389a15fe339193b660d961d5f853cd42d2cb8407`  
		Last Modified: Sat, 10 Jan 2026 00:49:46 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:db8b0a1ea6d35ea2503bb0b6cbc89a960cb382feee14353fed5f8d98d6b35405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a880afa31a58642c674dd8ccb1fb520cf9e96722736b6682ec90d36805e39`

```dockerfile
```

-	Layers:
	-	`sha256:176797ea0c9ecf1761b0a118349fe9c1ffef753fd998607ed8e86bb9fd88af74`  
		Last Modified: Sat, 10 Jan 2026 03:28:40 GMT  
		Size: 66.0 KB (65972 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:b16b362277ca4f52a54500af369bba90108a4ba36b2e3db6aaef02df68911488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241744850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aa668642c98178fab38a4b4337292bd66bd68d29dd13e5d639b7b1e449ab10`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:59:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:59:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:59:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:59:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:59:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:59:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:59:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:59:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:59:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:59:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:59:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:59:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:03:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:03:52 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:03:52 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:03:52 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jan 2026 23:35:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 09 Jan 2026 23:35:46 GMT
ENV GOSU_VERSION=1.17
# Fri, 09 Jan 2026 23:35:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 09 Jan 2026 23:39:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 23:39:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 09 Jan 2026 23:39:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 09 Jan 2026 23:39:01 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 09 Jan 2026 23:39:01 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Fri, 09 Jan 2026 23:39:01 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 09 Jan 2026 23:39:01 GMT
VOLUME [/var/www/html]
# Fri, 09 Jan 2026 23:39:01 GMT
VOLUME [/var/www/data]
# Fri, 09 Jan 2026 23:39:01 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 09 Jan 2026 23:39:01 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 09 Jan 2026 23:39:01 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 09 Jan 2026 23:39:05 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 09 Jan 2026 23:39:05 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 09 Jan 2026 23:39:05 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 09 Jan 2026 23:39:05 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 09 Jan 2026 23:39:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450c35b859fdaf015417139d60e46d501038ffc84cc8cfc56dd2d5355c291e7`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5137a3b0176cac5ea342caad3a5fed814bacae3fabb829ace4fff233766508`  
		Last Modified: Fri, 09 Jan 2026 23:04:33 GMT  
		Size: 98.2 MB (98165645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050f54b346ff672578f78bee0b344b2ddd3dd2d8587f73dad29a1d10b3eaa565`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a98881c16a3d3c86e2e550c716fdbbfc9d7f85edbb1bd13d1c2463ce7e47fe`  
		Last Modified: Fri, 09 Jan 2026 23:04:24 GMT  
		Size: 20.2 MB (20159105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4faff44f0315a732368c751c54fb9ece3b2d84d49f1948b8fea6edeb68e71`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6e69cb81880398e08379512ccf7a063f25f76ea74757ade4529ccbc5d213c`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693adf2964126a60ec236e69934b608eb6fd2225204b7df56c27c44f91fc9aa`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 12.7 MB (12730675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41aad276a4320c26af9db8dfeac2bb3f08c947baf9f4e86bccb8fd602bfa9b6`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3af918158cf3fbc2cda0b5b2577db9714e178361af9c7b03acb51165d283466`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 11.7 MB (11691135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadf7ca47ca804b8f79ddcfce6796d0126fb1aa1e8ce3ab061561ae510efc05`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f24cb8f109e2c487763d16c0400296952446291689f7649de663998a92f3294`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7951756ef41df75cb2b46cf57c2538cf7e574060c53561cf399b5e27f8f4e039`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d812e03e543d6608fe721dfbf2ae7d05087978b232bd6957aca0ce66dc999f04`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5286d4ee33aa4f43d336da2561d88fa9bd13e8f2325abcc96cbd2dc836d1b`  
		Last Modified: Fri, 09 Jan 2026 23:39:23 GMT  
		Size: 18.3 MB (18251886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc3c71129a3177d0b1148d7e0f8e172367e6023749349afc8b6d582662bef38`  
		Last Modified: Fri, 09 Jan 2026 23:39:22 GMT  
		Size: 1.1 MB (1059416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5824b8616d612b5f27d39d783f50da19af44b54d1820f1f279eaa8e2982933`  
		Last Modified: Fri, 09 Jan 2026 23:39:25 GMT  
		Size: 33.4 MB (33368994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99dc7c313f7e825c254e8ed66d7c98d671bc0e92cc5f7a9ae67454f21b1690f`  
		Last Modified: Fri, 09 Jan 2026 23:39:21 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db35ee892db2a306d2e4fda759dec0bf55b0ce9ac7a32cd0becf7925e5ad8b51`  
		Last Modified: Fri, 09 Jan 2026 23:39:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6516c8ee5a2810c40055e28f1de142f436e8d17faab463658a4a8b3cfc5fb780`  
		Last Modified: Fri, 09 Jan 2026 23:39:21 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0092d9bc48056bdfa3b49b6faaac0524ae092ad216d0e240ba107a954c3684c2`  
		Last Modified: Fri, 09 Jan 2026 23:39:23 GMT  
		Size: 18.2 MB (18203947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34da560505030f2be894faa7cec8bbf75eac5df6fdaf39519e7f33ebcc911c1a`  
		Last Modified: Fri, 09 Jan 2026 23:39:21 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780e27bde3063d8f019cb3a25089e14844bb10f8f1ce9ea258303675f726f717`  
		Last Modified: Fri, 09 Jan 2026 23:39:21 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:b1a39f795f202b5dcb474c97982336fba98f19e60d83f54f437433c0f36a1494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (66008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78648438ee3767fa3b9950c07102094ba55b785c2041b114e1b18d3d5f2526e1`

```dockerfile
```

-	Layers:
	-	`sha256:bc49a165631bbf4122f470ad4610c057d5afd6fa4328ee862b329f936bb64d8b`  
		Last Modified: Sat, 10 Jan 2026 00:30:11 GMT  
		Size: 66.0 KB (66008 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; 386

```console
$ docker pull friendica@sha256:4c176d6b7981843634b53c4faf58b3ba0bfcd802c42a5dce679447b5617a0e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249981117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7113a1bd397bf1d907862b3be1e0305c6a553911540a43c730f3cb3b697c792e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:29:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:29:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:29:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:29:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:29:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:29:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:29:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:30:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:56:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:59:35 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:59:35 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:59:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:59:35 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:04:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:04:45 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:07:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:07:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:07:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:07:23 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:07:24 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:07:24 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:07:24 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:07:24 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:07:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:07:24 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sat, 10 Jan 2026 00:07:24 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sat, 10 Jan 2026 00:07:28 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 10 Jan 2026 00:07:28 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:07:29 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:07:29 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 10 Jan 2026 00:07:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457d1ccad785195cd8bd82a3434569a2b2e357a1e61f19131ca5652d6ce1ac53`  
		Last Modified: Fri, 09 Jan 2026 22:33:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364dc2436467be37a657a53e4ecffa17670f77073ee1599544d346c68ed4637b`  
		Last Modified: Fri, 09 Jan 2026 22:34:06 GMT  
		Size: 101.5 MB (101518476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e91d2d69f9a2a540f430078be65bc6735b8b4cec70665b84ee7624f3fee76b`  
		Last Modified: Fri, 09 Jan 2026 22:33:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdbe4f2d1a8e1de791bf090afe58aaae18fca4fc5bf2ede2aab1b92053453ec`  
		Last Modified: Fri, 09 Jan 2026 22:34:01 GMT  
		Size: 20.7 MB (20658421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2afbd5f39f8a477d14e01d1cbd145a2ce6f152b25941e7afa835d339487525d`  
		Last Modified: Fri, 09 Jan 2026 22:33:58 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5da1d953a49f3c537d3ad2ffcf63ba53f03caea7ab18eac3348b3760ac7dfbd`  
		Last Modified: Fri, 09 Jan 2026 22:33:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95582bd179bf4d6d9a93de4217e75c295ffbda76e39c03736d42038bde95a8a3`  
		Last Modified: Fri, 09 Jan 2026 22:59:55 GMT  
		Size: 12.7 MB (12730169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b40d3dd2a8a54d18b6eb2d7c702aa87861b10ca2b307509f0cc15aaeaa318a`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995aedc2bbb69bf77467aaaa0346621c1abb1537801ac984f57a32b6797c6ea4`  
		Last Modified: Fri, 09 Jan 2026 22:59:54 GMT  
		Size: 11.9 MB (11884978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded6c2130cabf4d29ca0e90d8573dd5f361b951da4cb960059ceea48810a587`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312200252f68fd97203e4e64c48a3fd2a78c33442213e283e099c59501274f60`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59300bc514fc6ffea72ffa786c8d6f21289144365ea91c411f98e175fe5243b2`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d992366c38238f28845e95d60c74b0d97fe2596c6ad85ff3337515a598bc0a92`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d92cfdf2b1cb9769c1000b31c64132ed6e67f2a4030783f9f30c6bf67c3fd6`  
		Last Modified: Sat, 10 Jan 2026 00:07:45 GMT  
		Size: 19.0 MB (18983061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c55bd92fe2ee4cf043e418f07538c99ce69367990b9fc4dbcd9fadd958e682`  
		Last Modified: Sat, 10 Jan 2026 00:07:43 GMT  
		Size: 1.1 MB (1102114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c7a5a592276d75194689572b395fbb89831ba23c271f8eb6d85dd9acdaaeb`  
		Last Modified: Sat, 10 Jan 2026 00:07:49 GMT  
		Size: 34.8 MB (34822149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9937a0e4780bc511105ded7b576b9a5c63056cf58e8db6263d5f9a0b30800e65`  
		Last Modified: Sat, 10 Jan 2026 00:07:43 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc10ee70b030f10d8ce6a9b7dec02098f3d97f70ba1d1d44ac08e6bb6ec3c0b3`  
		Last Modified: Sat, 10 Jan 2026 00:07:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13b5714ef502e5fde2512a452da206e717f86896d9e1be90e0b73aed6d26d9c`  
		Last Modified: Sat, 10 Jan 2026 00:07:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc7fb0202dd7c61ad4fbf388a743baf734afa3dc70697387685a974a267c5`  
		Last Modified: Sat, 10 Jan 2026 00:07:46 GMT  
		Size: 19.1 MB (19060139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbbf29c749937afa39cb29a010afe659c92f16cb0dc2468029efadd3c07da48`  
		Last Modified: Sat, 10 Jan 2026 00:07:43 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54865e3dd7bdd261c06b9547dbd1b64c48bf60dfcfb0cf84732713ab5c706656`  
		Last Modified: Sat, 10 Jan 2026 00:07:43 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:e910d02e5fe2504e354a3a3aa47c6a867d72a9705b4386bbcc7183d0beed8a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef659616c09c4f80b8fed5b528a8d19ccd82afd908c6c41628ba8489064379f`

```dockerfile
```

-	Layers:
	-	`sha256:a759040da3075f91cfb2781835bcf7e69a2f35748e6b491953fbd222158f0fdb`  
		Last Modified: Sat, 10 Jan 2026 00:30:15 GMT  
		Size: 65.8 KB (65780 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; mips64le

```console
$ docker pull friendica@sha256:5649ceb5e334788e89a4de618261ec9f384b4d13adec61596702f6b145f9d768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221986081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ee72871d776928eff4e0bb5807d29bb07fd411286a8bd0d711c2ecd795f9e5`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:18:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:18:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:18:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:18:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:39:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:39:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:39:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 02:10:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:53:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 04:53:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:53:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 04:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 04:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 04:53:24 GMT
STOPSIGNAL SIGWINCH
# Sat, 10 Jan 2026 04:53:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:53:27 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 04:53:27 GMT
EXPOSE map[80/tcp:{}]
# Sat, 10 Jan 2026 04:53:27 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 06:35:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 06:36:35 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 06:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 06:48:43 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 06:48:43 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 06:48:43 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 06:48:45 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 06:48:46 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 06:48:48 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 06:48:48 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 06:48:48 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sat, 10 Jan 2026 07:08:02 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 10 Jan 2026 07:08:03 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 07:08:05 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 07:08:05 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 10 Jan 2026 07:08:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d9cabd4aab99e194d4a41705774411b061e905a5607b5d68428e6c0fdfc3f`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa90b950d6df8880366223e469aa2861d9bff3782a34bbbbd8c49d4d03a522`  
		Last Modified: Mon, 29 Dec 2025 23:38:16 GMT  
		Size: 80.7 MB (80670513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39959c61c1a601c13b85fe9f2c5c8646ffe26d790e73c6bfb044a1a8b6891d0e`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd3e0ce24ae30c711e9419a264d4d93fce74a5c8942103ed45335be3ce91d5f`  
		Last Modified: Mon, 29 Dec 2025 23:59:39 GMT  
		Size: 20.1 MB (20077244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66299e8474ac8c18bf4447b629ee9d516ca68ec5591d0b782108643a83b38af`  
		Last Modified: Mon, 29 Dec 2025 23:59:37 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252fef5e44ae8f0167582befd01c30b3a3ff36ecb05a852ed19c145bc6d5c389`  
		Last Modified: Mon, 29 Dec 2025 23:59:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2517ba538e65aac91e90741b78ea33277b591c2cf858ceca9083f796a89ce1a`  
		Last Modified: Tue, 30 Dec 2025 02:26:53 GMT  
		Size: 12.7 MB (12729094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8a6ab7831cf57fff1c762f8cae82a8944e319d01d7bd4f9e5200e298f241cd`  
		Last Modified: Tue, 30 Dec 2025 02:26:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f356c557382aec51a68da371ff5cbc3f40bafb97153d29d0ec558a25b6dc30`  
		Last Modified: Sat, 10 Jan 2026 04:54:14 GMT  
		Size: 10.7 MB (10746335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99427c011b9792d01eaecb5fd36a0fb30b485bb02b0287b7f162bc029346d02`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97513cc46e69ba1aac8556be8e556893a0a2c62a71b7db73b366face2e18313`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39330457423a74d9f33660e574a782d05fdbeeea9413aa5fdbc40c2fcb55abfe`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbcf6a4738869ac3ebb85bca1b3c2b41afe41e213e62e2d66f7e92507462a67`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac180bad3076c672da6dc391e6c5c520927a6b2e95ba7c797148e18514a9cc3`  
		Last Modified: Sat, 10 Jan 2026 06:51:24 GMT  
		Size: 17.7 MB (17738946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f223f05cbb9ef4ea15e4ff331aacddec48bb669f00037975647a4e2affbf8`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 1.0 MB (1012565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9528ea40e15d8d35afe62586282038b0c02e9ee1eb18423a53db3ce8f89b8a59`  
		Last Modified: Sat, 10 Jan 2026 06:51:25 GMT  
		Size: 32.6 MB (32587060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8762306849c53c0ce36d156352d1f793497cb3b2094f578734722e98840bf5`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1a6f587b2eb7fd6ab1f5427fa6e01939a012d03e23bccbf9d3818c15b272e`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75516c7b06069dc6e3cf84a510f0d322ed14eb07b05ef3869ef0b55542bf5c7b`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b521253546fd34132447280ad7fa27d056054ffa3be3413b3170adf1c7d2193`  
		Last Modified: Sat, 10 Jan 2026 07:08:59 GMT  
		Size: 17.9 MB (17898649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00aa532f9d0a02a75556ec38654df660a75fbab74fc55c0ebb1522e326a35792`  
		Last Modified: Sat, 10 Jan 2026 07:08:57 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d0cd0938bf2e1efe97ab18d8c10ef9af11e2c92ba837ec3d15b56079e5e754`  
		Last Modified: Sat, 10 Jan 2026 07:08:57 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:3307a5ff34af8761bb5645d78244adeee1397b07f20afb85b2f2d964a3e707fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b77540aa0fdd6731dd115a853ee8e15bc90cc908b697c6f03a654965f53e244`

```dockerfile
```

-	Layers:
	-	`sha256:02efb72c86726a5c0c3eb0548afe2fd508c58efaede7bfcc54f1691981377a1a`  
		Last Modified: Sat, 10 Jan 2026 09:27:54 GMT  
		Size: 65.9 KB (65898 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:d018fef6c4d8eda189cc8c4c3490c50de9910dd113f8075a6cd0a1ce1f4ef3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255295686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f64b0321829043d66fae0c4191389d31a7017285aaf13c577f8e2b3e15b04`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:15:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 30 Dec 2025 02:16:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 30 Dec 2025 02:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 30 Dec 2025 02:38:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 30 Dec 2025 02:38:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 02:38:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_VERSION=8.3.29
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 02:38:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 02:38:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:38:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 01:38:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:38:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 01:38:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 01:38:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 01:38:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 10 Jan 2026 01:38:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:38:44 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:38:44 GMT
EXPOSE map[80/tcp:{}]
# Sat, 10 Jan 2026 01:38:44 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 03:04:51 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 03:05:17 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 03:05:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 03:11:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 03:11:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 03:11:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 03:11:52 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 03:11:53 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 03:11:53 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 03:11:53 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 03:11:53 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sat, 10 Jan 2026 03:13:42 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 10 Jan 2026 03:13:46 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 03:13:48 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 03:13:48 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 10 Jan 2026 03:13:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93a9966845dddb639588fdcde0ed0ecf405e81db5bf3e7b306c9cbebf976cb`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226cbc8a9cbea94e5a9e2e037754124cee088acdf931d11622ed35b2aabbfeb`  
		Last Modified: Tue, 30 Dec 2025 02:21:55 GMT  
		Size: 103.3 MB (103328995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20082871cd07652f43cb1378561dfdd8cfbf23782814ff423bbb205eeab4afae`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb4530d72cd41f205428c35fbed64b09ccf2f3f4fbbaf043562a88e6007268e`  
		Last Modified: Tue, 30 Dec 2025 02:42:48 GMT  
		Size: 21.3 MB (21317921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5b57248912e84cfa43adc472de2f9fc3b5b62aa101d4e8fc58896028d1d26`  
		Last Modified: Tue, 30 Dec 2025 02:42:45 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e387f48c69b88a5fe2813456ea23e7fd37b459cb903368e549b64633df976`  
		Last Modified: Tue, 30 Dec 2025 02:42:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1e80a0bf2e049c7b710907e4fa7f6968bbacfd160cfeae222ce034a496ff26`  
		Last Modified: Tue, 30 Dec 2025 02:42:46 GMT  
		Size: 12.7 MB (12730458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fe507b26bad848467f50075fcd792df27ab6248bcc0ea98acfee5d22e8f27`  
		Last Modified: Tue, 30 Dec 2025 02:42:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4538a08e0234705391bfd4536f2024b4fb20328d5d1515d0301f81a3d58bf4a6`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 12.1 MB (12089620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de96dd923991ddd635c95d691de552987785a7ef4ac75dc92976abbea456d3`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8ad80e117b0884e07cad3cefd604ec298f87f1df0a1b929ea97a3b5af8360f`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226b77cbb106247e184770ec3c644b5f6077c34d3f869dfd109e5db682e254a`  
		Last Modified: Sat, 10 Jan 2026 01:39:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6375ee876d68a7f278b10602fc2f2d53c67faaa05969d12b9716bdb8f25f`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172f526ca4e86534b3297a5eac35be3c066b7fc6a8d4651db6b93c44db6100d`  
		Last Modified: Sat, 10 Jan 2026 03:13:14 GMT  
		Size: 18.6 MB (18578952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd16674efd4f38c34169c6d3314bc38dbb08e5179bb2ec93676bce4569061a8`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 1.1 MB (1050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fcd39f83fa98a7e9f6bb59acab3eab3306f0b52be03b733c532eccd25988a4`  
		Last Modified: Sat, 10 Jan 2026 03:13:17 GMT  
		Size: 35.4 MB (35447767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3cfab89a7322006fd057d1fc49a0d0665bfd9254d826622294d8746c07b11`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b6db5b19509f41c4c5c3096e908353e50ad2059fd602087f9cb3161c49c365`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7babcb84f639b6947d0a04b75d87803203018cd93b06ca07f2558f70ad`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d8884f67aab4ee55f810724e46ee7415c15dae32c74b50a41ee5c454542132`  
		Last Modified: Sat, 10 Jan 2026 03:14:07 GMT  
		Size: 18.7 MB (18670887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ad4c82b6148bae9abd8f0a688e532c1aa2703aac090630034ddae8b760377`  
		Last Modified: Sat, 10 Jan 2026 03:14:05 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5b7eab06632497ff7d8cc564b20d3e80bcd394ea7c0384ed2318018a41cfa`  
		Last Modified: Sat, 10 Jan 2026 03:14:05 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:e8c373d7def6435d999f6f821a516d45f36f67065beac8c834a19b2ec34a39be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e18b9b50556fb9893b990e4bfb390a4478755d8a3931cb5021a9a7c519c0a1f`

```dockerfile
```

-	Layers:
	-	`sha256:763ad42361def6ee147eeedada7f1ed4159f2347cef164250e1d244b605e65ba`  
		Last Modified: Sat, 10 Jan 2026 06:28:06 GMT  
		Size: 65.9 KB (65880 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-apache` - linux; s390x

```console
$ docker pull friendica@sha256:79bffc1d2569cce37c2f46a5560f5e5e96371d80b23c1bb1853844a5e0816ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219327501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee06de56db082deaf0897b96b5e890d8ff465365ff22b7364d1045385fe346`
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
# Fri, 09 Jan 2026 23:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:59:19 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:59:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:59:20 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:59:20 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:59:20 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:39:37 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:39:45 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:39:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:41:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:41:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:41:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:41:59 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:41:59 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:41:59 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:41:59 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:41:59 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:41:59 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:41:59 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Sat, 10 Jan 2026 00:41:59 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Sat, 10 Jan 2026 00:42:04 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 10 Jan 2026 00:42:04 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:42:04 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:42:04 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 10 Jan 2026 00:42:04 GMT
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
	-	`sha256:2ee1e7d723d1529427633d1266f3440b5268bbbee89860b5f860e3618579a754`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 10.9 MB (10895817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fd70d8f604ec41e1920fefae4804ffcd9b7976db49138e1ab133c72af7a26e`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2302490d3ad41ec798c7e9599cd079a85af736b2333b12b27c7569aa3d0b4692`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cad21b4a4cce962d44a7d2f3a9ff183cfcda1e0ab6e18d2c06186934b0f104b`  
		Last Modified: Fri, 09 Jan 2026 23:59:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d209b72318af561448271e5264639c438520ca684e8297cbdc412cf6a92bc0`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96bec61591c1b89fc04aff96f6840c1a8952c498c5398afc185757323aa842c`  
		Last Modified: Sat, 10 Jan 2026 00:42:25 GMT  
		Size: 17.7 MB (17737095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c885a3e4e4dd07b46f0f7d4cfd13ce2cea3008975dfd5578d2673341c99b1`  
		Last Modified: Sat, 10 Jan 2026 00:42:23 GMT  
		Size: 1.1 MB (1091917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32c597bd7d6eaa0060c756d3d562578a75bb44528c67ed9bbcc1f707ad8fa1`  
		Last Modified: Sat, 10 Jan 2026 00:42:26 GMT  
		Size: 31.6 MB (31576118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b790c7072ef218a87380aac1df95a6105b88d91d3c19ecedca0ba770d8efe979`  
		Last Modified: Sat, 10 Jan 2026 00:42:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4af0291a94f8ab674f4b3fbd66690dd7a800772064ab046af7c4fadaf7190b`  
		Last Modified: Sat, 10 Jan 2026 00:42:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89124786dfa438d5f5f05feb25bb87ff190d5cb8587ed18d7c860e0983f6a504`  
		Last Modified: Sat, 10 Jan 2026 00:42:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f205fa47e9899be5e382392143386751529019f462f007c2f9e97bbb30376`  
		Last Modified: Sat, 10 Jan 2026 00:42:25 GMT  
		Size: 17.7 MB (17664273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0990854763c7bc03b8fa6d35939fcea1517a680b92ff4f447ea9c82b5427e`  
		Last Modified: Sat, 10 Jan 2026 00:42:23 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c7df801d03826515f491ac0e3da36467bcfc3e0a81e60617d4dacb77fcd937`  
		Last Modified: Sat, 10 Jan 2026 00:42:23 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:b24be429df31e48d9870893e2bac06b7621a9679e2f37eaaff9a6393cc5f7d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892876ec977fcc001cca90e73cb6ade8c7b631051aec10af6261bb5f3031026a`

```dockerfile
```

-	Layers:
	-	`sha256:477938d34b1d358eb6ecdd40e5db19e62703957816fa2a132f4e520eba99d6a7`  
		Last Modified: Sat, 10 Jan 2026 03:28:50 GMT  
		Size: 65.8 KB (65814 bytes)  
		MIME: application/vnd.in-toto+json
