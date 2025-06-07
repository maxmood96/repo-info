## `drupal:10-apache-bullseye`

```console
$ docker pull drupal@sha256:eaf829bab7d4516562d42ba8cf53d0a438140c9ad8cadddffcf164f414268804
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
$ docker pull drupal@sha256:05cbb0b87897e6f1133c0650a7fda716fc0aa3395280624b55b76d6d6ebe4aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196072237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81097d612c36c52315f2742d5f0ccbe62052f9f1a89410674bcb6c9381584166`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 21:43:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_VERSION=8.3.22
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 21:43:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 21:43:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 21:43:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 21:43:31 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV DRUPAL_VERSION=10.4.8
# Fri, 06 Jun 2025 03:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:27:20 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d84a0a5d5fda4bf5735970c44024a919d4c735be50c6ec427b3ad377ca3e96`  
		Last Modified: Fri, 06 Jun 2025 17:39:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ad0c41aa37c0517a1d0b74743865dc7fba94898534e660fc3031b70559d86f`  
		Last Modified: Fri, 06 Jun 2025 17:39:16 GMT  
		Size: 96.6 MB (96588412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b508022e8291a36f72a345f4e7897678f4b2a67d8dc099fc86eaf8aeebf340`  
		Last Modified: Fri, 06 Jun 2025 17:39:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5aecf1691648da48bb4d375a614246da1c9688415452ba2caa17033d1d4e4`  
		Last Modified: Fri, 06 Jun 2025 17:39:13 GMT  
		Size: 19.1 MB (19064046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e955596655eb4b61b4afed03c343bd862c49029e52f7440fd9df3366f4904e85`  
		Last Modified: Fri, 06 Jun 2025 17:39:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47a6698b1f3bb44fc79bc50323d8d52a2ed07d7afb4b53cfc01c9aa42aff34d`  
		Last Modified: Fri, 06 Jun 2025 17:39:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34da4b7d3a07791a1ef8a12702bb846ed82b11ea8bfea97bf60a8ba2568b1a`  
		Last Modified: Fri, 06 Jun 2025 17:39:13 GMT  
		Size: 12.7 MB (12680161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43082ec10cc4c65a33a1380c4754d2ac08613092b2ca2bcdb8d00be9b4d3e89f`  
		Last Modified: Fri, 06 Jun 2025 17:39:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946804ee7360aaf7f618e936f992c8dfa13b74ed07c06cea493b5fe6ea151cea`  
		Last Modified: Fri, 06 Jun 2025 17:39:14 GMT  
		Size: 13.3 MB (13301601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005140603df4e9922f0287c898dd82ea632070c061a35131e7d59f9cdc334d43`  
		Last Modified: Fri, 06 Jun 2025 17:39:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d33cd03a0d5bb0dc5dbf96e821e4505a07493bf42400f1292f75a295a0eead`  
		Last Modified: Fri, 06 Jun 2025 17:39:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6decfd815da7887d0d38fb92325be10e961a9a0367cc9c227015a29690d93596`  
		Last Modified: Fri, 06 Jun 2025 17:39:14 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418792aa4ece6c274605fb27605abe19a172606848f6507fb6cdb3fd0472ef7`  
		Last Modified: Fri, 06 Jun 2025 18:20:42 GMT  
		Size: 1.9 MB (1934130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c960e884ef05fc77699e160bf6f691e5b4ae928a2337dcf0e1f44238b29506f4`  
		Last Modified: Fri, 06 Jun 2025 18:20:51 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3f050c3a13e50be0b865737d3a66e487ee98a4b1e82888c2d91c9ed1c3eb00`  
		Last Modified: Fri, 06 Jun 2025 18:20:55 GMT  
		Size: 752.8 KB (752772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80972783d5af29bdd8858716539c28586d91766a73451776b413aff7869e38b`  
		Last Modified: Fri, 06 Jun 2025 18:20:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62140752415e65714ed439ba47e7c3c38a120da2f9915eb288b4061e465f08d6`  
		Last Modified: Fri, 06 Jun 2025 23:45:19 GMT  
		Size: 21.5 MB (21489278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a88b273405c0af23b4fc2043902b1ae45d197792807e0f6eb097ee7677622e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7110070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b0a0517b8c990fd932c0e866f2cfbf966ab8d7edb531cffbbc0b0f67703120`

```dockerfile
```

-	Layers:
	-	`sha256:7be4f77f5daba06938eb669ac2c8ed5fc758518952d3dd05dba0d3e4a60bfaef`  
		Last Modified: Fri, 06 Jun 2025 22:54:09 GMT  
		Size: 7.1 MB (7072730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f628c05a31d9dea5451c508c5c768ef1506b3b2ac739646fb9da13f008147be`  
		Last Modified: Fri, 06 Jun 2025 22:54:10 GMT  
		Size: 37.3 KB (37340 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:51145c9342821d73bb56566d09fcc8fff3d90130756254bdc6ea8d4d04594642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160277290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ded4c876d901b1cae2f6525f30ab3e59535f0134b6cc8fd5db797e010ef2fb1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 21:43:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_VERSION=8.3.22
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 21:43:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 21:43:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 21:43:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 21:43:31 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV DRUPAL_VERSION=10.4.8
# Fri, 06 Jun 2025 03:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:27:20 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d9c98f5407c517a6c82e3d633185a6d76d2f1a1b173f8c84e8d09194a0047`  
		Last Modified: Fri, 06 Jun 2025 18:08:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174dd4c330a5cb2b275c9367f976035c4e9a7870c5bd8dfa239ede951528cdd9`  
		Last Modified: Thu, 22 May 2025 00:23:53 GMT  
		Size: 69.3 MB (69326451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b71238feba8c542154b4c87407bfbfba4330ed0b0c64c3f18e02484c87476`  
		Last Modified: Fri, 06 Jun 2025 18:08:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b2866468df76c8f23b86c6f9ea4b2b38f94eb9343d0d7f352d4382d36bd757`  
		Last Modified: Thu, 22 May 2025 00:23:51 GMT  
		Size: 17.8 MB (17817550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d273e51f04d91ef2cd8e161ebf289529ebde809b416532c18fc9b20d76b96784`  
		Last Modified: Fri, 06 Jun 2025 20:50:01 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d81b85a4c7605624890a6f4d58d2353c920c335651987605b5cf718d5ab013`  
		Last Modified: Fri, 06 Jun 2025 20:50:05 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eb1bf9b6b70b4996ae568e496d45e981c77d42ffbb40ac5434271fb2692f9e`  
		Last Modified: Fri, 06 Jun 2025 19:00:46 GMT  
		Size: 12.7 MB (12678792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304d4a8b86faede292eb9a0df49b23a021a6e4ac445554c8cc249b69967fd24`  
		Last Modified: Fri, 06 Jun 2025 19:00:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5743bd0931632a680073b154158ea47301d5409a5bdc71b215c94283f7c41c9`  
		Last Modified: Fri, 06 Jun 2025 19:00:37 GMT  
		Size: 11.3 MB (11349983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a36e86bb871d4435c360dc69ec73eef793ec0b2eb4c42a27a01383fc9aed2`  
		Last Modified: Fri, 06 Jun 2025 19:00:34 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6f3e6e193998eaa250e31851674824fb52f922e67c90e7b2ece6c6c0077fe0`  
		Last Modified: Fri, 06 Jun 2025 19:00:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836692bf3020230d97dd11306663d90d56a6c918577f24ace24df47e4f5f931`  
		Last Modified: Fri, 06 Jun 2025 19:00:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e278e1abbbac59fa728928baef4e099770d75af3dbe9297a9a1d86af2c67a408`  
		Last Modified: Fri, 06 Jun 2025 20:50:25 GMT  
		Size: 1.3 MB (1312638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceecaf611f826dc2a85d34528c57255b43c141aeabadbc5e7294fbbef2883a`  
		Last Modified: Fri, 06 Jun 2025 20:50:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbd245fba1a79de2f8e2f0203f76663896e97a7dca420bd0b01c7db493db117`  
		Last Modified: Fri, 06 Jun 2025 20:50:39 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbdc0fc3c1f513f28ada84b9b29e5685c0c698da8047c81af006468ee541c8a`  
		Last Modified: Fri, 06 Jun 2025 20:50:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f5d5ffe199dd83ef6e97442c9c094c853c8f03986b746113119410c3c6e9bb`  
		Last Modified: Fri, 06 Jun 2025 21:14:46 GMT  
		Size: 21.5 MB (21489295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:3a52997aab8490c824bfaa639729b1b3d39c66a6a683d8fc9ca617bc79758867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6918317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42dc08bc607d51d6aaf4a30393d4a6d5452f4c2a0fc6628fb244f63f2428e26`

```dockerfile
```

-	Layers:
	-	`sha256:461c7571d1bfe8534df30eb6f49a509857a1844de445abf5a833d935e7078411`  
		Last Modified: Fri, 06 Jun 2025 22:54:16 GMT  
		Size: 6.9 MB (6880837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3cd63c4213d12eb42e1d512afb804aeaf8b5c91daba7c449e7b719066bc6328`  
		Last Modified: Fri, 06 Jun 2025 22:54:16 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:adb7e079379c190b19bdca1b7f199bcca3670131d4f0595f4003fa3e02dc45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189165986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed7d379866fb3b7817c8e265f8f5a47432cc09ba857ac465f4df01b91875544`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 21:43:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_VERSION=8.3.22
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 21:43:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 21:43:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 21:43:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 21:43:31 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV DRUPAL_VERSION=10.4.8
# Fri, 06 Jun 2025 03:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:27:20 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8172ab386f3db13cd04f5ecb5a0ba3663a0da50f1f5f0f595a69b8407b39bd73`  
		Last Modified: Fri, 06 Jun 2025 17:57:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58f900c2f78730779b376264aab0a750a2b59069fedc8057d2bd990c5bd534b`  
		Last Modified: Fri, 06 Jun 2025 17:57:38 GMT  
		Size: 91.1 MB (91096803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eae96444bf9d20f4dfcb4f600754dc44a40935ef5c9bcfbb19f7e4d3e9241f3`  
		Last Modified: Fri, 06 Jun 2025 17:57:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c33ae52242bcfe0579c357f4a60c82043aca3008332f4d7427e07a52267206`  
		Last Modified: Fri, 06 Jun 2025 18:00:37 GMT  
		Size: 19.0 MB (18981738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f87cbc9a1d9252b24d3d7da6d375f912d058439e6aaa1779c1f49c679dfb2d2`  
		Last Modified: Fri, 06 Jun 2025 18:00:37 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d448e17840e5dd362808de65c14a7e839d2477e2aae43ee1ec46755fd1760e3e`  
		Last Modified: Fri, 06 Jun 2025 18:00:37 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ee1af995bdcd86bbc0d14aedef74aacfed1324fbb92d9c14e0cc5038979d9`  
		Last Modified: Fri, 06 Jun 2025 18:53:07 GMT  
		Size: 12.7 MB (12679622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abeb0da078c011b4d219f4163a87184cc9bb2a606bb4dcbde6e096c5f5c5a63`  
		Last Modified: Fri, 06 Jun 2025 18:53:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f120727e24500a28136503721a0e804dac0f3afbf884686f160676cee112c`  
		Last Modified: Fri, 06 Jun 2025 18:53:09 GMT  
		Size: 13.2 MB (13215971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b655068bab63baada872b2fd2372fb6ad6caf7e04630cb342f7cc5e1d694f`  
		Last Modified: Fri, 06 Jun 2025 18:53:07 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd58f1ff1ab8b7dff950bd285fab1ddd9931eb0b5597cbd4a891306ce47f0c0`  
		Last Modified: Fri, 06 Jun 2025 18:53:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a223487bf1f72b5ebd0368697940d262a54524227c37a8944bde55d3ef40a6`  
		Last Modified: Fri, 06 Jun 2025 18:53:09 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10d22b3f56b0d0e8572ccdae14ab965a182614c48960d86c9440b54ee6dca88`  
		Last Modified: Fri, 06 Jun 2025 21:19:32 GMT  
		Size: 2.2 MB (2197622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efc568a304f532ae3ea584ebb9a58d75ddf4d9f632878200baf10bcee3c3026`  
		Last Modified: Fri, 06 Jun 2025 21:19:31 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750e35e5de10aac7f8f19208e40ab5b993ffe15a78736ec934e8cd6ac3225ff`  
		Last Modified: Fri, 06 Jun 2025 21:19:39 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec38cedd1c941414660065fe0efd53270763cba70ae5e5c29bc532741f9eb0d5`  
		Last Modified: Fri, 06 Jun 2025 21:19:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b8763c5398d0c6c93e6dff96b0cf69a13ed7d67e8b0d63d2b235ba4bb7a94`  
		Last Modified: Fri, 06 Jun 2025 21:47:10 GMT  
		Size: 21.5 MB (21489299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:688f136cc8f22982621315fcb5cb0c78d52016dce6b18357cd7c1fa1fc0964be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7112784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c10772488c74683f094d729c99fc692fcb8e0931b22ba19dbcb1378ede0c9`

```dockerfile
```

-	Layers:
	-	`sha256:c222c90e84fbf9e77e709cf93bcc3194c091c21fe5e89089e4c51089f0c03744`  
		Last Modified: Fri, 06 Jun 2025 22:54:23 GMT  
		Size: 7.1 MB (7075260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe517e76440f1957886decee7d3721d531239d5ba6d51f9b89ee8dd07507cc2e`  
		Last Modified: Fri, 06 Jun 2025 22:54:23 GMT  
		Size: 37.5 KB (37524 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:565072ad08fdeb1a5c03753ba1bd86d80b8ea1cc7d20d08d75e67f81df7c6a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198416543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6acb724d0c11492ebd1e38e7b344301e673f979fc90d46ae33c7092aa597af`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 21:43:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 21:43:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_VERSION=8.3.22
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Thu, 05 Jun 2025 21:43:31 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 21:43:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 21:43:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 21:43:31 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 21:43:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 21:43:31 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV DRUPAL_VERSION=10.4.8
# Fri, 06 Jun 2025 03:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:27:20 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a819772a78c8b8001f4fcf9cc7d6639f373e61bff0fc434bc295ca0566eca292`  
		Last Modified: Fri, 06 Jun 2025 18:09:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeb8d0f836d9b7402777d716a3fc6c23b30dc5e9eea06774c577bcb56a4b701`  
		Last Modified: Fri, 06 Jun 2025 17:39:42 GMT  
		Size: 97.2 MB (97242660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38c981154410e6f6585ff949e88ea70d76916d8fb50e0ddb2baa0639c11b576`  
		Last Modified: Fri, 06 Jun 2025 17:39:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3ace7cfc53fb29a122a4fbed9ec35657c711ec9d06823238f7de268aff435`  
		Last Modified: Fri, 06 Jun 2025 17:39:39 GMT  
		Size: 19.6 MB (19552961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4637a262d6d9ac81e7d7c4e9856369aeefec6bc7fb4d74e130d66c9eb87b974c`  
		Last Modified: Fri, 06 Jun 2025 17:39:37 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0f10d187971b0e88708721edc92e91142c14d9a7338ff0f036ab25ee430fa`  
		Last Modified: Fri, 06 Jun 2025 17:39:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2742f152703d4c2629414b78bd073b56cd26760862faa1a7a75575421ee44c09`  
		Last Modified: Fri, 06 Jun 2025 17:39:39 GMT  
		Size: 12.7 MB (12679639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac8097733dc2bde107fc1e3d5e575c7c85d34a728f44cf8cfaa0657981fb9fd`  
		Last Modified: Fri, 06 Jun 2025 17:39:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e703c1f5ec4880544fb6c1ab5a0fc48bf11a356bd5ea1068dd89dba7f114bb`  
		Last Modified: Fri, 06 Jun 2025 17:39:40 GMT  
		Size: 13.5 MB (13505552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d05b0d87a051fa4a4ba3a243a3ce25f61ba19e1044c04c9745fb1ab821b0b`  
		Last Modified: Fri, 06 Jun 2025 17:39:39 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e4a348ced684cd7c7df13f0bf8884d24c485073b3b397c2a22aee9a839e9bf`  
		Last Modified: Fri, 06 Jun 2025 17:39:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397d5ecdc21e99ca5c87a40e0e3715b1cce2b97fe6ef53a0f7965ad001148993`  
		Last Modified: Fri, 06 Jun 2025 17:39:40 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b08d86fda935d3b87f01dec1870ed4640285c2d645b2f9c06aababb7354e97`  
		Last Modified: Fri, 06 Jun 2025 18:13:34 GMT  
		Size: 2.0 MB (1999181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b373a4b4d3d30cdebf3bedaeb913c4cdb72dfdb7832d7e18ee4e53a17bb315`  
		Last Modified: Fri, 06 Jun 2025 18:13:32 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d66d36d4b59f13def390c597691bd7163c329acc822f81b0e34ac1bc51838`  
		Last Modified: Fri, 06 Jun 2025 18:13:35 GMT  
		Size: 752.8 KB (752769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae50465de4eb1f65430f7be9bdfecf7ca3402683dcfc5806861e29a25c39105d`  
		Last Modified: Fri, 06 Jun 2025 18:13:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4418d461b14be2985a37a2f404e1b39807090f75ec7c96aa67dd142b7d791ce2`  
		Last Modified: Fri, 06 Jun 2025 18:13:38 GMT  
		Size: 21.5 MB (21488682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:46bb6786a0b90f689d5215678b7f7dd04973c798b5a1a889ccfe8ad0c8352bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7100131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e74f4967ff679c0ccad7d63e44ca173c7de185037f49cd14770f56fe08ce915`

```dockerfile
```

-	Layers:
	-	`sha256:1fd85e57c5cad6198c02f5bf72dfab25f9f7163aa44733da6beca988121ea586`  
		Last Modified: Fri, 06 Jun 2025 22:54:34 GMT  
		Size: 7.1 MB (7062845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21982b0094c0712ac93a51f3867c293cd380d4dbd62e9509e62e4fad79a13d84`  
		Last Modified: Fri, 06 Jun 2025 22:54:35 GMT  
		Size: 37.3 KB (37286 bytes)  
		MIME: application/vnd.in-toto+json
