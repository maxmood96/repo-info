## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:d9ee37ec8b3921763efed509db39391d8f11073653e1809a711597083b43fb10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:918d60da062f1d17872d12680a7561dbf4b3d78511bf0186ece0596cb24182fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192004321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78006cb469669ab977f8fd077a5b2c938435cf5864e371445d09cc75a5bea4e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 15:22:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 15:22:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cdc4d13cbbd81c4da28f0a5177669fb5f957466c2f904f98496f7ee0b40ef2`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fdc707494c42458e3bc8fa49c7d2fb3ba9bf7e0c4167b81ebb7da71e88d578`  
		Last Modified: Mon, 08 Sep 2025 21:46:02 GMT  
		Size: 117.8 MB (117835848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7af854b6e1ae3f00efa46e227cb802e00113099fad0730bf0ea79777571937d`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27844f0bba07885733a1a891137be2bb42e3b0fd74fad355ec9aeff9fe2dce1e`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 4.2 MB (4223985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57992caed768086a6c0e311f63782c09831610a3e32216259bdd76df6ae08363`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347ae1524e2ad360b24b4ef2387a9461da4891a4b8ef160eae8ec6ad34ca473a`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce000de9ce8887551c23d5c4567a55797742eb3a0e51305c7bc8cf1fc5ef754`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 12.8 MB (12750151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb1c55e0d2aad7b78b024ae001e27cce8b007128502a87b156bbd9cbdbe485`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b220f5e801fbe37e7f63103f02b4e2a791105442be23ed365551ac089d56cb8`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 11.7 MB (11705702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39fec0932f30c6ffb2c4b45aff32723c845214ce3c82df80f85e0053d04142d`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9df2d0f46cd215f60de277299b2285ecd1b6d40f305e7d230a2ffe293c65`  
		Last Modified: Mon, 08 Sep 2025 21:45:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d9c4eff296fff77f568ecb99d8c3c58ddf7f4643c37dbc869f973660fef40d`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fea5d06223ba540e4224bafb4f89d219c75cba16d48a33102d681aca5ac412`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff9d593534d9e425060c7e9e8f2c2634e6a4edcb1811e15b45f43b08411fd93`  
		Last Modified: Fri, 19 Sep 2025 17:14:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4c1b5e7ae3658ff4d55617f954848314a1c67cc3d7e03c8824dd98c8d9a607`  
		Last Modified: Fri, 19 Sep 2025 17:14:07 GMT  
		Size: 6.5 MB (6537323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d668a4157d1f62306869e044a3f9d86ad6d8ed7e77233a434e51d8bfb43172`  
		Last Modified: Fri, 19 Sep 2025 17:14:06 GMT  
		Size: 9.2 MB (9170795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b23b96a7bc1acd926ba5f754ac34f5b398548e7e6ea14c1c32766fab011244b`  
		Last Modified: Fri, 19 Sep 2025 17:14:05 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a5b113c78c2619a0f364dafa4435568b61fa3247f873aeeb329d79f3e368797d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0c905d397c0eeb18edfb1e74ff209db1cce419a42eae570f62d547c15baf5c`

```dockerfile
```

-	Layers:
	-	`sha256:8e693d90137ce24f322bc79f603d1caf177c87769b35fbd8db7ab65ab3189a92`  
		Last Modified: Fri, 19 Sep 2025 18:26:23 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893b0cc64b6f6bef59af858a58b96cc298530a80501d2179f36d0f06b48488cf`  
		Last Modified: Fri, 19 Sep 2025 18:26:24 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:20700cd4cd616a7144ae225d2cf6447b2751d4f253416dbc047589b6a6b5d4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185412350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8136533a4f9cc76eb02ae1c116539f6517b4b183cd127e351b4c7249164ac8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 15:22:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 15:22:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d62e0cfec9e84e4c3af62f0e2e2f35c0d2b43776e0f833da3bb1be361cef4b`  
		Last Modified: Mon, 08 Sep 2025 22:14:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01edce4cbf0eb2422cf320a499e3b79c2b8237c137a53b113d579a5079ca90d`  
		Last Modified: Mon, 08 Sep 2025 23:09:38 GMT  
		Size: 110.2 MB (110161594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3045fc49f81a1dc00369aac03359529eeceb6141a4335e5cf67a2a71d0c9046`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f798154dd6fce77d2fda99f17287d5cbcac140ce8d069be9a3ad9e4b4a8e2c`  
		Last Modified: Mon, 08 Sep 2025 23:09:33 GMT  
		Size: 4.3 MB (4302084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814c501dc5d5abd4e8a7fff4679a23804a4383866bffc576977ba3017b57c1cf`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9756904f2d1aee01dad39ac804538f982c188a36ad0e860f15f719123765b`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7ae7be6e677d55eef1a130c06e0667ee9370dee36be98d1989329d3d43c22`  
		Last Modified: Mon, 08 Sep 2025 23:09:35 GMT  
		Size: 12.7 MB (12749794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81dcdc4b950a19ba0fda7e25ec63befefb818fea05e64d6883fb99f7c5c734`  
		Last Modified: Mon, 08 Sep 2025 22:14:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7ac0322045582a5bb10d59cf3096964f451c306080af8906ed6b69ea5b6640`  
		Last Modified: Mon, 08 Sep 2025 23:09:37 GMT  
		Size: 11.7 MB (11727427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c25ab495860ad5fb7e2197a0b251a9f46d6a1bde9f3ac630482717c15e49cf6`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf1b55fb275dd6dc7c3058024831c1d0b53f9f81a300e2990c881dbd34fa9e5`  
		Last Modified: Mon, 08 Sep 2025 22:14:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d379843f75a8a85f56c33ddd4e93b94fe7f8096fcab3b1d668282330fac61b3`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7365f6418e40a65d1389c06c279bd3d578b92c67936775d8cabf7198d9ac3da`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121b11ad5dfafd9cfff6519b390bd53a1695400d0f6ab540ee53d9bac13e5520`  
		Last Modified: Fri, 19 Sep 2025 17:14:34 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0707fb9f787648ca97a56af46f3a1fd257eea52b17c2e2623af5e2fe55427a14`  
		Last Modified: Fri, 19 Sep 2025 17:14:35 GMT  
		Size: 7.2 MB (7156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418a72228bd150060fb36e8fffb4fa26fb854ece6a08e5602b0611cbcfa7682f`  
		Last Modified: Fri, 19 Sep 2025 17:14:35 GMT  
		Size: 9.2 MB (9170828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc119aafb779e6094becaed94ad90f4322ca09fa3488d69d5b49e95a67cc5c0`  
		Last Modified: Fri, 19 Sep 2025 17:14:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:e0c144c31ec439842d868d9ff539c8c9bf4fd7655515126cb0793a1d94c58bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297b8853960da3bb85a97a1ae5bf16ed2b5806704590750d6e0b8af8386c3f2b`

```dockerfile
```

-	Layers:
	-	`sha256:3ccb76d036f4855177f63e420b9a45a17619f5371ea17db1db3c39423777cbc2`  
		Last Modified: Fri, 19 Sep 2025 18:26:31 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf57b7b68c0a60aa11b2a4eb923c6d1eb1c33f4d5364660454e5ac24f99e74f`  
		Last Modified: Fri, 19 Sep 2025 18:26:32 GMT  
		Size: 30.8 KB (30782 bytes)  
		MIME: application/vnd.in-toto+json
