## `yourls:latest`

```console
$ docker pull yourls@sha256:4b7a2d17cd5b1f28f9e6d6d926dd9a87c78b689c76ac48026e129a52802b03d9
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

### `yourls:latest` - linux; amd64

```console
$ docker pull yourls@sha256:0dbb6d3712db34c7def13a8f2d2bf136bf04044097a3c8d4dfffb5d023aed94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187044436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4ae4afdefec6279159ebb0f0a001e9f0d507cd057c93756a792ed412de283e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d15608fcc14dc7c2a48e5724770170e76afd70a6065f7cefd253d5dff027780`  
		Last Modified: Tue, 01 Jul 2025 02:18:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a87193ff7f7e81eae1a883dd3c85e0f31f8d9f414c89cc97cbfb4ef122966d`  
		Last Modified: Tue, 01 Jul 2025 02:20:15 GMT  
		Size: 104.3 MB (104331327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3573b8df421c8a3d6e57e2921ec193bd2c3500e90b40c1e3479b037c2841f599`  
		Last Modified: Tue, 01 Jul 2025 02:19:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3f6b5ab28947b4834e2dfe6032ebf285fc723c2958bac80027cd88a9d42593`  
		Last Modified: Tue, 01 Jul 2025 02:20:04 GMT  
		Size: 20.1 MB (20123821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1805524a54cdae78ff3c3e5b75b43ddd1d970d908782b33318be2d3682e97fbf`  
		Last Modified: Tue, 01 Jul 2025 02:19:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2a1f437d42d52a4c61d5726da1fdd33a5f2204889e81a7e36a1622d45292a8`  
		Last Modified: Tue, 01 Jul 2025 02:19:53 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb29edbe6baab640f56ae98dafeadbeec1077ab2b999c522e45c5c394630a225`  
		Last Modified: Tue, 01 Jul 2025 02:19:56 GMT  
		Size: 13.7 MB (13748146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7637339f311ad3e9d4878a56191102c8914b136f34302c087eebc579bc44a`  
		Last Modified: Tue, 01 Jul 2025 02:19:53 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a800e4b60c3b892653e80b5b512a3ec754f46954398f462d6fa02f8c48fa8194`  
		Last Modified: Tue, 01 Jul 2025 02:19:58 GMT  
		Size: 14.2 MB (14169664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257ba648704f66d7165e84ef68c389a16578db7b9a09780e1af4f62b2180b49c`  
		Last Modified: Tue, 01 Jul 2025 02:19:37 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fdc4d21920ab89b0df8263cc2a2b7d6464aba79759f1a97cbd209d024b4859`  
		Last Modified: Tue, 01 Jul 2025 02:19:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e2858e73d168268d9d4f9f8bf17ece27c453dc3028ba5bbb7ea5c47ac5d8a4`  
		Last Modified: Tue, 01 Jul 2025 02:19:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800b3fe93cf91b5eb08687f718c5862c09d11d1d232fed1cbdd057c4eefc81b6`  
		Last Modified: Tue, 01 Jul 2025 02:19:38 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d741e9f91d152e70ce20783eaa76c44ce3086b8488dcc57fc9efbdb184e1a170`  
		Last Modified: Tue, 01 Jul 2025 03:20:08 GMT  
		Size: 663.3 KB (663255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd23d2405b654e7ea8efce1c16d99c8bacdea4a384e60d167b1672fb9516d6b6`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb947283328a733ed6adf5ca7bdd348ecfd69160b9851d21fc8e7a9b1304610`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f5b4f7e38611ef542c4e5182ac4e3252959154243e82149b8b1b2394d0547a`  
		Last Modified: Tue, 01 Jul 2025 03:20:08 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df05836650c9095ed8fad7d49b4ae63569c32a48f3e823e4e0b8d3f50f00f32`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5e35f073ad766937203ca550b633c25b9c2ef2cd580c092de07c87eed7670b`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de9a40edfd9de9d22ef5a912b5f43f536a19ce4c015fd6ac77f9495e568766`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:de394dfb611aadaae058f69a25bb4c2eb864503586d4a5612b710c654bac8b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086d37e34f1053c0347ab467e14b002abce9304e36e5f4f4d1c5157150ab5dd4`

```dockerfile
```

-	Layers:
	-	`sha256:d38d6b983095ef0fd2d3bda4482080ddad9cdf535741a71c1d23c34b45f51ae0`  
		Last Modified: Tue, 01 Jul 2025 04:42:30 GMT  
		Size: 40.2 KB (40241 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:6f4c6241b09b41bb464b02a4ce6837cee179adb03ac2759cfbb7f9c9f6fb9a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159771052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82f5243167fec3978ea190401037648669bd048c0532f4114266e5e6fdf02c5`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:1601706ea1ce67f559cb97c579c16dd941d3841c0536aea9a41a8892de970a15`  
		Last Modified: Tue, 01 Jul 2025 03:07:29 GMT  
		Size: 19.4 MB (19418152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e91d03bdddc0ecb98561647c397edd946b0e408f3e4b937dd86f102157fe`  
		Last Modified: Tue, 01 Jul 2025 03:07:28 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8793820eb88ba267b7037f6242d4786a223433f5744eebb87088af136b6b8015`  
		Last Modified: Tue, 01 Jul 2025 03:07:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b1c012007ceb1010304a08e6fa660bf875f3f3695ba07b265f981b8852b44`  
		Last Modified: Tue, 01 Jul 2025 03:22:36 GMT  
		Size: 13.7 MB (13746055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdaa9b182751fa08ee8f93dbe370d875dfeeb3c46cd2346ea2fef5e95d005e6`  
		Last Modified: Tue, 01 Jul 2025 03:22:33 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce0ef1967cb1becd9195cc76c855aa2951a0c5ac985d1ddd91132107d0b5ad`  
		Last Modified: Tue, 01 Jul 2025 03:22:35 GMT  
		Size: 12.9 MB (12919236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c733efc7fc688f32d47996322730f0eba80ba938c13e850bfe3486df8c7cfa2b`  
		Last Modified: Tue, 01 Jul 2025 03:22:33 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e406458f528445f4711ad1fd8b3ecceebf3f341f92d97b207c22ae1863e0793`  
		Last Modified: Tue, 01 Jul 2025 03:22:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58e8596476e83f7e37cd116a83119f99d4dfb107583b7d0eeadad08838ca818`  
		Last Modified: Tue, 01 Jul 2025 03:22:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da65818096a93fb5d85d24dd9278920878b39f343f38ef623a3230ec2b6cf58a`  
		Last Modified: Tue, 01 Jul 2025 03:22:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67919045ccd6efe6c77d504bffcb9fc1809ee1ee0585901fc81d071aebd537ae`  
		Last Modified: Tue, 01 Jul 2025 09:26:32 GMT  
		Size: 173.4 KB (173426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf4e0b72c381c96e3cbceab99ab47462460042e9610f70904c349614e9c4fbc`  
		Last Modified: Tue, 01 Jul 2025 09:26:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb3de0e1185f180baa35c00b77409cb637b8a9b6bc9f64e65d59a4ec88c1246`  
		Last Modified: Tue, 01 Jul 2025 09:26:32 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab5c72c9d2543cf3344f8699c025a2289ee37ecc962b53ef307124c2f2c13b`  
		Last Modified: Tue, 01 Jul 2025 09:26:32 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d454c8f49d4ba56cb8f2063bf09cd53bcaf35893ab8391ab7154ccd01a5ec2`  
		Last Modified: Tue, 01 Jul 2025 09:26:31 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c39196b6aaf5e76351d7f8168f9f7687454a7ab5854119a15afda68048564f`  
		Last Modified: Tue, 01 Jul 2025 09:26:31 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c6b2fee4fe5564fccabe2705b8df7c488d6c5c88381b94255888687bb40b16`  
		Last Modified: Tue, 01 Jul 2025 09:26:31 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:bd91a7b40cd1f85a78ae6ff62b6c32e6f30ca088afd8ed17e137c59b81579c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad816d57c26283e30eabbe7558e6378e2882d3590552a73a26242482d4adb50`

```dockerfile
```

-	Layers:
	-	`sha256:591522da9e284966899c23cc98b9c0d72ce3ca761cdbe4cd3454f3202fabbc13`  
		Last Modified: Tue, 01 Jul 2025 13:42:35 GMT  
		Size: 40.4 KB (40380 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:505c5fb8328e90e64549e4e54f7c1f0394254b78d81ec180d3663da73f03a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150909649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7369f95c9694fec9a01c9aff8d3cfd48517b51ed7d6ab5ad5ce840959cd6cf`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:4f48e36c51ca567e00204b7602dd2f3197ed65c785e21a191aec888d5acbe886`  
		Last Modified: Tue, 01 Jul 2025 02:40:42 GMT  
		Size: 18.9 MB (18855730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739500a213db554802bf5a3a6ea64baa201f9a9e42247c34a186877ff2824052`  
		Last Modified: Tue, 01 Jul 2025 02:40:41 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a65a3ecd90f92c07f97694692d2624d48f057c9b5aa300524021d73c2c682a3`  
		Last Modified: Tue, 01 Jul 2025 02:40:41 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8555c9c8953303e8be9e1e2e80d470e5150d29ccd48385bdd8e21abbcfe6e`  
		Last Modified: Tue, 01 Jul 2025 03:09:20 GMT  
		Size: 13.7 MB (13746026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0ed43a5662f22ff48ed006e63b96d6f007e95949f6c03cf8e3146c5016f105`  
		Last Modified: Tue, 01 Jul 2025 03:09:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fa83012e7d49aeda9a0fa78305b3327d88026fe8cf8050e4eddaf3548f4008`  
		Last Modified: Tue, 01 Jul 2025 03:09:20 GMT  
		Size: 12.3 MB (12282205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fccf1af63ee526e165bfc6c4eeb893e3ab27860911e2ac731a17211a08f96f`  
		Last Modified: Tue, 01 Jul 2025 03:09:09 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc12093abf3ff15a2d3f27580f7736c8cb803b2a2b2316f2354578d60d5bb48`  
		Last Modified: Tue, 01 Jul 2025 03:09:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec82ed815fa1e6c09b53c2a42c1578fcb4080c8ba07713e7775d96c8607bb95`  
		Last Modified: Tue, 01 Jul 2025 03:09:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394e8851d2f31eec78011b7d3c2957bbe41012222fe0ec6b2c3e0c47142ae8ec`  
		Last Modified: Tue, 01 Jul 2025 03:09:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e4dcfd17527eaedac18a4f9a52fc330ed000e35974ee398568a9af69b5ed69`  
		Last Modified: Tue, 01 Jul 2025 18:27:28 GMT  
		Size: 159.2 KB (159226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a13e702c3a68f17b831fdc0e5422cf63a258808095af4e463652195303247db`  
		Last Modified: Tue, 01 Jul 2025 18:27:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a40df148c724d3e2919e1261f0a4f11bdf27e3598354399c15674ce83b7ab8`  
		Last Modified: Tue, 01 Jul 2025 18:27:28 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906d6e7ace0353525d7e656b549b6aa30249e1b17c735f1bfe2541bba1e38dc`  
		Last Modified: Tue, 01 Jul 2025 18:27:29 GMT  
		Size: 5.8 MB (5767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74bad12cfc416c6f6f7418f356d1274f6b0b9efa6e64c3e1dd564f6fa07922`  
		Last Modified: Tue, 01 Jul 2025 18:27:28 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9b52b942421d110c5ec96eb78c41a15f84775b840af3754bf70d18be4ce997`  
		Last Modified: Tue, 01 Jul 2025 18:27:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2942d83c0a7a72485b00f9cb81d743d4d07b14c9d9450ee6cad65c4314aec99d`  
		Last Modified: Tue, 01 Jul 2025 18:27:29 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:0d87343a8df2d559e15c5dec89d42a3baca2f4a3f31cf09c1a538002fcb56940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ae6fea0876e468f20d9359a46b2d7f059c0cd0f91cde008683bd0932a5bf4a`

```dockerfile
```

-	Layers:
	-	`sha256:f8a4c6925ab1ac3cb43e9b0b65b9006b95b3fd78b540a677391a03e017634d93`  
		Last Modified: Tue, 01 Jul 2025 19:42:28 GMT  
		Size: 40.4 KB (40380 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:3b9f1e547f2e11977708579b95899994e6f5523078556e173c4161358fe42b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180258415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cedff2381a626856b5c3bcb7dc06763efb0eb366ad8b274cef82a8e82826ee3`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd1331e00b948007fed4efe1efe28dd101c09233e14bc0a08f8a0b9df83dc83`  
		Last Modified: Tue, 01 Jul 2025 03:46:32 GMT  
		Size: 13.7 MB (13747929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9059088cb44db06ba0fcc1770c8e50c634eb809e27d09b4cf215d7057af655d`  
		Last Modified: Tue, 01 Jul 2025 03:46:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea12fcf745b58756489bce91e410133727e6a61ab3dbd2cf036d3c34f44f7e`  
		Last Modified: Tue, 01 Jul 2025 03:46:28 GMT  
		Size: 13.8 MB (13810435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c95882f339117126293a28daa9969ce04c0262f82fa124b93774708743b6d`  
		Last Modified: Tue, 01 Jul 2025 03:46:28 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c6e0d706961277adeafdbaa8e11f3ac7b1782200ccfb2d6b61bfc273a78180`  
		Last Modified: Tue, 01 Jul 2025 03:46:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cb7a0108c4d7cd91e61e9e91fe010e6e010a8df9ad8465520daa30464ca059`  
		Last Modified: Tue, 01 Jul 2025 03:46:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08c8ac6021fb2a3b293ca172f731e82f1bdeb1ca8a3dc80bf5e4d83e59033b`  
		Last Modified: Tue, 01 Jul 2025 03:46:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6adc97282ed63f9a7049a97b88aaa5962bf344adbcd4b13b317df777010856`  
		Last Modified: Tue, 01 Jul 2025 13:24:16 GMT  
		Size: 577.4 KB (577434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d154ce12a3858b774fe22b4ae3414bb67a1f64472b4ae2d7527502e8f0c4670f`  
		Last Modified: Tue, 01 Jul 2025 13:24:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5d64930c37f72ae9d98277d8484ac19bf42054038f5b119aed10fcd5076ae7`  
		Last Modified: Tue, 01 Jul 2025 13:24:17 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ae8d23ad1e2ecfada012239a6862c96221f6a47c46451b24757b83021f993`  
		Last Modified: Tue, 01 Jul 2025 13:24:19 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6490906bd995bcc7500b535380d2172ea35247cd1e1cfa8b560890a232859202`  
		Last Modified: Tue, 01 Jul 2025 13:24:16 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5cf8158039087699d13ae554764fdecb92b6a07ab62558c4a4ab4700730fa5`  
		Last Modified: Tue, 01 Jul 2025 13:24:16 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c9789aea4acc245154189cd6dd9c595d653c68e3089cedc402c4564e7b141a`  
		Last Modified: Tue, 01 Jul 2025 13:24:16 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:4cf896494cc583fee3e8800f08089e519f123fb423d2e6a14cea7e696502e073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440875f21dbbeb57c231c7de76a4c4567881c5972d344c145b949e3bdcdb715f`

```dockerfile
```

-	Layers:
	-	`sha256:7a8936c12eb7361d0b811e01fb4e72d409042fa4e82c9c5a9a497fc8d362ab0a`  
		Last Modified: Tue, 01 Jul 2025 16:42:30 GMT  
		Size: 40.4 KB (40430 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:eeb1dce8356c4bfb84cad93a217d43990c191ddbb8236f99583f0c0b6fcf224b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186041391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34cfb175fd20326dddd31a180682e30c8f10187f115f491b58f2f056f63e05d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdf0ebcc4cf9c7bbe8b82f9a54c1f7e5a1fafdb8c54e5b037281fd99fb89a7f`  
		Last Modified: Tue, 01 Jul 2025 02:18:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b46cc2ba133efaf7c51628053fca0cfa0dfa19a29a3fd01a54b940b28df5d6`  
		Last Modified: Tue, 01 Jul 2025 03:19:04 GMT  
		Size: 101.5 MB (101515170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08be1330d4da0bf120c3b2589763841c35c8a96f29e9ac5e86619191101057b3`  
		Last Modified: Tue, 01 Jul 2025 02:18:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99aa337eda64b871c3420622b39d06d16c7f24a2144c818e77052973725dc7`  
		Last Modified: Tue, 01 Jul 2025 03:18:58 GMT  
		Size: 20.6 MB (20638485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c4c80c730e08f5437158016ad4daf0d58dd6999701433624fabb005fcd7ebd`  
		Last Modified: Tue, 01 Jul 2025 03:18:56 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27092c77149a9d3729252cc29a6388d2cf266f52d46bdc6f304000bf2b133f9a`  
		Last Modified: Tue, 01 Jul 2025 03:18:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57753f27df41be03d6f81dcb6cfa01a8ecd92c0c4a57a2a164396c1cb78bc132`  
		Last Modified: Tue, 01 Jul 2025 03:18:56 GMT  
		Size: 13.7 MB (13747056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11127fa27055d8fcdb475b256d46ee60c888757c40c483aa9e51ca7576e70b78`  
		Last Modified: Tue, 01 Jul 2025 03:18:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96403d4ba4b6296167fb69caebe409acd5827a871c35f354afbac375d79e4c1a`  
		Last Modified: Tue, 01 Jul 2025 03:18:56 GMT  
		Size: 14.5 MB (14463106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9055a4f96b0da896684536e249be03a1062ef67a0c26a41d411a9fffe3d4e3d9`  
		Last Modified: Tue, 01 Jul 2025 03:18:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229b165f78d62e1e79a37d7026c3bfccec64dedffef61f6a5dc96a2e2d06e5`  
		Last Modified: Tue, 01 Jul 2025 03:18:55 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9644511251fbdbba6242ca9218b0559a425b63e7aec5c4d469331dcaafbd64`  
		Last Modified: Tue, 01 Jul 2025 03:18:55 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e9804756fccf4911ee0ac7b7394688fed6d01b25c275f8e21b2f3d404ff3eb`  
		Last Modified: Tue, 01 Jul 2025 03:18:55 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a4d4619507804dc3b9b56031fd4d9c1e441a462407a6f162dc98e8f66589d`  
		Last Modified: Tue, 01 Jul 2025 03:20:24 GMT  
		Size: 687.0 KB (687050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bfe243356ec00941913fb72cb54e7486181a301e5bab182a735e51d75885e7`  
		Last Modified: Tue, 01 Jul 2025 03:20:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e6140b3d9418dcf741e7e7df2a14a7415eb40f724ed896b1ae06d42bed0e9`  
		Last Modified: Tue, 01 Jul 2025 03:20:24 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69552040655bd7bb550ae7ae9fcac2fa7a4b50fe7835e49bc34ee1bc44fecc6`  
		Last Modified: Tue, 01 Jul 2025 03:20:25 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e4ab203ee8c2256932ac3ad6cc04c8b2864d270dcddeee8f4683f0fb54255`  
		Last Modified: Tue, 01 Jul 2025 03:20:24 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ad05cd902264ee4cda9cbcf725338ade06645dc2d28b1b61535375ee06c13`  
		Last Modified: Tue, 01 Jul 2025 03:20:23 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a75f6d5e5b299e5a68f86bd48e3f539cd8b04e2ee9bbfc3719241ae210b0e6c`  
		Last Modified: Tue, 01 Jul 2025 03:20:23 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:32edc3e3775a13cfb5e810dc1bcc5ae45b6e006fd309fddc1fce2dbe44c8e68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0550c7632198642fba5fc4e903adbc27cb8204dea8809e0536a45b65b5252e17`

```dockerfile
```

-	Layers:
	-	`sha256:5e2b397d07a13e72923f52e6ee2600ddc52a4fa2fc59ff4467141bfb6f8b3666`  
		Last Modified: Tue, 01 Jul 2025 04:42:42 GMT  
		Size: 40.2 KB (40183 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; mips64le

```console
$ docker pull yourls@sha256:7f348f49893aca381422947814674d8d291a66e798df7005765e94cc08c56196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162014105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50402682ba2e32306672c32e1eb481ce082b21740782155534e6d5f00b1f2e8`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbaad9c575de27a78ec9ecda6c0f021d7843e351bd682abc01e8edfe52f3239`  
		Last Modified: Wed, 11 Jun 2025 01:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6a316d668681533c7b3478f23726ec4bacd15c983a623a42fa361b70101e1b`  
		Last Modified: Wed, 11 Jun 2025 01:37:09 GMT  
		Size: 80.7 MB (80670453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cd671d1ab5d1868581d736fae7d6e8644a5d539113a35ec3166149f5fc9c9`  
		Last Modified: Wed, 11 Jun 2025 01:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06711b2029b6e716b281e48add36e348d45d6e800fcb090dcaa6bcd7bfc1866`  
		Last Modified: Wed, 11 Jun 2025 02:13:47 GMT  
		Size: 20.1 MB (20069206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e9bb8bf9ba95bccaa6b37ca93e70a712b5b3fa91b06c76b60c7af5b2eeb0f`  
		Last Modified: Wed, 11 Jun 2025 02:04:03 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba7aa4e251348058de69a8466cb4f6e23ab562dd7bca8ab98c7e96c92d640e`  
		Last Modified: Wed, 11 Jun 2025 02:04:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70624c40eb1f12c343152a2038bd215aac49584d55abba9ab07b242c9b412005`  
		Last Modified: Wed, 11 Jun 2025 02:13:47 GMT  
		Size: 13.7 MB (13745883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa734eef02f6a307b84b27d0e14a768228371b52cb985b5fbb3991720a1979d0`  
		Last Modified: Wed, 11 Jun 2025 02:04:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f03858565a49dfe4342d01a6f8dc51996c0b9927fa1408f1910ef20e2b46fba`  
		Last Modified: Wed, 11 Jun 2025 02:13:48 GMT  
		Size: 13.1 MB (13063421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7fef5e4e59abe9cc594e62d4807262f68a712a5d5f8cf6d9d36e4c4826a1a`  
		Last Modified: Wed, 25 Jun 2025 19:32:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487873eaf964fb38fd9aa868152dc1c93077df3573458fbd8bff8bc2a86f1e87`  
		Last Modified: Wed, 25 Jun 2025 19:32:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259064cd1ba652a7b0c91a4f65bfbe65568a296c57f7931e9c3d4cd3456276c`  
		Last Modified: Wed, 25 Jun 2025 19:32:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c674aa938050a51c55b7c5cfd7c7089c2ff8d214af49422a6bfd75244ba495a`  
		Last Modified: Wed, 25 Jun 2025 19:32:25 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b9a939b7a4396031e49d37ca4fb90b5d6d78f958d6e511a5e0f96c49a2a0b`  
		Last Modified: Wed, 25 Jun 2025 23:19:18 GMT  
		Size: 170.3 KB (170276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1141f64235b41331cc85c87908627aaad14b3b4d4344e50c7fcefeca15135ef5`  
		Last Modified: Wed, 25 Jun 2025 23:19:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7918adf43d1ddfad5737f831f8015ab663f6ffb45f7c6ed29e6a0f4e25eb11fe`  
		Last Modified: Wed, 25 Jun 2025 23:19:18 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07f0935d51d8d44589bb33175301c78be43680d01fd4177b986d0fa73c0787c`  
		Last Modified: Wed, 25 Jun 2025 23:19:19 GMT  
		Size: 5.8 MB (5767594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6086f0abb87f6cf0403d6ae180561b6b2ae90f6ce37904da0ebeb616466523af`  
		Last Modified: Wed, 25 Jun 2025 23:19:17 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bcc495f62be46a4885b95f5f76d401cc71c312b4d99c1f36f509fb00295002`  
		Last Modified: Wed, 25 Jun 2025 23:19:17 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00f09b7e3b044b9052f0c7600e01ae0ea7a51da09b5c30926b5954fdb79bc5d`  
		Last Modified: Wed, 25 Jun 2025 23:19:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:08d3e3febd2d5638c027eb54749bdd6da5ef7fc8cfde48536203bb3ff7fdd2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eed5112a0f43c66c0f6f5203a50f2f361f4400a9437e095a50b67e6dad1f03a`

```dockerfile
```

-	Layers:
	-	`sha256:1f37ea25b16f012a5a4b457e55e3950d61d1ada698cdd3f478c8a8ea3696788d`  
		Last Modified: Thu, 26 Jun 2025 01:42:44 GMT  
		Size: 40.3 KB (40344 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:3f8c9fbcfc6994c11ddfb537c0c47258f520ad1f39c4b6028552f1d4941b0601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191032064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4379973862a1d91d3337aa84cdb7bb315e7ef9e0b98d69c116bca1378a2023b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:c4ed49ba7119690733e3d6ea549f616e27a3c2373536949c5f815f3016ee36d7`  
		Last Modified: Tue, 01 Jul 2025 03:02:55 GMT  
		Size: 21.3 MB (21308312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479685b6a0f37fa82ae54089bd94827adabd1a9762de07bf56c1d446529ccf77`  
		Last Modified: Tue, 01 Jul 2025 03:02:53 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6d05d1ea304b3577242e86313ab57d4487f5a6b60d212401488afbc705451`  
		Last Modified: Tue, 01 Jul 2025 03:02:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383461a4a23092cd08eb08eb5be35bf4c1fe7770d20d77bd756522cfcef27442`  
		Last Modified: Tue, 01 Jul 2025 03:19:05 GMT  
		Size: 13.7 MB (13747575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b85511e608150ca26e1aeb39db5ba318d2293d30ca15c9f459d9c667dacfff`  
		Last Modified: Tue, 01 Jul 2025 03:19:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f53bb362f4a8f0d2f7288b6ad72f39ad312b78c7fcd038a38ef68ccf9deca`  
		Last Modified: Tue, 01 Jul 2025 03:19:15 GMT  
		Size: 14.6 MB (14587929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdff91282c039a86f1db01484f8787ef7adfdc8136ff0df5c85a03a01d03689`  
		Last Modified: Tue, 01 Jul 2025 03:19:03 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5e7f008c58edbb57b446be0bf835011ce18429d83331b999c3515903089ac4`  
		Last Modified: Tue, 01 Jul 2025 03:19:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8a90c7fc887277e7a78410a57241231928dfa200446e233a221a99b7a7019`  
		Last Modified: Tue, 01 Jul 2025 03:19:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8ca24e68b8608676ab356c38ab0982fd90ab54d94517eaca3d5e232443d32f`  
		Last Modified: Tue, 01 Jul 2025 03:19:03 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70633f6490cd53f3f3e96304626098c0aaca0444133d4ce6d7932e41e261dc5e`  
		Last Modified: Tue, 01 Jul 2025 13:43:14 GMT  
		Size: 210.6 KB (210588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9964c980fe395692fcfff8702df76ba0e61f727096dcca455beeb3529cc8c021`  
		Last Modified: Tue, 01 Jul 2025 10:09:31 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7f351e45fec375a9d7df1a26e96ca74fe0d6382c83bba206ae96bc5778b0c7`  
		Last Modified: Tue, 01 Jul 2025 10:09:30 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62785a3bf0d1664972ea3cea9d7dcce09fb3034d92e3e11d645b59a78f1ab954`  
		Last Modified: Tue, 01 Jul 2025 10:09:31 GMT  
		Size: 5.8 MB (5767594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ccdeae83a13de1d84d7ac511e308381058d9350da0752f41b5465b93094d64`  
		Last Modified: Tue, 01 Jul 2025 10:09:31 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7cf98b2ef5fe51d22f6f5f6b83fa777906a66c2dc4bf7386484fbd6e73c1c3`  
		Last Modified: Tue, 01 Jul 2025 10:09:31 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661c4a87367de1977576c34774c6740606863ec3269cacf2f34b670cec462135`  
		Last Modified: Tue, 01 Jul 2025 10:09:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:d5b194be5ca16b84cd9fc85131be993d030cd132655367363b059ac7c2bf37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3365fa7439eda774a8bb3fa3676711b765ae9872248d1fe7f610ad3f247010d6`

```dockerfile
```

-	Layers:
	-	`sha256:922456d20284579309f51f906646c15cb609ef2a86c021a5ea7167fdf2527a86`  
		Last Modified: Tue, 01 Jul 2025 13:42:45 GMT  
		Size: 40.3 KB (40315 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; s390x

```console
$ docker pull yourls@sha256:65d5d60a97203cbe044972ff470869ddc50eccc4bd83153a120d685049ea39d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160853757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4537f9af2f61c0fa3ac8173b7cb1db874278183755bf6bacf3e9c8f62e63c125`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 25 Apr 2025 02:48:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Apr 2025 02:48:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:ab9f74fd63de9f24dccaa964cbc47698e5756777534bc5ee439c4ca7d69674d8`  
		Last Modified: Tue, 01 Jul 2025 02:45:56 GMT  
		Size: 19.9 MB (19895178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a092e0e5513f647567d630997b4cf552470a2029e0743a2a151d0bd02b65d`  
		Last Modified: Tue, 01 Jul 2025 02:45:54 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a1fef030de7b1908ef166e1bf67a5eda769c65bde46210584c1d1cf8dc3b7`  
		Last Modified: Tue, 01 Jul 2025 02:45:54 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bec3b08dd96cea4dbb2e0292150469912656ae74564f62b8be76678e7e53729`  
		Last Modified: Tue, 01 Jul 2025 02:59:56 GMT  
		Size: 13.7 MB (13746327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd42133e83d1b87a43089d28cf6831ba6d6a1231deca812ccafc9dc34d49e1d3`  
		Last Modified: Tue, 01 Jul 2025 02:59:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955cd0006e94a0ca8aeebc3c1729808638d2b327da059205275377c6cb382917`  
		Last Modified: Tue, 01 Jul 2025 02:59:55 GMT  
		Size: 13.5 MB (13540452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa26d0a10ff4f985064abd00933cd6bd82ca32601786009cdd3eb7b76b1d39c5`  
		Last Modified: Tue, 01 Jul 2025 02:59:54 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dca138dcb7f9254c99bb2c1e2b1d7a68311d8221aba9ecc38a112da41a7ba3`  
		Last Modified: Tue, 01 Jul 2025 02:59:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e189b4d00632ac3dd2ba78092f86f229ccb3a79aa44ca23aef48498d0beee1`  
		Last Modified: Tue, 01 Jul 2025 02:59:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecdd8b46475a7dac25e155d9736ad8d1c0aa3b0ece5ab0629b48dc636c06f24`  
		Last Modified: Tue, 01 Jul 2025 02:59:54 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b99acdcec0352921fdbacfa7970f312dc1a68f30c47a0f8c94d95a6b95f67a`  
		Last Modified: Tue, 01 Jul 2025 08:54:26 GMT  
		Size: 179.9 KB (179930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2687ac8007a5e964e3a118aa002825949a0699170366302b51da1824cb0aa88f`  
		Last Modified: Tue, 01 Jul 2025 08:54:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf53c3e08ca553e435065a3c1aa41ab8d5f1287b950ad4be5afe36c2fd84eabe`  
		Last Modified: Tue, 01 Jul 2025 08:54:25 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6112ca8827cd5e18417a908c5fb2f33de6cbc6a09732b624d7d0bbd8d008064`  
		Last Modified: Tue, 01 Jul 2025 08:54:26 GMT  
		Size: 5.8 MB (5767595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dd1e1973048d8ef9b2f010b6f8a14576a66ad89c48c434d0b441ae8c585086`  
		Last Modified: Tue, 01 Jul 2025 08:54:25 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a204290023c3a987671a58fd3632fbb427e54b4aa838c58fdf29d5b603e40c85`  
		Last Modified: Tue, 01 Jul 2025 08:54:25 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830be6baa4bb5368021f21567379a76b026cbbf1b74d6b937c519fefa665f9b`  
		Last Modified: Tue, 01 Jul 2025 08:54:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:51b3608bfecf6404263b3e5faa356c718958b35f598e84cfaf687cfae1073db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb95ea69f567d659667f2a8892823d32b48c4190683b8dd1092452834b32a777`

```dockerfile
```

-	Layers:
	-	`sha256:8c06eb255e6549c1efeec17dce8211fd4c629724b302ffea45dc85e69008177c`  
		Last Modified: Tue, 01 Jul 2025 10:42:45 GMT  
		Size: 40.2 KB (40233 bytes)  
		MIME: application/vnd.in-toto+json
