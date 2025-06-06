## `yourls:latest`

```console
$ docker pull yourls@sha256:891f80518117af2d8247b8cdcfdac9831cb517ef74233194fdea5a8ce26670df
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
$ docker pull yourls@sha256:5684fd2ca9df1a380b425755b3bfe62da75ad2fca11c7998d04fe1c41deaadec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187034333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a41f14979806491bf94e32607dc9379512b4becdbf72074b0b8e4810d7013`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d425376ca8328988e808d5c5a27bcd419b7deb0508a184e290239842133fac3`  
		Last Modified: Fri, 06 Jun 2025 17:42:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cec26ae36a389e3ff754c2b3736bd03ce3861e6f42da792a20afae2922254`  
		Last Modified: Fri, 06 Jun 2025 17:41:26 GMT  
		Size: 104.3 MB (104326190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcad424788d140b0d0921545bd2dee8e6136d3540d8f706c154b7783cf91005`  
		Last Modified: Fri, 06 Jun 2025 17:41:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428e8ffbbbf7f6632f181c633a52ffeca7f024bc2f1bab2e39e642d89020b47`  
		Last Modified: Fri, 06 Jun 2025 17:41:19 GMT  
		Size: 20.1 MB (20123889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd16d8ffc1fd319af695d946fa2f8e4a2e4833c5f2ea98702cdab0a1240d2bc7`  
		Last Modified: Fri, 06 Jun 2025 17:41:18 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f451c322a91b6b848adc2f7f36743d17a60fe273d2364d359eef6db36cfa1e7`  
		Last Modified: Fri, 06 Jun 2025 17:41:19 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e5f488bcb741a3d58d0f6bfa9bceb4d222ecfeddae3895dc9e200eb5c7c2c8`  
		Last Modified: Fri, 06 Jun 2025 17:41:31 GMT  
		Size: 13.7 MB (13748135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83499d28f06eac30145d90d5e54b089c4855c4bb10482a2b3a60c9fc2396f6`  
		Last Modified: Fri, 06 Jun 2025 17:41:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098d35f9bca9da7487f329b42be85c403062c19e51fc673a1ab93be8b06e252b`  
		Last Modified: Fri, 06 Jun 2025 17:41:31 GMT  
		Size: 14.2 MB (14169618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dd5519f02f8ed1a6b74943c234cc422b4d9d585982a3ba50d6660c0d8362e7`  
		Last Modified: Fri, 06 Jun 2025 17:41:20 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e952f595dc56ba86a16691bd7d2fee72e0c96ddcc6b1c4a070b7353a63c3de`  
		Last Modified: Fri, 06 Jun 2025 17:41:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606492437a38a207c198ec1ef89795f315ddb91a276e1bfd9ff24774bb32d999`  
		Last Modified: Fri, 06 Jun 2025 17:41:14 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668fc19d6171070f2fcbcb13f6985ccab80becc0c4d66d9d276e37347181f08e`  
		Last Modified: Fri, 06 Jun 2025 19:08:54 GMT  
		Size: 663.3 KB (663318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7d3faf8eb5899442e52eef61c14ad3b17bf43262c9e822ae84961369ebb074`  
		Last Modified: Fri, 06 Jun 2025 19:09:00 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07aac9ea2d19f9b256e8e00790e105eea4c87642870de7a0c385bcca467c1b`  
		Last Modified: Fri, 06 Jun 2025 19:09:02 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f37e6a38c1a6cae37c771b72a5db64768024f450e87628ad47b8da3dbe9d8b3`  
		Last Modified: Fri, 06 Jun 2025 19:43:46 GMT  
		Size: 5.8 MB (5767594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4335244fba836d3763a6ac04518cd45422fe0d1d23fd39a25ace1e97321536`  
		Last Modified: Fri, 06 Jun 2025 19:09:13 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245dc77f82c05ea8756e7c8152982ef0e468899edb30bd151f0e8c750501118`  
		Last Modified: Fri, 06 Jun 2025 19:09:16 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31643290820138031c83531a878cc849f139a6071a7bb48061e32b218426bd4c`  
		Last Modified: Fri, 06 Jun 2025 19:09:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:eedc69d7b17c8fae4ac074cbdd1bfd6e12433993c574d275a6ecd0bdbc77a251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (39009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7f73812ae9ef1f20f22d8dd46a93313c09e29955733e71d0cd9c0316dacdd2`

```dockerfile
```

-	Layers:
	-	`sha256:30dc8578408432569f07adc42f921fd5a165e94a979f5d29ee4950a464107174`  
		Last Modified: Fri, 06 Jun 2025 19:42:38 GMT  
		Size: 39.0 KB (39009 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:712c6f7aa2366163d428f4b811fdbaa54d084f600d8209431ce412bdac57b41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159763064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182796c1c78fc53ca6112676b6fa2ac6e1692ab53d8bce7dea7f96b2d3c736a8`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630a0ae6a7caa13c26c641757aedb6f2a685e945563086d454f01db874d5a4e`  
		Last Modified: Tue, 03 Jun 2025 14:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c1543f1d03f96cc1c05ba7756b5950bbb8edfd3038bc0902f7bd06c8b3a5a6`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 82.0 MB (81970289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1f2e7aca197ce584722af1cb59310256391ea143b4eee91fe64249d0f64ac8`  
		Last Modified: Tue, 03 Jun 2025 14:06:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58b58ecad378e2c244a47b087001bd8dd7a6bb20346f6a44056db42ab3a5ce`  
		Last Modified: Tue, 03 Jun 2025 14:07:07 GMT  
		Size: 19.4 MB (19419290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f2b7224a1481ccb5f31a4a4189cf4eba4409cd5baaf7402ee9bf4a6ba1d7c`  
		Last Modified: Tue, 03 Jun 2025 14:06:58 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e190f82563d835d64144f74a1701508a80fd49ac413b53cda42a431d89cf4b`  
		Last Modified: Tue, 03 Jun 2025 14:06:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18166f9f79e0a6d5c0b39387dff021f316e48f86f71ef3612b009e7ccce249a`  
		Last Modified: Fri, 06 Jun 2025 17:46:58 GMT  
		Size: 13.7 MB (13746040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861154f25c79cb76879290e93bbd87d4100753ccfa5bfe4c180cef085dcf6899`  
		Last Modified: Fri, 06 Jun 2025 17:46:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17ee7706ec9ba5d62d8e7d017e853f779ad86443bc00550a9af1d62a5211d98`  
		Last Modified: Fri, 06 Jun 2025 17:47:10 GMT  
		Size: 12.9 MB (12919205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e0aa899da40b39745c3ab000e876e97ad91b6052062b7bdb0bf5ea0c99c396`  
		Last Modified: Fri, 06 Jun 2025 17:47:00 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac4b78f7cb249760f79283d1e1c5d4e31fadf2ae53c1689cc1ee07704b7dbf`  
		Last Modified: Fri, 06 Jun 2025 17:47:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a3f0f4db7704f7256c2af4749d95b9731764699970e19b9853bf746da2003f`  
		Last Modified: Fri, 06 Jun 2025 17:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1829c081b3e4653c07a8ad95db07a9c16d28508e9f02e1029ad9081c4eda2c`  
		Last Modified: Fri, 06 Jun 2025 18:26:28 GMT  
		Size: 173.5 KB (173475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3b9eb91eef688c4f602028bb4e21b56f2e097a3af36f4544e950d528b0dd38`  
		Last Modified: Fri, 06 Jun 2025 18:26:28 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902e7d8550fe27cc1affa504ed55ba71553e28acff740fa5f1cd1f05ab3c7845`  
		Last Modified: Fri, 06 Jun 2025 18:26:28 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb92e6704420b6f40404f2202749b5e39cc2e3d4962146c02ad13bf818f7126`  
		Last Modified: Fri, 06 Jun 2025 18:26:30 GMT  
		Size: 5.8 MB (5767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24827339d169e1c1e7e6c952851da0f5bd5fcfe69168400c07bd3f48cecf0fbb`  
		Last Modified: Fri, 06 Jun 2025 18:26:29 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28c76d4a2f9bda068051b391d588548bd9fc2c193311da3e1770da7bc3a2e4`  
		Last Modified: Fri, 06 Jun 2025 18:26:30 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0422031bffa547841d972e30e49b9c52f0749461a47e01244b87a532446d489`  
		Last Modified: Fri, 06 Jun 2025 18:26:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:00f8182eb1c390d2eee4b547ef88d551afaebb8fe55f39cfd0106f1584da7fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c73972a8a02b30b9bb5e10ec15d0bd780765601555ec1b27263f37c8260189`

```dockerfile
```

-	Layers:
	-	`sha256:50a393ad7af3fbf7668919a89bc67b128e51d04acdd853669002da4deeaaff12`  
		Last Modified: Fri, 06 Jun 2025 19:42:41 GMT  
		Size: 39.1 KB (39148 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:92e7c1a6759bc878b937c6932a81bdf7a750188bb27a9f1a09909a81e268eeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150884141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b39906701e179db51d3f51165c4520a66d2ee570b5e7c38af2bd1470179551`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b0d6d3f419936777d490c71b48fd196b853be826a3cbe2a99f87ce45962a8`  
		Last Modified: Tue, 03 Jun 2025 13:33:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b3dbe5e2b037219e6a37b411897a539f579592c7d55f751f30cdcfee2dafdd`  
		Last Modified: Tue, 03 Jun 2025 13:33:29 GMT  
		Size: 76.1 MB (76132659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56653e4c243acfc3e7a605794bbf2267c510182bd9d2f39f4bcf6a23263375bd`  
		Last Modified: Tue, 03 Jun 2025 13:33:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685993b77f7d52922724cc7923b4ae3c3fca80c6d95d24466f21896fd02e39e6`  
		Last Modified: Tue, 03 Jun 2025 13:35:35 GMT  
		Size: 18.9 MB (18857575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa27ed9872b7024c07a4a56aa9a0f051809faa8364467d10f7af87990268507`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eac574232d2b47fe0f2924dbc13495d266c0790fe259b37113ec8f3ff7451d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0720ca91de9b15e1be6762f8af3d3de494b584482451179fb3ce69d75ce0fc`  
		Last Modified: Tue, 03 Jun 2025 16:41:36 GMT  
		Size: 13.7 MB (13744235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dfa2db170411cd0c41c50da7346cf8dd4281dcf0acaef17888d0701ae3bf54`  
		Last Modified: Tue, 03 Jun 2025 16:41:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493d47788762fb8564d78d9ae148fae3c5f6a796432b529127ab981947062a6`  
		Last Modified: Tue, 03 Jun 2025 16:41:35 GMT  
		Size: 12.3 MB (12279897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1eadbfbde45e922fd93e9f34e8bcb3de73d3de65005731bb2ef0d7a843d56f`  
		Last Modified: Tue, 03 Jun 2025 16:41:33 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f2c560f938e1c8970f7c99e2bb3c10b9d8f2e68e2aeface997cb36f2b32658`  
		Last Modified: Tue, 03 Jun 2025 16:41:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52594136cf5978f6a40231e23af290dcb1a3a5bb7f5f34804a119c23866a6aa0`  
		Last Modified: Tue, 03 Jun 2025 16:41:32 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32adbca28c0dbbf1967a79145e9895a0f1dc6635c03d0a30f0555f41ec7d578`  
		Last Modified: Thu, 22 May 2025 12:09:54 GMT  
		Size: 159.0 KB (159010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360b48301a447de37f00eab6eb5f38e5d6180d3096fc884d3db532d9fa925ca2`  
		Last Modified: Thu, 22 May 2025 12:09:54 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699fd5c2b66df251692f10632697b2abdf7b8f897552105310a709b61de022b8`  
		Last Modified: Thu, 22 May 2025 12:09:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce53d730812baf8f82fcb42bfb7e1f2f1cb3eb678ee7e5d4170e0e3fd1bdb218`  
		Last Modified: Thu, 22 May 2025 12:09:54 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6bd15dc12199122dc17b482a113557253a670905f05de5a51669ea7b54a182`  
		Last Modified: Thu, 22 May 2025 12:09:54 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4958da8ebd0ab76a86c443c2fcd5b2f41c58e94f1f19e2874c891197fbb7b47`  
		Last Modified: Thu, 22 May 2025 12:09:55 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5908bf4cfba5e503ba02501b7eefff3b337cadc3c5f14e019928d5b49c00137`  
		Last Modified: Thu, 22 May 2025 12:09:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:07e82ca5b7a71c0e41ff87cc65b3ecca6a3ea6ce5ea03a33bcdb4318283eb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e2ae97bc829b4200b8294512083c63fea508486f57fdb8f5189ce04ad45338`

```dockerfile
```

-	Layers:
	-	`sha256:b8fe221f472526bc3541053eeee79ae059072673dda8fa620160d9b8736ca725`  
		Last Modified: Fri, 06 Jun 2025 19:42:45 GMT  
		Size: 39.1 KB (39148 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:5e3dc01e40c9749f27b78bd1618d6ed9a0b27b32462d615e0658fb74ddb7a36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180223120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d8822aac079f3f8ae18783aa61e0993d20cface9a739b45d0d9edd5ef0a0d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162264c942aa762db417d45ba0a061dc8a07fdceff32a29a2d59afdc5dce9f9`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae464486e7a7b754207a11225be678aa24148395332f33c785867c1ee4adcd`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 98.1 MB (98128413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa473689d317e799934b0b99abeaba5a91da4380c0b6148373000ed23bde9ba2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c2eb5e806f90915c98adca0127759107240352870bfe86a7178c29ff06f3b`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 20.1 MB (20121045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0dcaea15d7a4ebb0f4028699191ca3aa2002cfeec7788806c673ebb001eade`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e656b0988010277ad979af2247a277d3699b9eef4559bbf50725b446fb4510`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ead0ec2347e3e26a75d8fe7e72e9d04edd294c277d34306f347f23aad493a`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 13.7 MB (13745867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b512964d5c44935132ea8379fa9ec04c714c25fbc8219ce9be9d17e22e0e8`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7c2433f4eeaca738aea13d5ddf73f3460a52426b6723b86b421095fef4c214`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 13.8 MB (13808729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4f121a271b4e117ea00e6520f524ec468a213582287d34fb87b2a956289bab`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324eb62460519ea7e4f27b42438565313549fd03016b68e94728d8bc1d9013e2`  
		Last Modified: Tue, 03 Jun 2025 13:31:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d960895d240c87088356d9df9f326c23f0a465052bd89d61d8bb66cc44663`  
		Last Modified: Tue, 03 Jun 2025 13:31:22 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fb3c9eb85fadba28e0f81719e24e173ea924d15c94ef8109128b9993dc99ed`  
		Last Modified: Tue, 03 Jun 2025 14:20:49 GMT  
		Size: 575.9 KB (575941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab1d1a8ef08912e00cb9a1b40da2111ce02eea04af1cc3156f653dad8097130`  
		Last Modified: Tue, 03 Jun 2025 14:20:48 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bc151f121d0d89abd80b070368889781193f30f7ddd602cfbf3448bff4788a`  
		Last Modified: Tue, 03 Jun 2025 14:20:49 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc7268b608da059c36080c7c9cd2dff186dac7b108189110d005059d7bb2ff`  
		Last Modified: Tue, 03 Jun 2025 14:20:50 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163d1b026b93ffe547d2206e7ee682528bc46d3f1a164f86072479ff2e1bd839`  
		Last Modified: Tue, 03 Jun 2025 14:20:50 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396a41ffc639bfce2d3343f278dadda9c3eb931223d405d6c1325729bb78160`  
		Last Modified: Tue, 03 Jun 2025 14:20:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b11d1b563a49bd1c807ac22e9d4a0a50aba6dfb3b550b4586b20dddd713c9`  
		Last Modified: Tue, 03 Jun 2025 14:20:51 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:27d2d1f30a36860d812d85d309584c65176787fdcb0fc7046d2948517103a584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 KB (39197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a3576b6f8a6556dc70a79068c8a19b598d255758671b787deadb68992aa58`

```dockerfile
```

-	Layers:
	-	`sha256:8c57e640c4ef55ede90daad94bc8d9844bfc30807dc24d4feee095490d280a85`  
		Last Modified: Fri, 06 Jun 2025 19:42:55 GMT  
		Size: 39.2 KB (39197 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:6111b59d28aace971bd127c209e10cc5a35c1652d7b6f198ed3c6e6e6958576d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186025316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6601faac4ffda2dc3491862ec592fd623e32299c905a74ff8141aba34a725d37`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22ddc18304ed3a1d53a7aef150fc623c71d6e2e5271505d97a5edd99adba64`  
		Last Modified: Tue, 03 Jun 2025 16:41:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f751008f4f5f49a30f966b3edf120baf093461c51e3e4b81abe71c99f63bf945`  
		Last Modified: Tue, 03 Jun 2025 16:41:37 GMT  
		Size: 101.5 MB (101507553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6f48694a3a9f0b4a293da62d08226d43d596c6036f8108607128ad773547a9`  
		Last Modified: Tue, 03 Jun 2025 16:41:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb6561101e5ed629668ff0d4ba56f5de5178dbdf5d2ec61b7af79cd4526e632`  
		Last Modified: Tue, 03 Jun 2025 16:41:28 GMT  
		Size: 20.6 MB (20638542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7922a39b24883d34c49da129820f2b0b53bc9440a6e353b8dbaa33551622a11a`  
		Last Modified: Tue, 03 Jun 2025 16:41:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3b06e384b21cf160b0ac6a79c7e8fc40f344e78c46f66e25ae86bfc90f274b`  
		Last Modified: Tue, 03 Jun 2025 16:41:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc639ace7c0fb7860ddef8f1275605c96c2b2ab6e5502700755c05019b53bac2`  
		Last Modified: Tue, 03 Jun 2025 16:41:24 GMT  
		Size: 13.7 MB (13745164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acebfdaa4e9d2a44a67564d6e028b0f99de391096de90c4130772d701f036a65`  
		Last Modified: Tue, 03 Jun 2025 16:41:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ee0252dd7c8e12f9a2b1825d33bd183f6307199e2b7c812b69c23f07b1bc32`  
		Last Modified: Tue, 03 Jun 2025 16:41:27 GMT  
		Size: 14.5 MB (14462610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68961fcee0e3e7ce72956398cdf90bd155a08748f6304409833df58ed9aea99`  
		Last Modified: Tue, 03 Jun 2025 16:41:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21915bbc8474349d4aac2b1fda5d6c15217674b0901ac0f3932db97ea613b902`  
		Last Modified: Tue, 03 Jun 2025 16:41:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743f602b299559c9d6f94b8d1950c8a009afdd1bcd4653a574d2821d583c3f8`  
		Last Modified: Tue, 03 Jun 2025 16:41:22 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99894a9dcbfb1afe4aab3b1dbc4f4701f49fd1e2e0e4e23a675f0613cd47f00d`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 686.1 KB (686108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23373da2acabf8d237f9fc30774a4a358359d0b273f9eb131fa259765c166e07`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae4a6c5fe301f857d99abd7dbe0bc273e3ccdb37395d3a2a14255706e4f8c61`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08605b15ed54921d89bbd94879ffe8f3b530ad93be3763d87dcd6b44d8d16703`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dbd2b6ca80b675a499cf0b98071a7110a767024d8773718120e3f0a62a6f64`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53858302db5010bd261b95ab5c4b9a98fb9d87a8f020c49fb056758619aaf19`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44465e7c3ef46cd3495c89a58d94cbc8c40f8b110289f972ffd2627119685e1e`  
		Last Modified: Wed, 21 May 2025 23:37:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:8b940f3262ee386393ad666f810d385e1fd7e07c5fe174663ec7b07c525330fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (38951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa1698aa944eaad79577b8acb1e2848abd6b4fbc6a7183188804bdec8979389`

```dockerfile
```

-	Layers:
	-	`sha256:f0d03ae4d5ea2e95cf6ddb5071f70d3d5e3810fa18e563671207dc8cb7bf89e0`  
		Last Modified: Fri, 06 Jun 2025 19:43:04 GMT  
		Size: 39.0 KB (38951 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; mips64le

```console
$ docker pull yourls@sha256:d7cdf5662ac0c8f3716ef23f89bccd6fa24de6d7355ad0ccb9add286e52989ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162005469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55257421a16359412bb6cef426ff060ebd78a4dfd78ca080e7c6d5af6efc0559`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b2d065c1ae51e1de38627f7944c17a1a577f385d527b6bf91b589844d0689`  
		Last Modified: Tue, 03 Jun 2025 14:07:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5af86f1704d74588bed3a81502d5b84aaa58ec860f5145be4f0fd74e864385c`  
		Last Modified: Tue, 03 Jun 2025 14:07:31 GMT  
		Size: 80.7 MB (80670380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286f15cd07eee9997888e6110e809261f661823a9bcc233812db970c553fb13`  
		Last Modified: Tue, 03 Jun 2025 14:07:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e479bd14b9daf00989f06fcc9447b78b71f0f81af33588568f8d5514c9dd5e5c`  
		Last Modified: Tue, 03 Jun 2025 14:07:25 GMT  
		Size: 20.1 MB (20069286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516d875c6c1a415ec40dd717d030fcbfa51d61ff8a893d36a8f709ff81ba6b86`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b026852626d4fa32104a7a1d8f0f0dc1b9dd3a30a7d8eea66f49a4d583c81`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883914e764b499e4552cf9a83af6cfe99160e113e57c1e0d6611e3a4fd6ac005`  
		Last Modified: Thu, 05 Jun 2025 12:15:23 GMT  
		Size: 13.7 MB (13744011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80652a093325ef5e494194dcfc8e349955eaa3a00fcea8a0169db624b9729706`  
		Last Modified: Thu, 05 Jun 2025 12:15:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86baaf906649a27b810ad3a6a22b913061b3f624a9c2542f21051d1805f10d`  
		Last Modified: Thu, 05 Jun 2025 12:15:23 GMT  
		Size: 13.1 MB (13062258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7d10a9f2df8edb1d9249695ac8a465d8b7589c034a47e673f19206b56b400`  
		Last Modified: Thu, 05 Jun 2025 12:15:22 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67922b71187164e1320548beb3f9cb6e9e3fc1e55a5500c02968ef0d519489b1`  
		Last Modified: Thu, 05 Jun 2025 12:15:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf08b91e36d9963a4479a83a3230363238e7df49a74f662e63e300b2e4d7eb2`  
		Last Modified: Thu, 05 Jun 2025 12:15:24 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c513bd2c5482326d4bba09fb511e1a232250018492d49b4a5df8debbf126814d`  
		Last Modified: Thu, 22 May 2025 14:23:56 GMT  
		Size: 169.8 KB (169815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7351724c15d1f28f4bf5198844ab9603e4875d8038150f39adf2c0927e1010c`  
		Last Modified: Thu, 22 May 2025 14:23:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3a04186be03324511f7c3858d21ef36704d77df49adc38542d9124c5901722`  
		Last Modified: Thu, 22 May 2025 14:23:56 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1210c7ceb513fa9c46ffb18a0d335269477579c5a0c8715ab5df4ba240c357b`  
		Last Modified: Thu, 22 May 2025 14:23:56 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5e223087e135de564cf8277805e972e452088f878bb01aa889957c516c1a3`  
		Last Modified: Thu, 22 May 2025 14:23:56 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14eed53ef880527a111d947f220d9fa22cad1a302d5d487c99b49df8f3e1e7b`  
		Last Modified: Thu, 22 May 2025 14:23:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e098dd5bcf26baa84af8ad4fc66fc28da7313f2833c0c14f9f8507305cb0b129`  
		Last Modified: Thu, 22 May 2025 14:23:57 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:8d5e03c2f80a5f5d4d56d74fd17afea03798362d5f00efa55cdae00990cf1eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d1239971e732f8f3667cba6b428447bb17b8b773a91b402228c8db8de6c8c2`

```dockerfile
```

-	Layers:
	-	`sha256:70f931d6b6209e693c22c5c151ad0da756f5333ea0b84611f61236622d920a71`  
		Last Modified: Fri, 06 Jun 2025 19:43:14 GMT  
		Size: 39.1 KB (39111 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:567e336a9a9bc64b9a3163c5a45af8b76b21a07fd5da38820d8a9d2c063774e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191017970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852029ce0a0a8cf3d34bafa99e7275c8cfef0fcf3e55e2d366abbfce5d4f578f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c8f6558609f4eda938f055dbc23ff092be663afb6bb7d22397dead0d155e4`  
		Last Modified: Tue, 03 Jun 2025 14:07:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95a24f0f53c73df78df26adee8011626da1dd6f4150d1531843c39f2fa7279`  
		Last Modified: Tue, 03 Jun 2025 14:07:40 GMT  
		Size: 103.3 MB (103318542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbbd3cd9d8dd0b29377d19251990f04906ba83ff91eb897513badc4d334a010`  
		Last Modified: Tue, 03 Jun 2025 14:07:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a26aa298acacfff30831e2b7eac827bbc698998de1d7f5e4980067b0e49b8`  
		Last Modified: Tue, 03 Jun 2025 14:07:38 GMT  
		Size: 21.3 MB (21308439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1af0ff654deb6e781136c8bf50cbc1620ff308937fa9386f4e352a660b1`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6045a09715f2b5e30561b3fe36e20f490290134575d98d8260aea00ce45d6`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f43812df8c4d29b1c0a1ecf920b8239afac2d66bd3686bd01c709bba839a3f`  
		Last Modified: Fri, 06 Jun 2025 17:45:27 GMT  
		Size: 13.7 MB (13747602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f9da58ae866f5859bb8a306f71620e369c94ff46ca7d029fa087d8cde42bf7`  
		Last Modified: Fri, 06 Jun 2025 17:45:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058c7b689fc249719dbd29d09d4f1a9a4539c93184ee950e4189aaa12927d31a`  
		Last Modified: Fri, 06 Jun 2025 17:45:38 GMT  
		Size: 14.6 MB (14587996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2839fa5c94f1361222bb286c1dca3dcd8fe5af5e570f7e330d571af4779efe`  
		Last Modified: Fri, 06 Jun 2025 17:45:26 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bd74f69b5df50f092f45e92d55567e5591b95b0fa39ec24209558c76232f13`  
		Last Modified: Fri, 06 Jun 2025 17:45:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c18bfe1ab775d07f039302c31668e70bb65a664f3fc22290875c2c194d061b`  
		Last Modified: Fri, 06 Jun 2025 17:45:27 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e442d04693d4a3844ce1f68343f4c6b3241f355a2a9b1ff09e33885f339f96`  
		Last Modified: Fri, 06 Jun 2025 19:06:37 GMT  
		Size: 210.6 KB (210627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39489cd4fa2739be36923da81b1f0dfab7f99fad07b12263d44acaa5c0e3e5c9`  
		Last Modified: Fri, 06 Jun 2025 19:06:37 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adca007d77c7d8bcd5af5d2d2a99e1949765950a3147cdb7ddfb8466d662a49`  
		Last Modified: Fri, 06 Jun 2025 19:06:37 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dd8edf9d04090f03947f4184e413cf2c9239c2958956887135e253031afcd7`  
		Last Modified: Fri, 06 Jun 2025 19:06:39 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183e78f540174c31ad03b73f663aa2a0b220eb7fb9aa90455b2a07c3251a7654`  
		Last Modified: Fri, 06 Jun 2025 19:06:38 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac1741e840ef45464be4d201dc1c561426d2fbb1fa6a8880b82a5a930197ad0`  
		Last Modified: Fri, 06 Jun 2025 19:06:38 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d9885036da3e87ac1cfd32ab5847cfe2aabaf7269b10d348fb04efcee1af5f`  
		Last Modified: Fri, 06 Jun 2025 19:06:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:9841a6f30f7e56d16ee60c4a74ac4c174e791e1958c57d4f8c2497448169d39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d2e17f3e621344a8b17c84a7c003f5ec0894f6700bc089709484e8968a01a0`

```dockerfile
```

-	Layers:
	-	`sha256:d02fa99a9714c773ee81bf371ac8b2ece07f80a6b9dfbe8eba9b624bf20abcb8`  
		Last Modified: Fri, 06 Jun 2025 19:43:23 GMT  
		Size: 39.1 KB (39083 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; s390x

```console
$ docker pull yourls@sha256:e0027674458cd534c583ef8ce4c6a6de722fa7be69450a5a0655aa129df32f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160847566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43c245f04cf7fcda79734d5238ffb382b122efdecb9d299745906c7b2c7976d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e64042a8c749f17bfb3b660d34f4e07edd06c81899da76f0b866d5592048d`  
		Last Modified: Tue, 03 Jun 2025 14:07:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae504c4e6cef239a74e8e2bc8e65a5adfc4fd86d2ce43efcb6fcf7b948f38c6`  
		Last Modified: Tue, 03 Jun 2025 14:07:59 GMT  
		Size: 80.8 MB (80824650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9845dffb4e53bff01a8cc52346eef48b2a105a195a30ab820e7df1e9682a7a`  
		Last Modified: Tue, 03 Jun 2025 14:07:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d076bcc60b618a69a01c7cec130e41e98f5d4ef5c1db46cceb7b121173ee5`  
		Last Modified: Tue, 03 Jun 2025 14:07:45 GMT  
		Size: 19.9 MB (19895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf1bc43a3bf929df811240c21fd8f7c539c8a225d996960c3345d25963bc4c`  
		Last Modified: Tue, 03 Jun 2025 14:07:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aaa5fa23882a5d77ecfeca856eb346385fec09755a18d670b6ceb0cba14cd0`  
		Last Modified: Tue, 03 Jun 2025 14:07:33 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0924551c0bf4e03568fb1100c64d34624e75a762476c08d7931652f531ac22`  
		Last Modified: Fri, 06 Jun 2025 17:42:06 GMT  
		Size: 13.7 MB (13746343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5167ab1c48b4065c4253b84c14072b239ded1eab7015d27e29a83695e1965f3`  
		Last Modified: Fri, 06 Jun 2025 17:42:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91701af16d46158c42934fb257b40f093341cc2af0b6e5e56d0536059772b8df`  
		Last Modified: Fri, 06 Jun 2025 17:42:15 GMT  
		Size: 13.5 MB (13540624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6360894dab6efe3e216eb60644d89d60fcae62386662f63a56655bd4d5f89e35`  
		Last Modified: Fri, 06 Jun 2025 17:42:05 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80a74b1c6106d40cfe83d4a5aadd3463518bec86e00561243b71591a3a817c`  
		Last Modified: Fri, 06 Jun 2025 17:41:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e60ac7a7ffdc5aefdb09cdababaf527b62cbaa22d32959fdd047feff668834`  
		Last Modified: Fri, 06 Jun 2025 17:42:00 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385f9ff6696a250fcb6bbe90863e4a8a118e3b20b3a6d91c949d24e6a2ba2f1`  
		Last Modified: Fri, 06 Jun 2025 18:51:51 GMT  
		Size: 180.0 KB (179979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdef9ae44f29b02987e92af625ba111b6fb1b1b0ad301a048d64cd1350a2e3d`  
		Last Modified: Fri, 06 Jun 2025 18:51:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d348698edd4639631d92f50c5d39c9c6503af3a04e1cfd18a7f608b2af305553`  
		Last Modified: Fri, 06 Jun 2025 18:51:55 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36781c5f35776ab4c4ce89f8da8feccab88fcd414f41c2f1a62b86af6830b2d3`  
		Last Modified: Fri, 06 Jun 2025 18:51:58 GMT  
		Size: 5.8 MB (5767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3948cab7683f8e933b0bca774e0da18ca16659eb24996d4f08075d3c736e2d00`  
		Last Modified: Fri, 06 Jun 2025 18:51:58 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cd78bc8a6309ef124d0668c8894d8f6ac080e94dfc078b21a2f34cfd84b54`  
		Last Modified: Fri, 06 Jun 2025 18:51:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001d4c80b3f3f05a8f15ae7060afdd5edaaa23ba212acb98ed6ad7b28b2c656a`  
		Last Modified: Fri, 06 Jun 2025 18:51:58 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:062d5e75758d40c004564e3980acc34e96e117dbd80f40d16e5469afcd2b2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (39000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e0a6814f44b2078b7f0f4b917c76a82032893aa49396882d062f27d9f1451`

```dockerfile
```

-	Layers:
	-	`sha256:1e2e2071a2483b2466043ce179670a7fde849620e708e1613d233aa1dc54a96f`  
		Last Modified: Fri, 06 Jun 2025 19:43:27 GMT  
		Size: 39.0 KB (39000 bytes)  
		MIME: application/vnd.in-toto+json
