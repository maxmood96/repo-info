## `drupal:10-apache-bullseye`

```console
$ docker pull drupal@sha256:fc4dc2cdb3f9e5dd105a5c191fbe55b69c45c845888809411db1ad54ea55a617
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

### `drupal:10-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:6a116091f367ce7711bbc49fd37729e609da9073a61b6f95fc65122e0be82b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189427805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e325a3a7ffd2beb42e80e3356d8944c9d1471f638d9dabdb2a2d80b0b77b0d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 03:27:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 03:27:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_VERSION=8.3.20
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 03:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 03:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 03:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 03:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV DRUPAL_VERSION=10.4.6
# Thu, 03 Apr 2025 03:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /opt/drupal
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476dc813534ee2de18bd714d853a4beebd6cb9b57bfe1701c541bd1db90c5e4`  
		Last Modified: Mon, 28 Apr 2025 21:53:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d94d66bdc51d80d8e96ee87beddc532321b72e123b4a577596e94c601576545`  
		Last Modified: Mon, 28 Apr 2025 21:53:28 GMT  
		Size: 91.7 MB (91653760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb50faa11ff35e67ac2478c72d55dd7a0d64ea82d7d33c7fc4e43048ee3421`  
		Last Modified: Mon, 28 Apr 2025 21:53:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1994953ea371a2e808d550ea3770a7bb6ee9e73d5e90bc064b54a00f988279`  
		Last Modified: Mon, 28 Apr 2025 21:53:26 GMT  
		Size: 19.1 MB (19064130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bfa5cb30a4c0e0a2614d132e8b5c7e9e2544b890153ba8fd18eb0675228073`  
		Last Modified: Mon, 28 Apr 2025 21:53:26 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab76726459f0c155281fc43d63879373d3826f6d6cb13001e7c466d409b12b07`  
		Last Modified: Mon, 28 Apr 2025 21:53:27 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452f0d0a588caa878d57293ff699c2c1a72ca02dccbdb946704fe6843d98fc56`  
		Last Modified: Mon, 28 Apr 2025 21:53:28 GMT  
		Size: 12.7 MB (12673941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb16db4082e959aaa712da7d51103ef6a07c8eda74abf71aaae257dd4de5a`  
		Last Modified: Mon, 28 Apr 2025 21:53:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ccbd0c4bcc429cf7331bd870d6721ceba3ed0d07ab822cc7a970d3dbf5d256`  
		Last Modified: Mon, 28 Apr 2025 21:53:28 GMT  
		Size: 11.6 MB (11599522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c17afc30cf2e25a3eb91229a6fcfba272b328327554271c5844ce908c1a4df`  
		Last Modified: Mon, 28 Apr 2025 21:53:28 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f168cd38a293864bfb0a1ac30f6c4fcaae8494d0d2c389d2a5c64237dfeb9c`  
		Last Modified: Mon, 28 Apr 2025 21:53:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a009e474540bf2f521f407e1b6b178f789c847d52317c6a699a1b7545b50e82d`  
		Last Modified: Mon, 28 Apr 2025 21:53:29 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567e63cfb120f3d8a19747fc9f92290cf8eb42d926d18f85b6b29b1bc11a95ca`  
		Last Modified: Mon, 28 Apr 2025 22:17:35 GMT  
		Size: 1.9 MB (1933215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184680a05e92c343825389353e467541eec7fee164547e896b588192824a4123`  
		Last Modified: Mon, 28 Apr 2025 22:17:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f3407839aad9861e4f871bca7807301935aac39592b9a8e594395c708e333c`  
		Last Modified: Mon, 28 Apr 2025 22:17:35 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996297b4641187a5d5469781d023cb845c81fd289e375f3387040ae93b3be8f2`  
		Last Modified: Mon, 28 Apr 2025 22:17:34 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100ce7f3b27fe6d3c7f737a09c5a7463a3258dd11cb3c2fdb1a8a104f1c733a7`  
		Last Modified: Mon, 28 Apr 2025 22:17:36 GMT  
		Size: 21.5 MB (21492128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:395a6ec4697eeffbb7e150a70d2950242f46364a55928175d01f91fedb7c950d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7069129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adfe0afbe45b9a05d3f762503ef69b1e30b34bb248db44c397614ff9509eaca`

```dockerfile
```

-	Layers:
	-	`sha256:b2f223546e72e291615443600789b03bf692bdf870f5e8a8b7159b1b50aa0e3c`  
		Last Modified: Mon, 28 Apr 2025 22:17:35 GMT  
		Size: 7.0 MB (7031789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45eccf42b0bebf5196ce8b04ff308c30e8cef709bd0bb219cda6d640ed8b81be`  
		Last Modified: Mon, 28 Apr 2025 22:17:34 GMT  
		Size: 37.3 KB (37340 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5c0f5fb11f9ead8e8d984be1f5629f896d15cfec2fcb06a906ef1af111934eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158946289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a81ab49190f785aa8d9984ce6a252b79d0547b7dc4d9909f6e9d8337edee6d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 03:27:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 03:27:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_VERSION=8.3.20
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 03:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 03:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 03:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 03:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV DRUPAL_VERSION=10.4.6
# Thu, 03 Apr 2025 03:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /opt/drupal
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5fed3526aa9a655f9051583860faef7fcc89d2b8dd45cbb36330f794b823`  
		Last Modified: Mon, 28 Apr 2025 22:53:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234cc059c4c04843743476aea79a8338e98813c033c7a8a6d11a05b306c529af`  
		Last Modified: Mon, 28 Apr 2025 22:53:24 GMT  
		Size: 69.3 MB (69324676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed313b30099a075eb05bf4a036c81061e7355fa5dbb96437932389a84592afc2`  
		Last Modified: Mon, 28 Apr 2025 22:53:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56081453e73ac66e871e927c5fc02cb58e9526ec2a96bde362e2d63a3c19a3f`  
		Last Modified: Mon, 28 Apr 2025 22:57:12 GMT  
		Size: 17.8 MB (17817249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec360212b8527b702dbf9d48cc7b37ab97c4ea05e4f5dde1064f810559fc12d3`  
		Last Modified: Mon, 28 Apr 2025 22:57:12 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15419f0759ae9faadeef72ce79af07c24c41b2361426b4b061d2c34acd3de93`  
		Last Modified: Mon, 28 Apr 2025 22:57:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bc26ca3e15d44267e7651af9c70228cda981721da4a2dc40ffd9084fc91e45`  
		Last Modified: Tue, 29 Apr 2025 16:13:40 GMT  
		Size: 12.7 MB (12672411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ce5895dae9b2a4bcc055de2b826e16c25b9fa4718c1c0f791b056ddbeaf899`  
		Last Modified: Tue, 29 Apr 2025 16:13:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8d5e239216ac30a0fb1753f46efa39332266fd11cfb8054f5eef9190f3d2a8`  
		Last Modified: Tue, 29 Apr 2025 16:13:40 GMT  
		Size: 10.0 MB (10029567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c07caf588ee969ac07d5541ec53fd39d65f28f079ccb8671f0fb183a83e7c1`  
		Last Modified: Tue, 29 Apr 2025 16:13:39 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4001c5de32e1d237361c7f86849f9d8a263819ee1b2223bcca09b56560d307`  
		Last Modified: Tue, 29 Apr 2025 16:13:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6330dcd1c5d3f5760c5cdedf8da5368afc45aef474e8e128a06678b13ba9622f`  
		Last Modified: Tue, 29 Apr 2025 16:13:40 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cced59868cfe456040cef6f54558b30e0be1f4da463bfcc4a929026a0e6505b`  
		Last Modified: Tue, 29 Apr 2025 16:52:14 GMT  
		Size: 1.3 MB (1311997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bfa9cb60fa268ce60802256e2e47d84f35d791f03b98f3b2a3ad7b2529bcd`  
		Last Modified: Tue, 29 Apr 2025 16:52:13 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b4009df5df4de8e5a6e738ef5ee251f66a1313681dc00a351a8245c514069`  
		Last Modified: Tue, 29 Apr 2025 16:52:14 GMT  
		Size: 750.6 KB (750630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8fe3f657c52ab0bf96d463d9dd98b907a9184e001ab2f9e794055bcb3673ae`  
		Last Modified: Tue, 29 Apr 2025 16:52:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea15669d07262c6d4ba07971d97b5f0ad0492a9bc7990b48bc465cd3e8f028`  
		Last Modified: Tue, 29 Apr 2025 16:55:50 GMT  
		Size: 21.5 MB (21491437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:790a29d1d05a26bb6658e6edd485340462b2c0b6a81186c3249111dbc56ec486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6878181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d458e7b4cd7f62440371553b48515feb86a393c43fb8542233ce2de6453885e1`

```dockerfile
```

-	Layers:
	-	`sha256:561c9136d73c74dec8387b8e5f73cacb14ea3863aaadbf48159f0c8f9e727674`  
		Last Modified: Tue, 29 Apr 2025 16:55:49 GMT  
		Size: 6.8 MB (6840701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5988be8600ba84610708fda3f1f2a81dfea7bf3af21197b9cfac1d397bc9611a`  
		Last Modified: Tue, 29 Apr 2025 16:55:49 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:64c0e6e933aeca73b18e41ed091d1545f700959c1df6ae52c2735aa5763d600d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183438674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adb4b16dd46bfe9bf9c48defc9ba5d8d2baf42b6ef456503bfe8a6d56c445d4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 03:27:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 03:27:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_VERSION=8.3.20
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 03:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 03:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 03:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 03:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV DRUPAL_VERSION=10.4.6
# Thu, 03 Apr 2025 03:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /opt/drupal
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e399040856549dc4a226a08faad5fb428e9430859d56acfe05462ca8444750a`  
		Last Modified: Mon, 28 Apr 2025 22:56:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72cf290eaa9cbf7926f0fecd941a3049b3b2eb55cee9a84dc7759b3868b4647`  
		Last Modified: Mon, 28 Apr 2025 22:57:02 GMT  
		Size: 86.9 MB (86940643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8132c544db419467815cf232bcf11c55005c5a76d14b74d0946ee2deb8fc75`  
		Last Modified: Mon, 28 Apr 2025 22:56:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca1004dd432d3dbd60abcd6df67845b15e9bf0bc2d8e0d1907b9b3554e82b1`  
		Last Modified: Mon, 28 Apr 2025 23:00:16 GMT  
		Size: 19.0 MB (18981565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e811ae31142dcfab211a404ff5f6c819ca24ff49c9a5aabdf2041df0ff3b818`  
		Last Modified: Mon, 28 Apr 2025 23:00:15 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c264e600aa01419ef570f8653e9bad74c4f0d98e3dd60ecca46e9492d54b0092`  
		Last Modified: Mon, 28 Apr 2025 23:00:15 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93adc86cb9e20f27aa23ee4e31db768adf8d13fea3cc7bf4af783e6e93d80c`  
		Last Modified: Tue, 29 Apr 2025 00:17:42 GMT  
		Size: 12.7 MB (12673242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494cf2751ae270baf7976c05258222d96ff496ae5aeb2c2add260eb024bb0086`  
		Last Modified: Tue, 29 Apr 2025 00:17:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c4bce7e8094471bf354de046989c56f65a07c5c8da6407d7826df96aee7851`  
		Last Modified: Tue, 29 Apr 2025 00:17:42 GMT  
		Size: 11.7 MB (11656865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4286a0e3a53109393f678250209c43376111bf4226f665e1846ef3048ad4f576`  
		Last Modified: Tue, 29 Apr 2025 00:17:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c90c91855a2e9364f1969a213fc5195465c607d2c2fdd7cc94b34fbf68583b`  
		Last Modified: Tue, 29 Apr 2025 00:17:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf6f9d0c2c49c7cb00f8347dd49345ef6cdffd55f0162a488d2f7e90f577a5`  
		Last Modified: Tue, 29 Apr 2025 00:17:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2335d0e2bd527d43e55842adaf7609a2c117716ec3177c02dea2873c3aec61d`  
		Last Modified: Tue, 29 Apr 2025 18:48:13 GMT  
		Size: 2.2 MB (2196599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5727bc96f318bf6a34206b7c28cb03e28814ea30e030beb4acded0483e8cdd`  
		Last Modified: Tue, 29 Apr 2025 18:48:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f00faeeff4ed3e3a1f12374f46d12e4e6b138306f16941739aba11fea07265`  
		Last Modified: Tue, 29 Apr 2025 18:48:13 GMT  
		Size: 750.6 KB (750626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d447fde2bb80e2c92986db780a2e6ac8d7e8d9b1f553c5743a7eae3b908fade`  
		Last Modified: Tue, 29 Apr 2025 18:48:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5bb95a4db334bb3776af3bcca9daaf0d3f17d5e3c58e8c1d9903c8534bde3b`  
		Last Modified: Tue, 29 Apr 2025 18:53:16 GMT  
		Size: 21.5 MB (21488592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:8cbeed19c6f9837e7d6cca4ef0d2a5609f0ef9329455f07342f368d973b5ec72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7072133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f2554cd0acff84573ada082df25fa4fb43a51308104ea9b47bb87e93cbd517`

```dockerfile
```

-	Layers:
	-	`sha256:03539373487866f7bc2842e9f5b9e5d451be45389a08113c9b28ba85bf583714`  
		Last Modified: Tue, 29 Apr 2025 18:53:15 GMT  
		Size: 7.0 MB (7034609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92de0802c4f0c25f73ecaa4671fc1394114eacc99960af387355bb929ceee9d`  
		Last Modified: Tue, 29 Apr 2025 18:53:15 GMT  
		Size: 37.5 KB (37524 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:25a8249ec9f6f6e52b3e480bf6ceddbbe0a8a39aafa65e55c9f231b0a97946d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192199294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971c7d575868357ab25be4cf638b433b7fa5fd0c0bb62fd0cceced4ff344cee4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 03:27:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 03:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 03:27:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_VERSION=8.3.20
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 03:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 03:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 03:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 03:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV DRUPAL_VERSION=10.4.6
# Thu, 03 Apr 2025 03:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Apr 2025 03:27:18 GMT
WORKDIR /opt/drupal
# Thu, 03 Apr 2025 03:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Apr 2025 03:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2a746239e56cd7f3164c987d8909541030a2105f8f3f811b1a998e5ba44c8`  
		Last Modified: Mon, 28 Apr 2025 21:49:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f996d828c2d3e571130a80949a0f2d7cfbd0ab6513ea351c23e73573a9f677`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 92.7 MB (92724658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50489c2cd9bf824bd554a3e54189c97ecab1d8ba694967ed7d1fdc100690ee3c`  
		Last Modified: Mon, 28 Apr 2025 21:49:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78507ce083c5d6f8d5e56948c93c826e325868af6acd4efd8b7f992fe5f9e200`  
		Last Modified: Mon, 28 Apr 2025 21:49:27 GMT  
		Size: 19.6 MB (19552789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a726299e13ca38053bef2d20bf158165ca11b35c77136c84cab575f07df3989`  
		Last Modified: Mon, 28 Apr 2025 21:49:27 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da4d3d3b7278642e33277fea74e1a02de38b78166ede30bcca8c7aadf43ccb`  
		Last Modified: Mon, 28 Apr 2025 21:49:27 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6201822dbf5b33819842a49fc7c19761cf367dffb6459ae3cd3980a8117c7c09`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 12.7 MB (12673188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0355acdac765b55ae6756a19e12aabfdd2f7c236ff1abb91b3e8de4ff6de0b77`  
		Last Modified: Mon, 28 Apr 2025 21:49:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb5921b837547d60d315e604a3ba4dbfd7d7bbe4608d687e0f3c917a59eb19a`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 11.8 MB (11813759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a044c7716389a9041fdca472bec1d0c45841480c841c6f1d32f57e7d100aff`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8707b3d07624a30755109d49a28293cc1aa7261648d0fc8383947485c1ab4551`  
		Last Modified: Mon, 28 Apr 2025 21:49:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b54eabc01294e54efa74497b1c5073b49331b0397d8c2f8b426836cdb7a0`  
		Last Modified: Mon, 28 Apr 2025 21:49:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07ddf6b17f9a25fc47906425fb4851071bf543e4bc307765a4073abc545e329`  
		Last Modified: Mon, 28 Apr 2025 22:17:04 GMT  
		Size: 2.0 MB (1998440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aae755643a058dcfd18434041e7ea23b5c5cb3a0e3fce80cd5cf012986f7c6`  
		Last Modified: Mon, 28 Apr 2025 22:17:03 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395810c6f59682bcd877a3233268d117e27b6a6c20e3afecc775bd584e7aa8a`  
		Last Modified: Mon, 28 Apr 2025 22:17:03 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5610875f947dad574294b9da69c28fa22e14ae26e7264612e741e7a8254bd5d`  
		Last Modified: Mon, 28 Apr 2025 22:17:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92e8a25b24b6797e867d54c8b1d3e0e616bb24726d745cf7be06ca93f9f3d8`  
		Last Modified: Mon, 28 Apr 2025 22:17:05 GMT  
		Size: 21.5 MB (21492033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5b4516fbffba2c88ca322abfc771efe404bb1b9b6bf4f224293afb8ae39a73e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7059668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b4f0e459488d560df6b5711e8a34da6a30009009c0ae47f6fd299a4afc5863`

```dockerfile
```

-	Layers:
	-	`sha256:5155f3e63c0f80d32f1fee4985e99aecc72b800f18a4b7daa999740f5a43759d`  
		Last Modified: Mon, 28 Apr 2025 22:17:04 GMT  
		Size: 7.0 MB (7022381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837e1d9e3cc7039e18fc2d593fc643cc93b7e2b86c7f9a4e616c17fea154105a`  
		Last Modified: Mon, 28 Apr 2025 22:17:03 GMT  
		Size: 37.3 KB (37287 bytes)  
		MIME: application/vnd.in-toto+json
